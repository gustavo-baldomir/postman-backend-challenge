## Challenge Backend API Testing
 
Este proyecto contiene una solución de automatización de pruebas sobre una API REST.
Se utilizaron herramientas modernas que permiten ejecutar los tests de forma local, automatizada.

## Tecnologías utilizadas

- Postman: Plataforma principal para el diseño y ejecución de las pruebas.
- Newman: CLI oficial de Postman para ejecutar colecciones de manera automatizada.
- Node.js + npm: Para la gestión de scripts y dependencias.

## Pre Requisitos

Antes de ejecutar las pruebas asegurate de tener instalado:

- Node.js (v14 o superior): https://nodejs.org
- npm (incluido con Node.js)

Importante: Clonar el repositorio no instala automáticamente las dependencias del proyecto. Es necesario ejecutar "npm install" una vez descargado el proyecto para instalar todo lo necesario (como Newman) desde el archivo package.json.

## Estructura del repositorio

postman-backend-challenge/
├── .env/                        # Entornos para Postman
│   └── env-UAT.postman_environment.json
│
├── collections/                # Colecciones de Postman separadas por funcionalidad
│   ├── login-api-wallet-v1.postman_collection.json
│   └── movimientos-api-wallet-v1.postman_collection.json
│
├── node_modules/               # Dependencias instaladas (auto generadas por npm)
│
├── package.json                # Script y configuración del proyecto
├── package-lock.json           # Lockfile automático de npm
├── README.md                   # Documentación del proyecto

## Scripts disponibles

Los siguientes scripts permiten ejecutar las pruebas automatizadas sobre la API de manera local desde la terminal.

- Intalar dependencias (solo se ejecuta una vez): npm install
- Ejecutar tests de login: npm run test:login
- Ejecutar tests de movimientos: npm run test:movimientos
- Ejecutar todas las colecciones juntas: npm run test:all

## Notas Finales 

El proyecto está preparado para escalar agregando nuevas colecciones o entornos en el futuro.