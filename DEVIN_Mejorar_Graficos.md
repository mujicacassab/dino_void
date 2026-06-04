# DINO VOID — Brief para Devin: mejorar los gráficos

El juego ya está completo y funcionando en `index.html`. La tarea para Devin es **subir el nivel visual** sin romper la jugabilidad ni la estructura, y dejándolo listo para una **presentación/demo de 60 segundos**.

---

## 1. Prompt maestro (pega esto en Devin)

> **Rol:** Actúa como un Desarrollador de Videojuegos Senior y Tecnólogo Creativo especializado en gráficos de canvas.
>
> **Tarea:** Toma el archivo `index.html` de este repo (un juego completo y funcional) y **mejora únicamente la calidad visual**. No cambies la mecánica, los estados, los controles ni la duración del recorrido. Mantén todo en un solo archivo `index.html`, HTML + CSS + JavaScript vanilla con `<canvas>`, **sin dependencias externas, sin CDNs, sin build**, que abra con doble clic en Chrome y funcione offline.
>
> **Qué hace el juego (no lo alteres):** Fase 1 corredor 2D en blanco y negro (saltar) → al llegar a 300 puntos cae un meteorito, se congela, hay glitch y un escudo de datos verde (Platzi + Devin.ai) lo desintegra → Fase 2 retrowave 3D en perspectiva (cambiar de carril para esquivar "bugs") → si chocas en Fase 2 el personaje **evoluciona a ángel** (le brotan alas + halo) y asciende → pantalla de cierre «SOBREVIVE A LA EXTINCIÓN CON LA EDUCACIÓN Y LA IA» con los logos a los lados y el ángel volando en medio. Ganar = cruzar el portal (Evolución Completa).
>
> **Mejoras gráficas a implementar** (mantén 60fps): ver lista de abajo. Después de cada cambio, abre el juego y verifica que sigue corriendo fluido y que el recorrido completo sigue cabiendo en ~60s. Al terminar, recorre el checklist de aceptación y corrige lo que falle antes de entregar.

---

## 2. Mejoras gráficas sugeridas (en orden de impacto)

1. **Bloom / glow real:** renderiza los elementos neón en un canvas fuera de pantalla, aplícale desenfoque y compón con `globalCompositeOperation='lighter'` sobre el principal, en lugar de solo `shadowBlur`. Da el brillo retrowave de verdad.
2. **Sprite del dino mejorado:** más detalle y mejor animación de carrera (más cuadros), y una versión "tech" de la Fase 2 con acentos de circuito y estela.
3. **Ángel pulido:** alas con plumas en capas y aleteo suave, halo con destellos, haz de luz de ascensión y partículas tipo chispa/pluma cayendo. Que se lea claramente como evolución angelical.
4. **Retrowave más rico:** degradado de cielo con malla/auroras, sol con bandas animadas, rejilla con perspectiva y brillo por distancia, niebla en el horizonte, estrellas con parpadeo variado.
5. **Transición (momento WOW):** aberración cromática (separación RGB) y scanlines durante el glitch; meteorito con estela de partículas y calor; escudo de datos con lluvia de código tipo Matrix y un hexágono de energía animado; flash de ruptura con ondas.
6. **Post-proceso sutil:** viñeta, grano/CRT muy leve, y un toque de motion blur en Fase 2 para sensación de velocidad.
7. **Tipografía y HUD:** jerarquía más cuidada, barras de progreso con brillo, microanimaciones al cambiar de carril.
8. **Partículas reutilizables:** un sistema de partículas único (chispas, plumas, escombros, polvo de estrellas) para impacto, ascensión y victoria.

---

## 3. Restricciones que NO se deben romper

- Un solo `index.html`, vanilla + canvas, **sin librerías ni CDNs**, abre offline con doble clic.
- **No usar `localStorage`** (falla en `file://`).
- Soporte de **teclado y táctil/click** intacto.
- **Marca y lemas siempre visibles:** insignias Platzi (verde) + Devin.ai (chip neón) y los lemas, presentes en todas las fases y pantallas.
- Mantener la **pantalla de cierre** con el ángel volando entre los dos logos.
- **Duración del recorrido completo ~60s** (no alargar): Fase 1 ≈ 20s, transición ≈ 6s, Fase 2 ≈ 20s.
- Resolución lógica fija escalada a la ventana; mantener proporción.

---

## 4. Checklist de aceptación (Devin debe pasar todo)

- [ ] Abre con doble clic en Chrome, sin errores de consola, sin red.
- [ ] Corre fluido (≈60fps) en las tres fases tras las mejoras.
- [ ] El recorrido completo (inicio → ganar) sigue durando ~60s o menos.
- [ ] Fase 1 en blanco y negro; salto y colisión correctos.
- [ ] Transición completa: meteorito → glitch → escudo de datos (Platzi/Devin.ai) → ruptura → 3D.
- [ ] Fase 2 retrowave con cambio de carril fluido y "bugs" como obstáculos.
- [ ] Choque en Fase 2: impacto + **evolución a ángel** (alas, halo, ascensión).
- [ ] Pantalla de cierre con lema, logos a los lados y ángel volando en medio.
- [ ] Victoria (Evolución Completa) y reinicio (R/Espacio/Click) funcionan.
- [ ] Marca y lemas visibles en todas las pantallas. Sin `localStorage` ni dependencias externas.

---

## 5. Cómo correrlo en Devin

1. Sube `index.html`, `README.md` y este `DEVIN_Mejorar_Graficos.md` a tu repo de GitHub (p. ej. `dino-void`).
2. En Devin: modo Agente → selecciona el repo → agente Devin.
3. Pega el **Prompt maestro** (sección 1) y @menciona este archivo como contexto.
4. Aprueba el plan, deja que trabaje y revisa el PR contra el checklist.
5. Si algo falla, comenta en el PR citando el ítem del checklist (p. ej. "no mantiene 60fps en Fase 2").
