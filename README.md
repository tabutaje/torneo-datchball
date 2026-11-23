# Torneo de datchball · 4º, 5º y 6º de Primaria

Web del torneo de datchball de Educación Física. Cada curso gestiona su liga desde su propio enlace.

**Web:** https://tabutaje.github.io/torneo-datchball/

## Enlaces directos

| Sección | Enlace |
| --- | --- |
| Liga de 4º | `#/liga/4` |
| Liga de 5º | `#/liga/5` |
| Liga de 6º | `#/liga/6` |
| Dentro de cada liga | `/partidos`, `/clasificacion`, `/jugadores`, `/puntos`, `/juego-limpio`, `/autoevaluacion`, `/equipos` |
| Reglas, cronómetro, valores, zona profe | `#/reglas`, `#/crono`, `#/valores`, `#/profe` |

Ejemplo: `https://tabutaje.github.io/torneo-datchball/#/liga/5/clasificacion`

## Qué hace

- **Ligas por curso** con resumen, partidos al mejor de 3 partidas, clasificación con podio y gran final.
- **Modo edición** para apuntar resultados, juego limpio y estadísticas de cada jugador (aires, eliminaciones y tarjetas verdes).
- **Puntos** para cada jugador (aire, juego limpio, compañerismo, esfuerzo…), tocando su ficha.
- **Autoevaluación** interactiva: cada equipo se puntúa después de cada partido y el profe ve las respuestas en modo edición.
- **Mejores jugadores** y **ranking de juego limpio** calculados automáticamente.
- **Equipos** con nombre, mascota y jugadores, y reparto al azar de la clase.
- **Reglas** del reglamento oficial de datchball 2024, **cronómetro** con partidas de 10 minutos y aviso de acorte a los 5 y página de **valores**.

## Datos

Los datos se sincronizan con **Firebase (Firestore)**: todos los dispositivos ven lo mismo. Cualquiera puede consultar las ligas y enviar su autoevaluación; solo la cuenta de Google del profe puede editar y ver las autoevaluaciones.

- Las reglas de seguridad están en [`firestore.rules`](firestore.rules). Hay que pegarlas en Firebase → Firestore Database → Reglas, cambiando el correo del profe.
- La configuración de Firebase que aparece en `index.html` es pública por diseño; la seguridad la ponen esas reglas.
- Si no hay conexión, la web muestra los últimos datos guardados en el dispositivo.

Es un único archivo `index.html`, sin instalación. Cada cambio subido a `main` se publica solo con GitHub Pages.

Fuente de las reglas: [Reglamento oficial de datchball 2024](http://wasg.info/mundialito/Reglamento_Datchball.pdf) · [datchball.com](https://www.datchball.com)
