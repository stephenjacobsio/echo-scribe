# EchoScribe

EchoScribe is a modern, scalable blogging platform, built as a microservices architecture using .NET 8. This project showcases best practices in developing RESTful APIs, microservices orchestration, and cloud-native application development.

## Features 🌟

- Microservices architecture with individual services for Users, Blogs, and Comments.
- RESTful API endpoints implemented with .NET 8 minimal APIs.
- Robust data persistence with PostgreSQL.
- Asynchronous communication and message queuing (e.g., RabbitMQ/Kafka).
- Containerization with Docker and orchestration with Kubernetes.
- Comprehensive unit and integration testing with NUnit.
- CI/CD integration using GitHub Actions.
- Global exception handling and robust logging.

## Services 📦

- **UserService**: Manages user information and authentication.
- **BlogService**: Handles blog post creation, updates, and retrieval.
- **CommentService**: Manages comments on blog posts.
- **ApiGateway**: A central point for routing requests to respective services.

## Getting Started 🚀

These instructions will get a copy of EchoScribe up and running on your local machine for development and testing purposes.

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Docker](https://www.docker.com/get-started)
- [PostgreSQL](https://www.postgresql.org/download/)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/rootiovo/echoscribe.git
   ```

2. Navigate to the service directory (e.g., UserService) you want to run:
   ```bash
   cd EchoScribe.UserService/src/EchoScribe.UserService.API
   ```

3. Build and run the service:
   ```bash
   dotnet build
   dotnet run
   ```

4. Repeat steps 2 and 3 for other services, or use Docker Compose at the root:
   ```bash
   docker-compose up
   ```

## Running the Tests ⚙️

Execute the following commands to run the automated tests for EchoScribe.

### Unit Tests

```bash
dotnet test EchoScribe.UserService.Tests
```

### Integration Tests

```bash
dotnet test EchoScribe.UserService.IntegrationTests
```

## CI/CD Pipeline and Deployment 🚀

EchoScribe employs a robust CI/CD pipeline using GitHub Actions, ensuring that every commit and pull request is built, tested, and, upon merge, automatically deployed to an Amazon EKS (Elastic Kubernetes Service) cluster. This setup guarantees a consistent and reliable delivery process, essential for maintaining high-quality software.

### Key Features of the Pipeline

- **Automated Builds**: On every push and pull request to the `main` branch, the code is automatically built to check for compilation errors.
- **Testing**: The pipeline runs all unit and integration tests, ensuring that new changes do not break existing functionality.
- **Coding Standards Check**: StyleCop is integrated into the pipeline to enforce coding standards and maintain code quality.
- **Automated Deployment**: Merged changes are automatically deployed to the Amazon EKS cluster, ensuring that the latest version of the application is always running.

### Workflow Steps

1. **Build**: The application is compiled to check for any compilation errors.
2. **Test**: NUnit is used to run all unit and integration tests.
3. **StyleCop Check**: Coding standards are enforced through automated checks, ensuring adherence to best practices.
4. **Deployment**: Upon successful completion of the above steps, the application is deployed to Amazon EKS.

### Amazon EKS Deployment

- The application uses Kubernetes manifests for deployment, ensuring scalable and manageable orchestration.
- The CI/CD pipeline is configured with necessary AWS credentials for secure deployment to the EKS cluster.

### Local Development vs. Production Deployment

- For local development, developers can use Docker Compose to run the application in a containerized environment.
- The production deployment is handled through the CI/CD pipeline, ensuring a consistent and reliable process from development to production.

This CI/CD process forms the backbone of EchoScribe's development workflow, embodying best practices in continuous integration and deployment.

## Support ☕

If you like my work and want to support me, consider buying me a coffee!

[![Buy Me A Coffee](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/yourusername)

## Contributing 🤝

Contributions to EchoScribe are welcome! Please read [CONTRIBUTING.md](https://github.com/rootiovo/echoscribe/CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License 📄



EchoScribe is licensed under the MIT License - see the [LICENSE.md](https://github.com/rootiovo/echoscribe/LICENSE.md) file for details.

## Acknowledgments 🙏

- Thanks to all contributors and supporters of the EchoScribe project.
