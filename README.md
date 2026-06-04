# DINO VOID — Evolución

**Lema:** *Sobrevive a la extinción · evoluciona · IAprende.*

Un dinosaurio rompe su propia dimensión. En vez de extinguirse por un meteorito, es salvado por la **educación y la IA** (Platzi + Devin.ai) y **evoluciona** a un mundo retrowave 3D.

## Cómo jugar
Abre `index.html` con doble clic en Chrome. No requiere instalación, internet ni dependencias.

| Acción | Tecla / gesto |
|---|---|
| Iniciar / Reiniciar | ESPACIO · ENTER · R · CLICK |
| Saltar (Fase 1) | ESPACIO · ↑ · CLICK |
| Carril izquierda (Fase 2) | ← · click mitad izquierda |
| Carril derecha (Fase 2) | → · click mitad derecha |

## Flujo
1. **Fase 1 · El Pasado (2D, blanco y negro):** corres de izquierda a derecha y saltas obstáculos.
2. **Momento WOW:** al llegar a 300 puntos cae un meteorito → el juego se congela → glitch de código corrupto → aparece un escudo de datos verde (PLATZI / DEVIN.AI) que desintegra el meteorito → la dimensión se rompe.
3. **Fase 2 · La Evolución (3D retrowave):** la cámara se ubica tras el dino tecnológico; avanzas hacia el fondo y cambias de carril para esquivar los "bugs".
4. **Cierre:** ganas al cruzar el portal (**Evolución Completa**). Si chocas en la Fase 2, sientes el impacto y al dino **le brotan alas y asciende convertido en ángel** (evolución), seguido de una pantalla de cierre: «SOBREVIVE A LA EXTINCIÓN CON LA EDUCACIÓN Y LA IA», con los logos de Platzi y Devin.ai a los lados y el **ángel volando en medio**. En la Fase 1, chocar lleva a **Game Over**.

## Técnico
- Un solo archivo `index.html` (HTML + CSS + JavaScript vanilla, `<canvas>`).
- Sin frameworks, sin CDNs, sin build. Funciona offline.
- El 3D es pseudo-3D por proyección de perspectiva manual.

## Ajustes rápidos (en el bloque de parámetros del `<script>`)
- `SCORE_TRANS` — puntos para disparar la transición (default 300).
- `SCORE_WIN` — puntos para ganar (default 600).
# dino_void
