# Vendor-библиотеки

## three/ — Three.js r128 (npm three@0.128.0)

- `three.min.js` — UMD-сборка, подключается обычным `<script src=...>`;
- `three.module.js` — ES-модуль той же версии;
- `OrbitControls.js` — управление камерой (UMD, examples/js);
- `LICENSE` — лицензия MIT.

r128 — последняя версия с UMD-сборкой на cdnjs, поэтому локальная копия
и CDN взаимозаменяемы. WebGL-рендеринг проверен в среде Claude Code
(Chromium + SwiftShader).

## gsap/ — GSAP 3.15.0 (официальный публичный пакет)

Все минифицированные UMD-сборки, подключаются обычным `<script src=...>`.
Включая ранее платные плагины (GSAP полностью бесплатен с 2024 г.):
ScrollTrigger, ScrollSmoother, DrawSVG, SplitText, MorphSVG, MotionPath,
Flip, Draggable, CustomEase и др.

Лицензия: GSAP Standard License (https://gsap.com/standard-license) —
бесплатное коммерческое использование.

Проверено в среде Claude Code (Chromium): core 3.15.0 + ScrollTrigger +
DrawSVG + SplitText + MotionPath — рабочие.
