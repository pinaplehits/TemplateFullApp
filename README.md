# TemplateFullApp

This project is a combination of two submodules: [TemplateWebApi](https://github.com/pinaplehits/TemplateWebApi) and [TemplateViteVue](https://github.com/pinaplehits/TemplateViteVue).

## Getting Started

After cloning this repository, you need to initialize and update the submodules. Run the following commands:

```sh
git submodule update --init --remote --depth 1
git submodule foreach git checkout master
git submodule foreach git pull origin master
```

## Building and Running the Project

This project consists of a frontend and a backend that can be built and run using Docker Compose. There are separate Docker Compose files for development and production environments.

### Building and Running in Production

To build and run the project in production, use the following command in the root directory of the project:

```sh
docker-compose up --build
```

This command will build both the frontend and the backend of the project as specified in the [docker-compose.yml](docker-compose.yml) file and run them in the background. The frontend will be accessible at <http://localhost:80> and the backend at <http://localhost:90>.

### Building and Running in Development

To build and run the project in development, use the following command in the root directory of the project:

```sh
docker-compose -f docker-compose.dev.yml up --build
```

This command will build both the frontend and the backend of the project as specified in the [docker-compose.dev.yml](docker-compose.dev.yml) file and run them in the background. The frontend will be accessible at <http://localhost:81> and the backend at <http://localhost:92>.
