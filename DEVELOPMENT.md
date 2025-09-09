# Desarrollo local

Pasos rápidos para contribuir y ver el sitio generado localmente.

Requisitos:
- Node.js (v16+ recomendado)
- Python 3 (opcional para servir)

Instalar dependencias:

```bash
npm install
```

Generar la documentación y el JSON:

```bash
npm start
# Esto ejecuta `idoc` y luego `node build/ast.mjs`, la salida queda en `dist/`
```

Servir `dist/` localmente:

Opción A (recomendado, usa `http-server`):

```bash
npm run serve
# abre http://localhost:8000
```

Opción B (Python):

```bash
cd dist
python3 -m http.server 8000
# abrir http://localhost:8000
```

Despliegue en GitHub Pages:

El workflow `.github/workflows/deploy.yml` ya está configurado para ejecutar el build y publicar `dist/` a la rama `gh-pages` al hacer push a `master` o `main`.

Notas:
- Si prefieres otro puerto, edita el script `serve` en `package.json`.
- Para servir con autoreload instala `live-server` o `nodemon`.
