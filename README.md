<h1 align="center" style="
  font-family: 'Barlow', sans-serif;
  font-size: 3.8em;
  font-weight: bold;
  text-transform: uppercase;
  margin-bottom: 40px;
  position: relative;
  color: #00aaff;
  text-shadow: 0 0 10px #00aaff, 0 0 20px #0077cc, 0 0 30px #003366;
  background: url('https://www.transparenttextures.com/patterns/cubes.png');
  -webkit-background-clip: text;
  background-clip: text;
  animation: fractalNetBlue 4s infinite ease-in-out;
">
  Post-Wave Project
</h1>

<style>
@keyframes fractalNetBlue {
  0% {
    text-shadow: 0 0 10px #00aaff, 0 0 20px #0077cc, 0 0 30px #003366;
    transform: scale(1);
  }
  50% {
    text-shadow: 0 0 20px #00aaff, 0 0 30px #0077cc, 0 0 40px #003366;
    transform: scale(1.05);
  }
  100% {
    text-shadow: 0 0 10px #00aaff, 0 0 20px #0077cc, 0 0 30px #003366;
    transform: scale(1);
  }
}
</style>

<div style="text-align: center; margin: 40px 0;">
  <div style="display: block; width: 100%; max-width: 600px; margin: 20px auto;">
    <a href="https://nick8787.github.io/post-wave-documentation/" target="_blank" style="text-decoration: none;">
      <div style="
        display: flex;
        align-items: center;
        justify-content: center;
        background: linear-gradient(135deg, #1e1e1e, #333333);
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.7);
        transition: transform 0.4s ease, box-shadow 0.4s ease;
        position: relative;
        overflow: hidden;
        font-family: 'Barlow', sans-serif;
        border: 1px solid rgba(255, 255, 255, 0.1);
      ">
        <img src="https://img.icons8.com/fluency/96/000000/document.png" alt="Documentation" width="40" style="margin-right: 15px; filter: brightness(0.9);">
        <span style="color: #ffffff; font-size: 1.3em; font-weight: bold; text-transform: uppercase;">Project Documentation</span>
        <div style="
          position: absolute;
          top: 50%;
          left: 50%;
          width: 200%;
          height: 200%;
          background: radial-gradient(circle, rgba(255, 255, 255, 0.1), transparent);
          transform: translate(-50%, -50%) scale(0);
          transition: transform 0.6s ease;
          border-radius: 50%;
          z-index: 0;
        "></div>
      </div>
    </a>
  </div>

  <div style="display: block; width: 100%; max-width: 600px; margin: 20px auto;">
    <a href="https://nick8787.github.io/post-wave-demo-project/" target="_blank" style="text-decoration: none;">
      <div style="
        display: flex;
        align-items: center;
        justify-content: center;
        background: linear-gradient(135deg, #1e1e1e, #333333);
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.7);
        transition: transform 0.4s ease, box-shadow 0.4s ease;
        position: relative;
        overflow: hidden;
        font-family: 'Barlow', sans-serif;
        border: 1px solid rgba(255, 255, 255, 0.1);
      ">
        <img src="https://img.icons8.com/fluency/96/000000/internet.png" alt="Live Project" width="40" style="margin-right: 15px; filter: brightness(0.9);">
        <span style="color: #ffffff; font-size: 1.3em; font-weight: bold; text-transform: uppercase;">Visit Live Project Site</span>
        <div style="
          position: absolute;
          top: 50%;
          left: 50%;
          width: 200%;
          height: 200%;
          background: radial-gradient(circle, rgba(255, 255, 255, 0.1), transparent);
          transform: translate(-50%, -50%) scale(0);
          transition: transform 0.6s ease;
          border-radius: 50%;
          z-index: 0;
        "></div>
      </div>
    </a>
  </div>
</div>

<style>
  a div:hover {
    transform: translateY(-8px) scale(1.05);
    box-shadow: 0 6px 18px rgba(0, 0, 0, 0.9);
  }
  
  a div:hover > div {
    transform: translate(-50%, -50%) scale(1);
  }

  a div span, a div img {
    position: relative;
    z-index: 1;
  }
</style>

<p align="center">
  <img src="images/post-wave-gif-1-last.gif" alt="Post-Wave Logo" />
</p>

## ⚙️ Project Overview

Post-Wave is a microservices-based platform that enables users to register, create posts and comments, and track all actions performed on the platform. The project serves as a learning tool for understanding microservices architecture, integration, and deployment.

## 🛠️ Tech Stack

The following technologies and tools were used in this project:

- **Java:** The primary programming language for developing microservices.
- **Spring Boot:** Used to build the microservices with RESTful APIs.
- **JWT & Spring Security:** Ensures secure user authentication and authorization.
- **Kafka:** Facilitates asynchronous communication between microservices.
- **Flyway:** Manages database migrations.
- **H2 & PostgreSQL:** H2 is used for local development, and PostgreSQL is used for production.
- **Docker:** Containerizes the application and its services.
- **IntelliJ IDEA Ultimate:** Integrated Development Environment (IDE) used for coding.

## 🚀 Deployment Workflow

The deployment process involves the following steps:

1. **Image Logs Stage:** Retrieve the last 1000 lines of Docker container logs from the remote server via SSH.
2. **Docker Stop Stage:** Stop and remove the current Docker container to prepare the server for deployment.
3. **Data Check Stage:** Validate the Docker environment, network, and user data on the server.
4. **Build JAR Stage:** Compile the application code into a JAR file using Maven.
5. **Build Docker Stage:** Create a new Docker image from the JAR file and push it to the Docker Registry.
6. **Deploy Stage:** Pull the new Docker image from the registry and deploy it on the server.

## 🗄️ Database & Hosting

The project uses a managed PostgreSQL database hosted on the ScaleGrid platform, leveraging AWS for high availability and scalability. The application is hosted on a dedicated server that uses Docker for deployment, ensuring flexible resource management and maintaining high performance.

### 📦 Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/nick8787/post-wave-demo-project.git
   cd post-wave
