# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

## Deployment (Vercel)

### Variables de Entorno

Este proyecto usa Vite, que **reemplaza las variables de entorno en tiempo de build**, no en tiempo de ejecución.

Para configurar la API URL en producción:

1. Ve al [Dashboard de Vercel](https://vercel.com/dashboard)
2. Selecciona tu proyecto
3. Ve a **Settings** → **Environment Variables**
4. Añade:
   - **Name**: `VITE_API_URL`
   - **Value**: `https://conpedales.46.224.216.234.nip.io`
   - **Environment**: Production (y Preview si quieres)
5. **IMPORTANTE**: Haz un **Redeploy** del proyecto:
   - Ve a la pestaña **Deployments**
   - En el último deploy, click en los tres puntos → **Redeploy**

⚠️ **Nota crítica**: Si cambias la variable después del deploy, debes hacer redeploy para que Vite la incorpore en el build.

### Desarrollo local

```bash
# Copia el archivo de ejemplo
cp .env.example .env

# Edita .env con tus valores
VITE_API_URL=http://localhost:8081

# Inicia el servidor de desarrollo
npm run dev
```
