# PádelFuerza

App de entrenamiento de fuerza para jugadores de pádel. Programa periodizado de 26 semanas, dos perfiles con login, registro de peso y reps por serie, timer de descanso, gráficos de progreso y editor completo del plan.

**App en vivo:** https://facugramaglia.github.io/padelfuerza/

---

## Instalar en el iPhone

Abrí la URL **en Safari** (no Chrome) → botón Compartir → **Agregar a inicio**. Queda como una app a pantalla completa y funciona sin señal.

## Acceso

| Usuario | Contraseña |
|---|---|
| `facu` | `facu1234` |
| `cami` | `cami1234` |

Cambialos desde **Ajustes → Mi cuenta**.

**El login no es seguridad real.** Sin servidor, las credenciales viven en el navegador y cualquiera con conocimientos técnicos las saltea. Sirve para separar perfiles en un teléfono compartido y nada más.

---

## Dónde viven los datos

En el `localStorage` del navegador de cada dispositivo. Consecuencias:

- Cada teléfono tiene su propio registro.
- Si borrás datos de sitio en Safari o cambiás de teléfono, **se pierde todo**.
- La app avisa cada 4 sesiones para que exportes. Hacelo.

**Exportar:** Ajustes → Respaldo → Exportar. Guardá el `.json` en Archivos.
**Importar:** reemplaza los datos de los dos perfiles. Pide confirmación.

---

## El programa

26 semanas, 2 sesiones de gimnasio por semana, en 4 bloques.

| Bloque | Semanas | Foco | Series × reps | Descarga |
|---|---|---|---|---|
| 1 · Adaptación anatómica | 1–4 | Reconectar sin castigar la pista | 2 × 12-15, RIR 3-4 | — |
| 2 · Base de hipertrofia | 5–12 | Construir masa | 3-4 × 8-12, RIR 2 | sem 12 |
| 3 · Intensificación | 13–20 | Más tensión mecánica, variantes nuevas | 4 × 6-8 en básicos | sem 20 |
| 4 · Fuerza aplicada | 21–26 | Convertir masa en fuerza en pista | 4 × 4-6 + explosivo | sem 26 |

En la semana de descarga la app reduce automáticamente las series a la mitad. Mismo peso.

Al terminar la semana 26: **Ajustes → Reiniciar ciclo**. Volvés al bloque 2 con todas las cargas más altas que la primera vuelta.

### Doble progresión

Empezás en el extremo bajo del rango de reps. Cuando completás el extremo alto en **todas** las series, subís el peso y volvés al piso del rango. La app marca el ejercicio en verde cuando toca.

### Reglas fijas

- Cero cardio extra. Con 5 sesiones de pista semanales ya está cubierto.
- Nunca al fallo absoluto.
- Descanso completo entre series. Es parte del entrenamiento, no tiempo perdido.
- No hagas piernas pesado el día antes de un partido que te importe.
- Dolor articular, no muscular: parás ese ejercicio.

---

## Editar el plan

**Ajustes → Días de entrenamiento.** Podés crear días nuevos, renombrarlos, asignarlos a cualquier bloque, y agregar, editar, reordenar o eliminar ejercicios con sus series, rangos de reps, descanso y notas.

Los cambios afectan solo al perfil con el que iniciaste sesión.

## Si actualizás la app

Al subir un `index.html` nuevo, cambiá también `const CACHE` en `sw.js` (`v4` → `v5`). Si no, el service worker sigue sirviendo la versión vieja.

## Stack

HTML, CSS y JavaScript en un solo archivo. Cero dependencias, cero build, cero backend. View Transitions API, scroll-driven animations, `:has()`, `color-scheme` nativo y service worker para uso sin conexión.

---

## Aviso

Esto es un plan general, no una prescripción individualizada. No reemplaza la evaluación de un profesional. Si tenés una lesión previa, dolor persistente o alguna condición médica, consultá antes de empezar.
