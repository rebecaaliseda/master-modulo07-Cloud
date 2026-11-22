# Laboratorio correspondiente al Módulo 7 - Cloud del Máster Front End XVII.

Aplicación desarrollada con React y Vite que muestra una página informativa utilizada como ejemplo para realizar los despliegues solicitados en el laboratorio.

# Ejercicio obligatorio

## 1. Despliegue manual en GitHub Pages

Se configuró GitHub Pages para publicar la aplicación generada por Vite.

Para ello se realizaron los siguientes pasos:

- Instalación de `gh-pages`.
- Configuración de la propiedad `base` en `vite.config.ts`.
- Generación de la carpeta `dist`.
- Publicación manual: https://rebecaaliseda.github.io/master-modulo07-Cloud/

## 2. Automatización con GitHub Actions

Se creó un workflow de GitHub Actions para automatizar el proceso de construcción y despliegue.
Archivo creado: .github/workflows/deploy.yml. Encargado de automatizar el despliegue en GitHub Pages.

Cada vez que se realiza un push sobre la rama principal se ejecuta:

npm install
npm run build

y posteriormente se actualiza GitHub Pages de forma automática.

# Ejercicios opcionales

## 1. Despliegue manual en Render

Se realizó un despliegue manual mediante Render usando un Static Site.

- Configuración utilizada: npm install && npm run build
- Publish Directory: dist
- URL: https://master-modulo07-cloud.onrender.com

## 2. Despliegue en Render utilizando Docker

Se configuró la aplicación para ejecutarse dentro de un contenedor Docker.

Se creó el archivo Dockerfile. Define la imagen Docker utilizada para desplegar la aplicación. Responsable de:

- Instalar dependencias.
- Construir la aplicación.
- Servir el contenido generado.
- Exponer el puerto 3000.

Se creó el archivo .dockerignore para evitar copiar directorios innecesarios al contenedor.

Se creó un Web Service en Render utilizando el Dockerfile incluido en el repositorio.

### Construcción de imagen

docker build -t modulo07-cloud .

### Ejecución local

docker run -p 3000:3000 modulo07-cloud

# Resultado

Se ha conseguido:

- Despliegue manual en GitHub Pages.
- Automatización mediante GitHub Actions.
- Despliegue manual en Render.
- Dockerización de la aplicación.
- Despliegue de la imagen Docker en Render.
