# Навчання по роботі з CSS Grid

## Зміст

1. [Вступ](#вступ)
2. [Основи CSS Grid](#основи-css-grid)
3. [Створення простого грід-контейнера](#створення-простого-грід-контейнера)
4. [Розташування елементів у грід-контейнері](#розташування-елементів-у-грід-контейнері)
5. [Використання грід-шаблонів](#використання-грід-шаблонів)
6. [Адаптивні макети з CSS Grid](#адаптивні-макети-з-css-grid)
7. [Ресурси](#ресурси)

## Вступ

CSS Grid Layout — це двовимірна система макетів для веб-дизайну. Вона дозволяє
розміщувати елементи у вигляді сітки з рядків і стовпців, що полегшує створення
складних макетів.

## Основи CSS Grid

CSS Grid складається з грід-контейнера та грід-елементів. Грід-контейнер — це
батьківський елемент, до якого застосовується властивість `display: grid;`.
Грід-елементи — це дочірні елементи грід-контейнера.

## Створення простого грід-контейнера

Щоб створити грід-контейнер, додайте властивість `display: grid;` до
батьківського елемента.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS Grid Basics</title>
    <style>
      .grid-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 10px;
      }
      .grid-item {
        background-color: lightblue;
        border: 1px solid #333;
        padding: 20px;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <div class="grid-container">
      <div class="grid-item">1</div>
      <div class="grid-item">2</div>
      <div class="grid-item">3</div>
      <div class="grid-item">4</div>
      <div class="grid-item">5</div>
      <div class="grid-item">6</div>
    </div>
  </body>
</html>
```

## Розташування елементів у грід-контейнері

Для розташування елементів у грід-контейнері використовуйте властивості
`grid-template-columns` і `grid-template-rows`.

```
.grid-container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: auto;
}
```

## Використання грід-шаблонів

Грід-шаблони дозволяють визначати макет у вигляді рядків і стовпців.

```
.grid-container {
  display: grid;
  grid-template-columns: 100px 200px 100px;
  grid-template-rows: 100px 200px;
  gap: 10px;
}
```

## Адаптивні макети з CSS Grid

CSS Grid дозволяє створювати адаптивні макети за допомогою медіа-запитів.

```
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  gap: 10px;
}

@media (max-width: 600px) {
  .grid-container {
    grid-template-columns: 1fr;
  }
}
```

## Ресурси

- [MDN Web Docs: CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [A Complete Guide to Grid | CSS-Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Grid by Example](https://gridbyexample.com/)
- [CSS Grid Layout Module Level 1](https://www.w3.org/TR/css-grid-1/)
