# iBank DS Mobile — Components Reference (из 21 05.html)

## Токены
```css
--color-primary: #14A551
--color-text-primary: #353548
--color-text-gray: #949BA6
--color-divider: #DCE0E6
--color-disabled-bg: #F5F7FA
--color-error: #DD2A4B
--color-warning: #FFA800
--color-bg: #FFFFFF
--color-surface: #FFFFFF

--text-heading-large: 500 20px/26px 'Roboto'
--text-heading-medium: 500 18px/26px 'Roboto'
--text-body-large: 500 16px/24px 'Roboto'
--text-body-regular: 400 16px/24px 'Roboto'
--text-caption-large: 500 14px/20px 'Roboto'
--text-caption-regular: 400 14px/20px 'Roboto'
--text-caption-small: 400 12px/18px 'Roboto'

--btn-height: 48px
--input-height: 56px
--field-sum-height: 64px
Кнопки
Primary

html
<button class="btn">Продолжить</button>
Высота 48px, ширина 100%, фон var(--color-primary), текст белый.
Pressed: #11A34F. Disabled: фон var(--color-disabled-bg), текст var(--color-text-disabled).

Secondary

html
<button class="btn btn-secondary">Отмена</button>
Фон var(--color-disabled-bg), текст var(--color-text-primary). Pressed: #EDF0F4.

Short pair

html
<div class="btn-short-pair">
  <button class="btn-short btn-short-primary">Да</button>
  <button class="btn-short btn-short-secondary">Нет</button>
</div>
Каждая кнопка 115×48px, отступ между ними 16px.

Product Actions pair

html
<div class="btn-product-pair">
  <button class="btn-product">
    <span class="btn-product-icon">→</span> Перевести
  </button>
  <button class="btn-product">
    <span class="btn-product-icon">+</span> Пополнить
  </button>
</div>
Кнопка 160×56px, фон var(--color-disabled-bg), текст var(--color-text-primary).
Иконка на зелёном круге 24×24px. Отступ 8px.

SBP Banner

html
<div class="sbp-banner">
  <span class="icon">💳</span>
  <span>СБП</span>
</div>
360×80px, border: 1px solid var(--color-divider), текст и иконка по центру. Некликабельно.

Поля ввода
Text field с плавающим лейблом

html
<div class="floating-group">
  <input type="text" class="floating-input" placeholder=" ">
  <label class="floating-label">Логин</label>
</div>
Input высота 56px, border 1px solid var(--color-divider), border-radius 8px.
При фокусе border-color var(--color-primary).
Ошибка: добавить класс .error к input.
Disabled: фон var(--color-disabled-bg), цвет текста var(--color-text-disabled).

Sum field (сумма)

html
<div class="floating-group">
  <input type="text" class="floating-input floating-input-sum" placeholder=" ">
  <label class="floating-label">Сумма</label>
</div>
Высота 64px, шрифт 20px. Остальное как у text field.

Preview field (нередактируемое)

html
<div class="preview-field-wrapper">
  <div class="preview-label">Счет списания</div>
  <div class="preview-text">75A533214351-051-213</div>
</div>
Лейбл — 12px regular, цвет text-gray. Текст — 16px regular, border-bottom 1px solid var(--color-preview-line).

Элементы выбора
Checkbox

html
<input type="checkbox" class="checkbox-input" id="cb1">
<label for="cb1" class="checkbox-label"></label>
Квадрат 20×20px, border-radius 6px. При :checked — зелёный фон, белая галочка.

Radio

html
<input type="radio" class="radio-input" id="rb1">
<label for="rb1" class="radio-label"></label>
Круг 20×20px. При :checked — зелёная обводка и зелёная точка внутри.

Switch

html
<input type="checkbox" class="switch-input" id="sw1">
<label for="sw1" class="switch-label"></label>
Трек 36×20px, тумблер 16px. При :checked трек становится var(--color-primary).

Tab Bar
html
<div class="tab-bar">
  <button class="tab-item active">Главная</button>
  <button class="tab-item">История</button>
</div>
Отступ между кнопками 30px. Активный — цвет primary, подчёркивание 2px.

Product Select
html
<div class="product-select-wrapper">
  <div class="product-select-label">Списать с</div>
  <div class="product-select">
    <div class="icon">₽</div>
    <div class="info">
      <div class="name">Счет в рублях *1414</div>
      <div class="amount">13 000<span class="kopecks">,00</span> ₽</div>
    </div>
    <div class="arrow">
      <svg viewBox="0 0 12 8"><path d="M2 1 L10 1 L6 7 Z"/></svg>
    </div>
  </div>
</div>
Плашка 328×64px, padding: 9px 16px, border-radius 6px. Состояния: .focus, .error, .disabled.

Dropdowns
Product dropdown

html
<div class="dropdown-wrapper">
  <div class="dropdown-field">
    <div class="icon">₽</div>
    <div class="info">...</div>
    <div class="arrow">...</div>
  </div>
  <div class="dropdown-content">
    <div class="dropdown-list">
      <div class="dropdown-item-product">...</div>
    </div>
  </div>
</div>
Поле — 64px, как product-select. Выпадающий блок — высота 200px, тень, обводка.
Элемент .dropdown-item-product: 308×52px, иконка, название, сумма.

Icon+Text dropdown
Поле .dropdown-icon-text-field, элемент .dropdown-item-icon-text (308×56px, иконка + текст).

Text dropdown
Поле .dropdown-text-field, элемент .dropdown-item-text (308×36px, только текст).

Модальные окна
Modal

html
<div class="modal-overlay open">
  <div class="modal">
    <div class="modal-icon-wrapper"><div class="warning-icon">!</div></div>
    <div class="modal-title">Внимание!</div>
    <div class="modal-text">Текст вопроса</div>
    <div class="modal-actions-row">
      <button class="modal-btn secondary">Нет</button>
      <button class="modal-btn primary">Да</button>
    </div>
  </div>
</div>
Ширина модалки 328px, border-radius 16px, тень, обводка.

Driver Sheet

html
<div class="driver-sheet open">
  <div class="driver-title">Новый продукт</div>
  <div class="driver-list">
    <button class="driver-item"><span class="driver-item-icon">💳</span> Выпустить карту</button>
  </div>
</div>
Нижний лист, ширина 360px, скругления сверху 16px.