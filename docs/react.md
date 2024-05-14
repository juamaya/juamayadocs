# <mark> Publicar Aplicaciones de ReactJS en github-pages </mark> 
![vite](img/vite.jpg)

[Vite](https://vitejs.dev/)



---

##  INSTALAR LIBRERIA

- Aqui instalamos la libreria gh-pages

Abrir la consola <mark>cmd</mark> situada en la carpeta del proyecto escribimos el comando:

```
  npm i gh-pages -D
```

---

##  CREAR REPOSITORIO EN TU CUENTA DE GITHUB.com

Nombre REPO:<mark> web</mark>

---

##   CONFIGURAR ARCHIVOS

Paso 1 -  AÑADIR EN EL ARCHIVO: <mark> vite.config.js</mark>

```
 base:"/web/"
```

vite.config.js

```js
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  base: "/web/",
});
```

---

Paso 2 - AÑADIR EL SCRIPT AL ARCHIVO: <mark> package.json</mark>

```
"deploy": "gh-pages -d dist"
```

package.json

```json
{
  "name": "app-componentes",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview",
    "deploy": "gh-pages -d dist"
  },
  "dependencies": {
    "gh-pages": "^5.0.0",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-router-dom": "^6.9.0"
  },
  "devDependencies": {
    "@types/react": "^18.0.27",
    "@types/react-dom": "^18.0.10",
    "@vitejs/plugin-react": "^3.1.0",
    "vite": "^4.1.0"
  }
}
```

---

##  SUBIR PROYECTO AL REPOSITORIO.

En la consola situada en la carpeta del proyecto escribimos el comando:

```
  git init

  git add .

  git status

  git commit -m "mi primer commit"

  npm run build

  git remote add origin https://github.com/juamaya/web.git

  git branch -M main

  git push -u origin main
```

---

##  SUBIR CAMBIOS AL REPOSITORIO.

En la consola situada en la carpeta del proyecto escribimos el comando:

```

  git add .

  git commit -m "cambios realizados."

  npm run build

  git push


```

---
![docusaurus](img/gh-pages.jpg)
##  PUBLICAR PROYECTO EN GITHUB-PAGES.

En la consola situada en la carpeta del proyecto escribimos el comando:

```
  npm run deploy
```

---

##  CLONAR EL REPOSITORIO. (web)

### Crear una carpeta.

   - Abrir la consola <mark>cmd</mark> situada en la carpeta escribimos el comando:
   - Escribir el comando:

```sh
   git clone https://github.com/juamaya/web.git
```

### Abrir el editor de codigo vsCode.

   - Abrir la consola <mark>cmd</mark> situada en la carpeta   escribimos el comando:
   - Escribir el comando:

```sh
   code .
```

### Instalar la carpeta **node_modules.**

   - Abrir la terminal en vsCode.
   - Escribir el comando:

```sh
   npm i
```

### Correr la app.

   - Abrir la terminal en vsCode.
   - Escribir el comando:

```
   npm run dev

```

---



# <mark> JUAMAYA 🍺 2024</mark>
