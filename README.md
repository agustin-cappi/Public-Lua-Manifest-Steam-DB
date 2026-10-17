# Public Lua Manifest Steam DB

mirror publico de manifests `.lua` de Steam cosechados desde fuentes autoritativas.
cada archivo esta nombrado por appid (`manifest.lua/<appid>.lua`) y contiene
`setManifestid(depot, gid, size)` + `addappid(...)` para instalar el juego via
Steam con DLC/depots desbloqueados.

## uso

- buscar el appid del juego en https://steamdb.info o en la URL de la tienda:
  `https://store.steampowered.com/app/<APPID>/<nombre>/`
- descargar `manifest.lua/<APPID>.lua`
- colocarlo en `C:\Program Files (x86)\Steam\config\stplug-in\<APPID>.lua`

## estructura

```
manifest.lua/
  730.lua
  440.lua
  578080.lua
  ...
```

## actualizaciones

el repo se puebla automaticamente. los luas no se actualizan en caliente: cuando
un juego recibe un parche con nuevos depot GIDs, hay que volver a correr el
harvester contra ese appid para refrescarlo.
