FROM python:3.11-slim  
  → Sets the base image. Our container starts as a lightweight Python environment.

WORKDIR /app  
  → Sets the working directory inside the container. All following commands run here.

COPY app.py .  
  → Copies our app file from the local machine into the container's /app directory.

RUN echo "App files copied successfully"  
  → Runs a command during the build step (normally used for installing packages, e.g. pip install).

CMD ["python", "app.py"]  
  → The command that runs when the container starts. Launches our web server.
