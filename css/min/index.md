---
title: "`min()`"
description: "Функция, выбирающая меньшее значение. Удобно для адаптивной вёрстки и не только!"
authors:
  - gingerraccoon
keywords:
  - наименьшее из двух
related:
  - js/function
  - css/calc
  - css/numeric-types
tags:
  - doka
---

## Кратко

Функция `min()` возвращает наименьшее из перечисленных через запятую значений внутри круглых скобок.

## Пример

```css
.selector {
  width: min(50%, 500px);
}
```

## Как пишется

Функция принимает одно или несколько значений, разделённых запятой. Так же поддерживается вложенность других функций, например [`calc()`](/css/calc/):

```css
.selector {
  width: min(50%, calc(1000px / 2));
}
```

Использовать функцию можно в любых CSS-свойствах, значение которых является числом, например:

```css
.selector {
  background: linear-gradient(135deg, #2c3e50, #2c3e50 min(20vw, 60%), #3498db);
}
```

## Как понять

При отрисовке браузер определяет минимальное значение и подставляет его в стили.

<iframe title="Работа функции min()" src="demos/view/index.html" height="470"></iframe>

В примере выше использованы значения `min(50vw, 350px)`, что буквально означает: элемент занимает половину ширины [вьюпорта](/css/vw-vh/#vw), но не больше 350 px.

## Подсказки

💡 Очень удобно с помощью функции `min()` ограничивать ширину компонента в зависимости от ширины родителя.
