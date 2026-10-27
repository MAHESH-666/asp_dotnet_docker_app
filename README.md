# ASP.NET Core + Docker Sample

A small ASP.NET Core MVC sample packaged with a Dockerfile to demonstrate building and running a web application in a container.

## Technology

- C#
- ASP.NET Core / .NET Core 3.1 (as specified by the project file)
- Docker

> **Framework note:** .NET Core 3.1 is out of support. Treat this as a legacy learning sample and consider upgrading to a supported .NET release before using it for new or production work.

## Prerequisites

- Docker Desktop or Docker Engine
- .NET SDK matching the project when building outside Docker

## Run with Docker

From the repository root:

```bash
docker build -t aspnet-docker-sample .
docker run --rm -p 8080:80 aspnet-docker-sample
```

Then open http://localhost:8080. If the Dockerfile uses a different internal port, use the port declared in that file.

## Run from Visual Studio

Open the web project, restore NuGet packages, select the web project as startup, and run it with IIS Express or the configured launch profile.

## Notes

Check the Dockerfile and launch settings before running because port mappings vary by image configuration. Do not add credentials or environment-specific configuration to the image.
