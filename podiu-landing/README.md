# Podiu — Landing mínima

Landing estática de una sola pantalla, minimalista, con degradado cálido.

## Estructura
- `index.html`: markup principal.
- `styles.css`: estilos del layout y el fondo tipo atardecer.
- `App.svelte` (opcional, no usado): remanente si luego migras a SvelteKit.

## Vista local
Abre `index.html` en el navegador.

## Deploy en Cloudflare Pages (vía GitHub)
1. Crea un repo en GitHub y sube este proyecto.
2. En Cloudflare Pages:
   - Create Project → Conecta con GitHub → selecciona el repo.
   - Framework preset: None
   - Build command: (vacío)
   - Output directory: `.`
3. Deploy.

## Notas
- Si más adelante migras a SvelteKit, este repo ya incluye `.gitignore` preparado.
- Se recomienda mantener el root simple para que Cloudflare sirva archivos estáticos sin build.
