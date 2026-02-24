# 🧠 Project Overview
This project is a comprehensive application that utilizes a reverse proxy server with Nginx, multiple backend nodes with Docker, and a monitoring system with Promtail and Loki. The application is designed to handle incoming HTTP requests, route them to the corresponding upstream servers, and manage SSL certificates. The project consists of multiple components, including a proxy service, client services, and a monitoring system. The core features of the project include load balancing, SSL termination, and log collection and analysis.
Also, this project is for my own documentation for client server setup (backend) when my position was a DevOps Engineer at MAPID.

## 🚀 Key Features
- **Reverse Proxy**: Nginx acts as a reverse proxy server, routing incoming requests to the corresponding upstream servers.
- **Load Balancing**: The application uses load balancing to distribute incoming traffic across multiple backend nodes.
- **SSL Termination**: Nginx handles SSL termination, providing a secure connection between the client and the server.
- **Log Collection and Analysis**: Promtail and Loki are used for log collection and analysis, providing insights into the application's performance and behavior.
- **Dockerization**: The application uses Docker to containerize the backend nodes, providing a scalable and efficient deployment solution.

## 🛠️ Tech Stack
- **Nginx**: Used as a reverse proxy server and for load balancing.
- **Docker**: Used for containerizing the backend nodes and managing the application's deployment.
- **Promtail**: Used for log collection and forwarding to Loki.
- **Loki**: Used for log storage and analysis.
- **Certbot**: Used for SSL certificate management.
- **Amazon ECR**: Used for storing Docker images.
- **Node.js**: Used as a backend technology for the client services.
- **Bun.js**: Used as a backend technology for the client services.

## 📦 Getting Started / Setup Instructions
### Prerequisites
- Docker installed on the system
- AWS CLI installed on the system
- Amazon user with ECR `AmazonEC2ContainerRegistryPullOnly` policy
- Loki API 

### Installation
1. Clone the repository to your local machine.
2. Make sure the Amazon CLI and Amazon User is correctly configured in your local machine.
3. Navigate to the clients directory. Make sure the environment variables is on the correct directory and then run `docker-compose up -d` to start the client services.
4. Configure the Nginx configuration file to point to the correct upstream servers.
5. Navigate to the proxy directory and run `docker-compose up -d` to start the proxy service.
6. Configure the Promtail configuration file to point to the correct Loki API.

### Running Locally
1. Start the client services by running `docker-compose up -d` in the clients directory.
2. Start the proxy service by running `docker-compose up -d` in the proxy directory.
3. Start the monitoring service by running `docker-compose up -d` in the monitoring directory.
4. Access the application by navigating to `http://localhost` in your web browser.

## 📂 Project Structure
```markdown
.
├── clients
│   ├── client1
│   │   ├── docker-compose.yml
│   │   └── ...
│   ├── client2
│   │   ├── docker-compose.yml
│   │   └── ...
│   └── ...
├── monitoring
│   ├── promtail-config.yml
│   └── ...
├── proxy
│   ├── docker-compose.yml
│   ├── nginx.conf
│   └── ...
├── ...
└── README.md
```

## Setting Up CertBot
1. Make sure the DNS has been setup in route53 or any dns service
2. Run the following command 'docker compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot -d your-domain'

## 🤝 Contributing
Contributions are welcome and encouraged. To contribute, please fork the repository, make your changes, and submit a pull request.

## 📝 License
This project is licensed under the MIT License.

## 📬 Contact
For any questions or concerns, please contact us at [firmansyahwicaksono30@gmail.com](mailto:firmansyahwicaksono30@gmail.com).

## 💖 Thanks Message
Thank you for using our application. We hope you find it useful and efficient.

