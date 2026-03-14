# Django Todo App with CI/CD, Docker & Kubernetes

A simple **Todo List web application built with Django**, containerized using **Docker**, and prepared for **CI/CD pipelines and Kubernetes deployment**.

This project demonstrates how a basic Django application can be packaged and deployed using modern DevOps practices.

---

## Features

* Create and manage todo tasks
* Django admin panel
* Dockerized application
* Docker Compose setup
* Kubernetes deployment manifests
* CI/CD ready project structure

---

## Application Preview

![Todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)

---

## Project Structure

```
django-todo-cicd
│
├── Dockerfile
├── docker-compose.yml
├── Jenkinsfile
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── MYSQL-DB/
│       ├── configMap.yml
│       ├── deployment.yml
│       └── secret.yml
│
├── todoApp/
├── staticfiles/
├── manage.py
└── requirements.txt
```

---

## Requirements

Make sure the following tools are installed:

* Python 3.x
* pip
* Django
* Docker (optional for containerized setup)
* Kubernetes / Minikube (optional)

---

## Local Setup (Without Docker)

### Clone the Repository

```bash
git clone https://github.com/YashChauhan321/django-todo-cicd.git
cd django-todo-cicd
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

### Run Database Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

### Create Admin User

```bash
python manage.py createsuperuser
```

Follow the prompts and enter:

* username
* password
* email

---

### Run the Application

```bash
python manage.py runserver
```

Open your browser and go to:

```
http://127.0.0.1:8000/todos
```

---

## Running with Docker

Build the Docker image:

```bash
docker build -t django-todo .
```

Run the container:

```bash
docker run -p 8000:8000 django-todo
```

---

## Kubernetes Deployment

The repository contains Kubernetes manifests inside the `k8s/` directory.

To deploy the application:

```bash
kubectl apply -f k8s/
```

This will create:

* Django application deployment
* MySQL database deployment
* Kubernetes services
* ConfigMaps and Secrets

---

## CI/CD

The project includes a **Jenkinsfile** which can be used to create a CI/CD pipeline that:

1. Pulls the repository
2. Builds the Docker image
3. Runs tests
4. Deploys the application to Kubernetes

---

## Tech Stack

* Django
* Python
* Docker
* Kubernetes
* Jenkins
* MySQL
* HTML / CSS

---

## Author

Yash Chauhan

---

## License

This project is licensed under the MIT License.
