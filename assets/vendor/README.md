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

## chartjs/ — Chart.js 4.5.1 (npm chart.js)

- `chart.umd.min.js` — UMD-сборка, обычный `<script src=...>`;
- `LICENSE.md` — MIT.

Нужен скиллу slides (графики в HTML-презентациях). Проверен рендером
в Chromium этой среды.

## fonts/ — фирменная типографика (@fontsource, OFL)

Variable-шрифты woff2 c кириллицей и латиницей (RU/EN/UZ):
- `inter/` — Inter (основной текст, wght 100–900);
- `manrope/` — Manrope (заголовки, цифры, wght 200–800);
- `playfair/` — Playfair Display (акцентные serif-заголовки, wght 400–900).
Подключение: `fonts/fonts.css` (@font-face с unicode-range).

## d3/ + geo/ — карты (npm d3 7.9, topojson-client 3.1, world-atlas 2.0.2)

- `d3/d3.min.js`, `d3/topojson-client.min.js` — UMD;
- `geo/countries-110m.json` — контуры стран (обзорные карты);
- `geo/countries-50m.json` — детальнее (крупные планы).
Узбекистан: id "860" (ISO numeric). Проверено картой Центральной Азии.

## icons/lucide/ — иконки Lucide 1.49 (ISC)

- `icon-nodes.json` — вектор-данные всех ~1600 иконок (тег+атрибуты);
  из него собирается инлайн-SVG любой иконки (viewBox 0 0 24 24,
  stroke-width 2, fill none);
- `sprite.svg` — спрайт для <use>; `tags.json` — поиск по ключевым словам.

## three/addons/ — дополнения Three.js r128

- `GLTFLoader.js`, `RGBELoader.js` — загрузка 3D-моделей (glTF) и HDR-окружения;
- `EffectComposer/RenderPass/ShaderPass/MaskPass` + `UnrealBloomPass` +
  `CopyShader/LuminosityHighPassShader/FXAAShader` — постобработка:
  свечение (корона на изоляторах, огни), сглаживание.
Порядок подключения скриптов: шейдеры → EffectComposer → пассы.
Проверено рендером bloom-эффекта.
