# 📦 Curso: Despliegue de Aplicaciones con Docker  

## 🎓 Información del Curso  
- **Curso:** Despliegue de Aplicaciones con Docker  
- **Proyecto:** Práctica de Docker Compose  
- **Profesor:** Ing. Edison Naranjo (CEC-EPN)  
- **Fecha:** 19 de Septiembre de 2025  

---

## 📑 Proyecto – Análisis de Vulnerabilidades y Despliegue Automático con Docker Hub - Grupo 1 – Tarea 3  

### 📋 Descripción del Proyecto  
Este proyecto implementa una aplicación **FastAPI** en GitHub y un archivo **.yml** en GitHub Actions para:  

1. Realizar análisis de vulnerabilidades de la aplicación.  
2. Construir la imagen Docker.  
3. Publicar la imagen automáticamente en **Docker Hub**.  

---

## 👥 Integrantes - Grupo 1 (Municipio de Quito)  

| Integrante                           | Repositorio GitHub                                                         |
|--------------------------------------|----------------------------------------------------------------------------|
| Carpio Zaquinaula Byron Orlando      | https://github.com/bcarpio16/fastapi-app-scout.git                         |
| Villarroel Vera Milton Orlando       | https://github.com/movillarroel/fastapi-app-scout.git                      |
| Mena Segura Edison Fabián            | https://github.com/Bulls1168-C/fastapi-app-scout.git                       |
| Benavides Freire Alex Vicente        | https://github.com/abenavides86/fastapi-app-scout.git                      |
| Gallardo Nicolalde Marcelo Iván      | https://github.com/panivinux/fastapi-app-scout.git                         |

---

Archivo workflow YAML de GitHub Actions 🚀

name: Build and Analyze Docker Image

on:
  push:
    branches: [ "main" ]

env:
  IMAGE_NAME: panivinux/fastapi-app-scout
  SHA: ${{ github.sha }}

jobs:
  build-and-analyze:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Log in to Docker Hub
        uses: docker/login-action@v3
        with:
          username: ${{ secrets.DOCKERHUB_USERNAME }}
          password: ${{ secrets.DOCKERHUB_TOKEN }}

      - name: Set up Docker Buildx
        uses: docker/setup-buildx-action@v3

      - name: Build image and load to runner
        id: build
        uses: docker/build-push-action@v6
        with:
          context: .
          file: ./Dockerfile-single
          push: true
          load: true
          tags: ${{ env.IMAGE_NAME }}:sha-${{ env.SHA }}

      - name: Install Docker Scout
        run: |
          mkdir -p ~/.docker/cli-plugins
          curl -sSfL https://raw.githubusercontent.com/docker/scout-cli/main/install.sh | sh
          sudo cp ~/.docker/cli-plugins/docker-scout /usr/local/bin/
          docker-scout version


      # 6. Escanear la imagen con Docker Scout
      - name: Scan image with Docker Scout
        run: |
          echo "🔍 Ejecutando análisis de vulnerabilidades con Docker Scout..."
          docker scout cves ${{ env.IMAGE_NAME }}:sha-${{ github.sha }} --output json 2>&1 | tee scout-report.json
          echo "==== Resumen de vulnerabilidades detectadas ===="
          cat scout-report.json

      # 7. Subir reporte como artefacto en GitHub Actions
      - name: Upload Scout JSON report
        uses: actions/upload-artifact@v4
        with:
          name: docker-scout-report
          path: scout-report.json
          
### 📋 Carpio Zaquinaula Byron Orlando 

<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/bc1.jpg" width="600">
<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/bc2.jpg" width="600">

### 📋 Villarroel Vera Milton Orlando

<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/mv1.jpg" width="600">
<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/mv2.jpg" width="600">

### 📋 Mena Segura Edison Fabián 

<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/em1.jpg" width="600">
<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/em2.jpg" width="600">

### 📋 Benavides Freire Alex Vicente

<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/ab1.jpg" width="600">
<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/ab2.jpg" width="600">

### 📋 Gallardo Nicolalde Marcelo Iván     

<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/mg1.jpg" width="600">
<img src="https://github.com/panivinux/fastapi-app-scout/raw/main/img/mg2.jpg" width="600">


