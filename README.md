# Mótu — documentos legales

Términos de servicio y política de privacidad de la app Mótu, publicados con
GitHub Pages. La fuente canónica vive en el repo de la app
(`docs/legal/`); este repo existe solo para servir las páginas.

## La cartera de Mótu

El **estado** de las líneas de trabajo de Mótu vive en un tablero local, la
**cartera**, en `http://127.0.0.1:8096`. Se abre con doble clic en
`~/Documents/GitHub/motu-tablero/Cartera.command`.

Reglas de ese tablero, resumidas:

- **Nada se cierra sin evidencia y sin una nota en cristiano**, y la evidencia se
  comprueba de verdad: que la propuesta exista, que se integrara y que sus checks
  salieran verdes.
- **Manda siempre `X-Autor`.** Sin firma se rechaza; lo que escribe una IA nace
  sin revisar.
- **La fase se calcula, no se mueve a mano.**

Al terminar una sesión, deja las tres líneas de la bitácora:

```bash
curl -s -X POST http://127.0.0.1:8096/api/proyecto/CODIGO/bitacora \
  -H "Content-Type: application/json" -H "X-Autor: claude" \
  -d '{"hice":"...","me_quede_en":"...","lo_siguiente":"..."}'
```

Si `http://127.0.0.1:8096/api/salud` no contesta, el tablero está apagado: ábrelo
con su lanzador. Si dice `"conectado": false`, no hay conexión y no se puede
escribir — dilo, y no lo intentes de otra forma.

En la cartera, este repositorio es el proyecto **`LEG`** (legal y términos), y su
alias para la evidencia es `legal`.
