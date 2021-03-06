# Селектор

Для отступа между парами, то есть перед каждым нечётным элементом, можно использовать селектор [nth-child](http://css-tricks.ru/Articles/Details/HowNthChildWorks).

Селектор будет `li:nth-child(odd)`, к нему нужно ещё добавить отсечение первого элемента: `li:nth-child(odd):not(:first-child)`.

Можно поступить и по-другому: `li:nth-child(2n+3)` выберет все элементы для `n=0,1,2...`, то есть 3й, 5й и далее, те же, что и предыдущий селектор. Немного менее очевидно, зато короче.

# Правило

Отступ, размером в одну строку, при `line-height: 1.5` -- это `1.5em`.

Поставим отступ перед каждым *нечётным* элементом, кроме первого:

```css
li:nth-child(odd):not(:first-child) {
  margin-top: 1.5em;
}
```

Получится так:

```html
<!--+ run src="index.html" -->
```

