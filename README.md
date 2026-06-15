# Kabilio — Estrategia de marketing 3 años

Dashboard interactivo de la estrategia de marketing de Kabilio. Vive como sitio estático: un único archivo HTML autocontenido sin build step ni dependencias.

## Estructura

- `index.html` — Dashboard completo (HTML, CSS y JS inline).
- `vercel.json` — Configuración mínima de despliegue en Vercel.

## Despliegue local

Cualquier servidor estático funciona. Por ejemplo:

```bash
python3 -m http.server 8000
```

Y abre `http://localhost:8000`.

## Despliegue en Vercel

El proyecto está configurado para auto-deploy en cada push a `main`.

1. Conectar el repo a Vercel.
2. Vercel detecta el `index.html` y publica como sitio estático.
3. No requiere comando de build ni instalación de dependencias.

## Persistencia local

Las tareas del kanban de la sección **Status del plan** y el estado del menú lateral (comprimido/expandido) se guardan en `localStorage` del navegador. Cada visitante ve su propio estado independiente.

## Edición

Para cambios pequeños se edita directamente `index.html`. Por la naturaleza del archivo único, basta con commit y push para desplegar.
