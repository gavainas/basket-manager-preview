# Basket Manager — preview de prueba

**Esto no es el juego.** El juego vive en
[gavainas/basket-manager](https://github.com/gavainas/basket-manager) y se juega en
<https://gavainas.github.io/basket-manager/>.

Este repositorio es un **banco de pruebas**: contiene solo el resultado compilado de una
rama que está en evaluación, para poder jugarla desde cualquier lado antes de decidir si
entra al juego.

- **Se juega en:** <https://gavainas.github.io/basket-manager-preview/>
- **Rama en prueba ahora:** `preview/identidad-club` — fundá tu club (nombre, barrio,
  colores, escudo, camiseta y cancha) y jugá con su identidad.
  Documentación: [design/IDENTIDAD_CLUB.md](https://github.com/gavainas/basket-manager/blob/preview/identidad-club/design/IDENTIDAD_CLUB.md)

## Los guardados están separados

`gavainas.github.io` es el mismo origen para el juego y para esta preview, y el navegador
comparte `localStorage` entre carpetas del mismo origen. Para que jugar acá no pise la
partida de verdad, la preview se compila con su propia clave de guardado
(`VITE_SAVE_KEY`, ver `.env.preview` en la rama). Son dos partidas distintas que no se
tocan.

## Actualizar la preview

Desde el repo del juego, en la rama que se quiera probar:

```bash
npx vite build --mode preview --base=/basket-manager-preview/
```

y copiar el contenido de `dist/` a la raíz de este repositorio, commit y push. GitHub
Pages republica solo. La URL no cambia, así que la partida de prueba guardada sigue ahí.

## Retirar la preview

Borrar este repositorio (Settings → Danger Zone), o desactivar Pages en Settings → Pages.
Nada de esto afecta al juego publicado.
