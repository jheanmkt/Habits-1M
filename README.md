# Ritmo

Mini app de hábitos con recordatorios, temporizador, checklist y análisis. Estilo liquid glass, modo claro y oscuro. Inicio de sesión y sincronización con Supabase. Es un sitio estático: no necesita build.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa |
| `config.js` | URL y clave pública de tu proyecto de Supabase |
| `supabase/schema.sql` | Tabla y reglas de seguridad (RLS) |
| `manifest.webmanifest`, `icon*` | Para instalarla en el celular como app |
| `vercel.json` | Configuración del hosting |

## Puesta en marcha

1. **Supabase** → SQL Editor → pega y ejecuta `supabase/schema.sql`.
2. **Supabase** → Project Settings → API → copia *Project URL* y la clave *anon / publishable* en `config.js`.
3. **GitHub** → sube esta carpeta a un repositorio.
4. **Vercel** → Add New → Project → importa el repositorio → Framework: *Other* → Deploy.
5. **Supabase** → Authentication → URL Configuration → *Site URL* = tu dominio de Vercel, y agrégalo también en *Redirect URLs* (`https://tu-app.vercel.app/**`).

## Probar en tu computadora

```bash
npx serve .
```
Abre http://localhost:3000 y agrega `http://localhost:3000/**` en *Redirect URLs* de Supabase.
Si `config.js` no está completo, la app funciona en modo local (sin cuenta).
