# Challenge Backend API Testing
 
Este proyecto contiene una solución de automatización de pruebas sobre una API REST.
Se utilizaron herramientas modernas que permiten ejecutar los tests de forma local, automatizada.

# Tecnologías utilizadas

- Postman: Plataforma principal para el diseño y ejecución de las pruebas.
- Newman: CLI oficial de Postman para ejecutar colecciones de manera automatizada.
- Node.js + npm: Para la gestión de scripts y dependencias.
- newman-reporter-htmlextra: Para generar reportes visuales detallados de la ejecución de pruebas.

# Pre Requisitos

Antes de ejecutar las pruebas asegurate de tener instalado:

- Node.js (v14 o superior): https://nodejs.org
- npm (incluido con Node.js)

Importante: Clonar el repositorio no instala automáticamente las dependencias del proyecto. Es necesario ejecutar "npm install" una vez descargado el proyecto para instalar todo lo necesario (como Newman) desde el archivo package.json.

# Estructura del repositorio

- postman-backend-challenge/
 -.env/                                             # Entornos para Postman
    -env-UAT.postman_environment.json

 -collections/                                      # Colecciones de Postman separadas por funcionalidad 
    -login-api-wallet-v1.postman_collection.json
    -movimientos-api-wallet-v1.postman_collection.json

 -reports/                                          # Reportes HTML generados automáticamente
    -.gitkeep

 -node_modules/                                     # Dependencias instaladas (auto generadas por npm)

 -package.json                                      # Script y configuración del proyecto  
 -package-lock.json                                 # Lockfile automático de npm
 -README.md                                         # Documentación del proyecto

# Scripts disponibles

Los siguientes scripts permiten ejecutar las pruebas automatizadas sobre la API de manera local desde la terminal.

- Intalar dependencias (solo se ejecuta una vez): npm install
- Ejecutar tests de login: npm run test:login
- Ejecutar tests de movimientos: npm run test:movimientos
- Ejecutar todas las colecciones juntas: npm run test:all

# Generación de reportes

Este proyecto genera reportes en formato HTML detallado, usando el paquete newman-reporter-htmlextra. Los reportes incluyen resultados de ejecución, información de requests y validaciones.

Los archivos HTML se guardan en la carpeta reports/, ubicada en la raíz del proyecto. Esta carpeta ya está incluida en el repositorio y configurada para ignorar los archivos .html generados automáticamente, con el objetivo de que dichos reportes no se suban al repositorio remoto.

Los mismos pueden encontrarse en la carpeta reports/ dentro del directorio local donde se haya clonado el repositorio (por ejemplo, en el escritorio). 

# Comandos para ejecutar test y generar reportes

- npm run test:login:report         # Ejecuta tests de login y genera login-report.html
- npm run test:movimientos:report   # Ejecuta tests de movimientos y genera movimientos-report.html
- npm run test:all:report           # Ejecuta ambas colecciones y genera ambos reportes

# Comparativa rápida de comandos disponibles

Comando                                Acción

npm run test:login --->                Ejecuta los tests de login sin generar reporte HTML

npm run test:login:report --->         Ejecuta los tests de login y genera reporte HTML

npm run test:movimientos --->          Ejecuta los tests de movimientos sin generar reporte

npm run test:movimientos:report --->   Ejecuta los tests de movimientos y genera reporte HTML

npm run test:all --->                  Ejecuta todas las colecciones sin generar reporte

npm run test:all:report --->           Ejecuta todas las colecciones y genera todos los reportes

# Notas Finales 

El proyecto está preparado para escalar agregando nuevas colecciones o entornos en el futuro.