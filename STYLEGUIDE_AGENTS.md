# STYLEGUIDE AGENTS — iBank Mobile Bank

## Цель
Генерация HTML/CSS экранов по iBank DS styleguide.

## Глобальные правила
- Используй CSS-переменные из `components.md`.
- Ширина контента 328px, отступы 16px, экран 360px.
- Touch targets ≥48px.
- Без лишних скриптов.
- Компоненты только из стайлгайда.

## Формат JSON для фронтенд-агента
{
  "screen": "string",
  "elements": [
    {"type": "title", "text": "...", "style": "heading-large/medium"},
    {"type": "product-select", "label": "...", "state": "default/focus/error/disabled"},
    {"type": "input-text", "label": "...", "state": "default/error/disabled"},
    {"type": "input-sum", "label": "..."},
    {"type": "button", "text": "...", "variant": "primary/secondary/short/product"},
    {"type": "tab-bar", "tabs": ["Главная", "История"]},
    {"type": "modal", "title": "...", "text": "..."}
  ]
}