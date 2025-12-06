# 🌐 H-Suite Portal

H-Suite Portal es la interfaz web principal del ecosistema **H-Suite**, una plataforma modular diseñada para soportar múltiples microservicios, ofreciendo escalabilidad, mantenibilidad y una experiencia de usuario moderna basada en **React + Vite**.

---

## 📦 Tecnologías principales

- ⚛️ React 18
- ⚡ Vite
- 🎨 CoreUI
- 🐳 Docker & Docker Compose
- 📦 Node.js (opcional para desarrollo sin Docker)

---

## 📁 Estructura principal del proyecto

H-Suite-portal/
 ├── public/
 ├── src/
 │   ├── assets/
 │   ├── components/
 │   ├── layout/
 │   ├── scss/
 │   ├── views/
 ├── docker-compose.dev.yml
 ├── Dockerfile.dev
 ├── package.json
 ├── vite.config.mjs
 └── README.md

---

# 🐳 Ejecución del proyecto con Docker

Este proyecto está configurado para ejecutarse únicamente con Docker, sin necesidad de instalar dependencias de Node.js.

---

## ▶️ 1. Construir y levantar el contenedor

```
docker compose -f docker-compose.dev.yml up --build
```

El portal quedará disponible en:

👉 http://localhost:5100

---

## ▶️ 2. Levantar en segundo plano (background)

```
docker compose -f docker-compose.dev.yml up -d
```

---

## ⏹️ 3. Detener el contenedor

```
docker compose -f docker-compose.dev.yml down
```

Para eliminar también volúmenes:

```
docker compose -f docker-compose.dev.yml down -v
```

---

## 📜 4. Ver logs del contenedor

```
docker logs H-Suite-portal -f
```

---

# 🛠️ Ejecución sin Docker (opcional)

Si prefieres ejecutar el proyecto localmente:

### 1. Instalar dependencias

```
npm install
```

### 2. Ejecutar en modo desarrollo

```
npm run dev
```

### 3. Construir para producción

```
npm run build
```

---

# ⚙️ Variables de entorno

Si requieres configurar variables de entorno, crea un archivo:

```
.env
```

Ejemplo:

```
VITE_API_URL=https://api.hsuite.com
```

---

# 🌳 Flujo de trabajo con Git

Ramas recomendadas:

- main → rama estable
- dev → rama de desarrollo
- feature/* → ramas por funcionalidad

```
git checkout -b feature/nuevo-modulo
```

---

# 🤝 Contribuir al proyecto

1. Crear una rama feature/*
2. Realizar cambios
3. Crear Pull Request hacia `dev`
4. Esperar revisión y merge

---

# 📄 Licencia

Este proyecto está bajo la licencia incluida en el archivo LICENSE.

---

# 👨‍💻 Autor

**Johan López**
Desarrollador Backend | Arquitectura de Software
📍 Cali, Colombia

---

# ⭐ ¿Te fue útil este proyecto?

¡No olvides dejar una estrella en el repositorio! ⭐