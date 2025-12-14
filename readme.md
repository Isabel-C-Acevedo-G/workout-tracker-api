# Workout Tracker API

Pequeña API REST para gestionar usuarios, entrenamientos y ejercicios (placeholder).

## Requisitos
- Node.js >= 18
- npm o yarn

## Instalación
1. Clonar el repositorio.
2. Instalar dependencias:
   - npm: `npm install`
   - yarn: `yarn`

3. Crear archivo `.env` en la raíz (ya incluido en el proyecto). Valores recomendados:
```
PORT=3000
NODE_ENV=development
DATABASE_URL=mongodb://localhost:27017/workout-tracker
JWT_SECRET=change_this_to_a_strong_secret
LOG_LEVEL=info
```

## Ejecutar
- Desarrollo:
  - npm: `npm run dev` (si tienes script con nodemon)
  - o: `node --experimental-specifier-resolution=node src/index.js`
- Producción:
  - `NODE_ENV=production node src/index.js`

La app escucha en el puerto definido en `PORT` (por defecto 3000).

## Rutas principales (ejemplos)
- GET /users — listar usuarios
- GET /users/:id — obtener usuario por id
- POST /users — crear usuario (JSON body: { "name": "...", "email": "..." })
- GET /users/add?name=Nombre&email=email@ejemplo.com — crear usuario desde query (helper)
- PUT /users/:id — reemplazar usuario
- PATCH /users/:id — actualizar parcialmente
- DELETE /users/:id — eliminar usuario

Rutas opcionales (si existen los archivos):
- /workouts
- /exercises

## Ejemplos curl
- Listar usuarios:
  `curl http://localhost:3000/users`
- Crear usuario:
  `curl -X POST -H "Content-Type: application/json" -d '{"name":"Ana","email":"ana@example.com"}' http://localhost:3000/users`

## Notas
- Actualmente los datos de usuarios son en memoria (array). Persistencia pendiente.
- Añadir linters (eslint), formateo (prettier) y tests es recomendable.

```// filepath: c:\Users\EQUIPO\OneDrive\Desktop\workout-tracker-api\readme.md
# Workout Tracker API

Pequeña API REST para gestionar usuarios, entrenamientos y ejercicios (placeholder).

## Requisitos
- Node.js >= 18
- npm o yarn

## Instalación
1. Clonar el repositorio.
2. Instalar dependencias:
   - npm: `npm install`
   - yarn: `yarn`

3. Crear archivo `.env` en la raíz (ya incluido en el proyecto). Valores recomendados:
```
PORT=3000
NODE_ENV=development
DATABASE_URL=mongodb://localhost:27017/workout-tracker
JWT_SECRET=change_this_to_a_strong_secret
LOG_LEVEL=info
```

## Ejecutar
- Desarrollo:
  - npm: `npm run dev` (si tienes script con nodemon)
  - o: `node --experimental-specifier-resolution=node src/index.js`
- Producción:
  - `NODE_ENV=production node src/index.js`

La app escucha en el puerto definido en `PORT` (por defecto 3000).

## Rutas principales (ejemplos)
- GET /users — listar usuarios
- GET /users/:id — obtener usuario por id
- POST /users — crear usuario (JSON body: { "name": "...", "email": "..." })
- GET /users/add?name=Nombre&email=email@ejemplo.com — crear usuario desde query (helper)
- PUT /users/:id — reemplazar usuario
- PATCH /users/:id — actualizar parcialmente
- DELETE /users/:id — eliminar usuario

Rutas opcionales (si existen los archivos):
- /workouts
- /exercises

## Ejemplos curl
- Listar usuarios:
  `curl http://localhost:3000/users`
- Crear usuario:
  `curl -X POST -H "Content-Type: application/json" -d '{"name":"Ana","email":"ana@example.com"}' http://localhost:3000/users`

## Notas
- Actualmente los datos de usuarios son en memoria (array). Persistencia pendiente.
- Añadir linters (eslint), formateo (prettier) y tests es recomendable.
