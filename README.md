Guess the Capital Game


Overview
This is a web-based Guess the Capital game application that challenges users to guess the capital cities of different countries. It was developed as part of a cloud computing course to explore containerization, deployment, and cloud-based application management. The project uses HTML, CSS, and JavaScript for the front-end, with Docker for containerization and IBM Cloud Code Engine for cloud deployment.

Project Structure
/fyidw-guess-the-capital
│
├── index.html      # The main HTML page of the game
├── script.js       # JavaScript logic for game interactions
├── style.css       # Styling for the game interface
├── data.json       # JSON file with country and capital data
└── Dockerfile      # Docker configuration for containerization
Features
Interactive Gameplay: Users can guess the capital of a given country.
Cloud Deployment: The application is deployed on IBM Cloud, making it accessible via a web URL.
Technologies Used
Frontend: HTML, CSS, JavaScript
Cloud: IBM Cloud Code Engine
Containerization: Docker
Version Control: Git, GitHub
Setup Instructions
To run this project locally, follow these steps:

Clone the Repository
git clone https://github.com/your-username/guess-the-capital.git
cd guess-the-capital
Run the Application Locally
Start a local server:
python3 -m http.server
Open a browser and go to http://localhost:8000 to play the game.

Dockerization
To containerize the application with Docker, ensure you have Docker installed. Then, build and run the Docker container:

Build the Docker image:
docker build -t guess-the-capital .
Run the Docker container:
docker run -it -d -p 8080:80 guess-the-capital
Open the browser and navigate to http://localhost:8080 to access the game.

Deployment on IBM Cloud
This project was deployed to IBM Cloud using Code Engine. Below are the steps taken to deploy the containerized application to the cloud:

Build the image for IBM Cloud:
docker build . -t us.icr.io/${SN_ICR_NAMESPACE}/guess-the-capital
Push the Docker image to IBM Cloud Container Registry:
docker push us.icr.io/${SN_ICR_NAMESPACE}/guess-the-capital
Deploy the image on IBM Cloud Code Engine:
ibmcloud ce application create --name guess-the-capital --image us.icr.io/${SN_ICR_NAMESPACE}/guess-the-capital --registry-secret icr-secret --port 80
Access the deployed application: Once deployed, the application is accessible via the cloud URL:
https://guess-the-capital.somerandomalphanumeric.us-south.codeengine.appdomain.cloud


This project was a valuable exercise in modern cloud-based application development. It allowed me to deepen my understanding of containerization and cloud deployment using Docker and IBM Cloud Code Engine. I look forward to further enhancing the game and exploring more cloud-native features.


