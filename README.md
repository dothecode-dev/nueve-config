# nueve-config

Configuración pública que lee la app Nueve al abrir. Se sirve por GitHub Pages en
`https://dothecode-dev.github.io/nueve-config/version.json`.

## version.json

- `minVersion` por plataforma: si la versión instalada es menor, la app pide actualizar antes de entrar a Inicio
  (nunca corta una partida en curso). Sin red o si este archivo no se puede leer, la app sigue normal.
- `storeUrl`: la ficha de la tienda que abre el botón "Actualizar". Tiene que empezar con `https://`.

## Antes de subir una minVersion

1. Publicar la versión nueva en la tienda de **esa** plataforma.
2. Esperar a que esté disponible para descargar (Apple revisa; puede tardar días).
3. Recién ahí subir `minVersion` de esa plataforma. Si se sube antes, esos usuarios quedan bloqueados sin nada que bajar.

`ios` se agrega cuando exista la ficha en App Store Connect (su `storeUrl` lleva el id de la app).
