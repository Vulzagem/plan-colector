---
target: "Plan Collector MLBB (https://vulzagem.github.io/plan-colector/)"
total_score: 28
max_score: 40
na_heuristics: 
p0_count: 1
p1_count: 1
timestamp: 2026-08-28T18-07-39Z
slug: vulzagem-github-io-plan-colector
---
## Design Health Score

| # | Heurística | Score | Hallazgo clave |
|---|---|---|---|
| 1 | Visibilidad del estado del sistema | 3/4 | Los switches de fuente de cristales recalculan sin micro-feedback de "listo" |
| 2 | Coincidencia con el mundo real | 4/4 | Vocabulario 100% jugador, sin traducción corporativa |
| 3 | Control y libertad | 3/4 | Reset con confirmación en dos pasos; no hay deshacer para "Ya lo hice" |
| 4 | Consistencia y estándares | 3/4 | Switches con aria-pressed; botones de día, no — dos patrones distintos |
| 5 | Prevención de errores | 3/4 | Selector de mes bloquea fechas pasadas; el modo manual no |
| 6 | Reconocimiento antes que recuerdo | 2/4 | Usuario sostiene 6+ cifras simultáneas sin resumen de una línea |
| 7 | Flexibilidad y eficiencia | 2/4 | Sin atajo "marcar hasta hoy" |
| 8 | Estética minimalista | 2/4 | 8+ módulos apilados sin jerarquía de prioridad |
| 9 | Recuperación de errores | 3/4 | Mensajes puntuales, tono correcto |
| 10 | Ayuda y documentación | 3/4 | Guía de instalación excelente; sin onboarding de la lógica central |
| **Total** | | **28/40** | **Good** |

## Veredicto de especificidad
Autorado específicamente para MLBB (aviso de precios variables por evento, recordatorio porque el tiro diario no se acumula, precios de Bonoxs fechados por país). Detector en modo degradado, 2 hallazgos de bajo impacto (transición de width sin jank observado; falso positivo de "marquee" sobre el splash, que ya respeta prefers-reduced-motion). Overlay de navegador no disponible (bloqueado por contenido mixto del sandbox de la herramienta, no un defecto del sitio).

## Problemas prioritarios

[P0] Espacio muerto ~700px en el carrusel semanal, encontrado independientemente por A (lectura de CSS: .weeks sin align-items) y B (medición en vivo: los 5 paneles miden 769.59px por igual). Fix: align-items:flex-start en .weeks. Comando: /impeccable layout

[P1] Sin estado de finalización, peak-end rule ausente — verificado en código, no hay string de celebración al llegar a 100%. Comando: /impeccable delight

[P2] El color no distingue información normal de decisión de plata real (mismo ámbar para ambos). Comando: /impeccable colorize

[P2] Botones de día sin aria-pressed, a diferencia de los switches. Comando: /impeccable harden

[P3] Recarga en pesos sin el ahorro logrado al lado. Comando: /impeccable clarify

## Persona red flags
Jordan: pills "atrasado" sin contexto al empezar a mitad de mes. Sam: progreso de día no auditable sin visión. Casey: el P0 lee como "se rompió la página".

## Minor observations
Foco de teclado visible en 7/7 paradas. Contraste: 16 pares medidos, todos >4.5:1 (mínimo 4.70:1). Fecha de precios de Bonoxs no visible en la UI. Desktop 1440px con ~400px vacíos a cada lado.

## Questions to consider
1. ¿"Hoy" merece más peso visual que las secciones de una sola vez?
2. ¿La tabla de combo más barato (ahorra ~$30 sobre $34.000) resuelve un problema real del usuario?
