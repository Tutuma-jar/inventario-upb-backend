# Inventario UPB — Backend

API Express para gestionar productos.

## Desarrollo local

1. Define `DATABASE_URL` y `DB_SSL=false` en un archivo `.env`.
2. Inicializa la tabla:

   ```bash
   npm run db:init
   ```

3. Inicia la API:

   ```bash
   npm start
   ```

La API queda disponible en `http://localhost:3000/api/productos`.

## Despliegue

`render.yaml` define el Web Service y la base PostgreSQL administrada. Al iniciar, Render
ejecuta `npm run db:init` antes de levantar la API; GitHub Actions requiere el secreto
`RENDER_DEPLOY_HOOK` con el deploy hook del servicio.
