# Microservices Architecture

This project demonstrates a microservices architecture. It includes multiple services that communicate with each other to form a complete application. The services included in this project are:

- **[Authentication Service](https://github.com/Prosperibe12/microservice-auth)**: Manages user registration and authentication routes.
- **[Gateway Service](https://github.com/Prosperibe12/gateway-service)**: Manages the routing of requests to the appropriate services.
- **[RabbitMQ Service](https://github.com/Prosperibe12/rabbitmq-service)**: Handles messaging between services.
- **[MongoDB Service](./mongodb_service/README.md)**: Manages MongoDB database operations.
- **[DB Service](./db_service/README.md)**: Manages the database operations.
- **[Notification Service](./notification_service/README.md)**: Sends notifications to users.
- **[Video to MP3 Service](./video_to_mp3_service/README.md)**: Converts video files to MP3 format.
- **[PDF to Podcast Service](./pdf_to_podcast_service/README.md)**: Converts PDF documents to podcast format.

## Overview

The primary function is to take a video file, authenticate the user via the API Gateway, and place the video in a queue for the Video to MP3 Converter service. This service converts the video to MP3 format and sends a notification to the user to download the file.

The secondary function allows a user to send a PDF file to the gateway, which routes it to the PDF to Podcast Converter service. This service generates a two-person podcast from the PDF and notifies the user once the podcast is ready.

The MongoDB Service stores the videos for easy retrieval. This service ensures that all video files are saved in a MongoDB database, allowing for efficient access and management of video data. It plays a crucial role in the overall architecture by providing a reliable storage solution for video files.

## Architecture

![Microservices Architecture](architecture.png)

The above diagram illustrates the architecture of the microservices in this project.

## Getting Started

To get started with this project, follow these steps:

1. Clone the repository.
2. Navigate to the project directory.
3. Follow the instructions in each service's README to set up and run the services.

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) before submitting a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or inquiries, please contact [Prosperibe12@gmail.com](mailto:Prosperibe12@gmail.com).