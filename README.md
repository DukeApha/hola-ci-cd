# 🚀 Proyecto CI/CD con GitHub Actions + Docker + Render

Este proyecto es una aplicación web desarrollada con Node.js y Express, que implementa un flujo completo de CI/CD utilizando GitHub Actions, Docker Hub y Render para automatizar pruebas, construcción y despliegue.

---

## 📌 Descripción

La aplicación expone un endpoint básico:
GET /

Y retorna la siguiente respuesta:
Hola Mundo DevOps 🚀

---

## 🧱 Tecnologías utilizadas

- Node.js
- Express
- Jest
- Supertest
- Docker
- GitHub Actions
- Docker Hub
- Render

---

## 📁 Estructura del proyecto
hola-ci-cd/
│── app.js
│── server.js
│── package.json
│── package-lock.json
│── Dockerfile
│── .dockerignore
│── test/
│ └── app.test.js
│── .github/
│ └── workflows/
│ └── ci-cd.yml
│── README.md


---

## ⚙️ Funcionamiento del sistema

El proyecto sigue una arquitectura de integración y despliegue continuo (CI/CD).

Cada vez que se realiza un push a la rama `main`, se ejecuta automáticamente el pipeline en GitHub Actions con los siguientes pasos:

---

### 1. Instalación de dependencias
Se instalan todas las dependencias necesarias del proyecto.

```bash id="step1"
npm install

2. Ejecución de pruebas

Se ejecutan las pruebas unitarias para validar el funcionamiento de la aplicación.

npm test

3. Construcción de imagen Docker

Se genera la imagen de la aplicación.

docker build -t usuario/hola-ci-cd .

4. Publicación en Docker Hub

La imagen se sube automáticamente al repositorio de Docker Hub.

5. Despliegue en Render

La aplicación se despliega automáticamente en producción.

🧪 Ejecución local

Para ejecutar el proyecto en entorno local:

npm install
npm start

🧪 Ejecución de pruebas
npm test

🐳 Ejecución con Docker
docker build -t hola-ci-cd .
docker run -p 3000:3000 hola-ci-cd
🌍 Despliegue en producción

La aplicación está desplegada en Render:

👉 https://hola-ci-cd.onrender.com

🔄 Flujo del pipeline CI/CD
Push a GitHub
      ↓
GitHub Actions
      ↓
Ejecución de tests
      ↓
Build de Docker image
      ↓
Push a Docker Hub
      ↓
Deploy automático en Render
