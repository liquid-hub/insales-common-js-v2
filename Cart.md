# Корзина

## Методы

### add

> Добавить в корзину заданное кол-во товаров

<details>
<summary>:memo: Параметры</summary>

```js
/**
 * items {Object} хэш таблица добавляемых товаров. Ключ id варианта, значение кол-во.
 * comments {Object} комментарий к позиции заказа. Ключ id варианта, значение текст комментария.
 * coupon {string} купон
 */
{
  items: {
    123456: 2,
    123457: 1
  },
  comments: {
    123457: 'Мой комментарий'
  },
  coupon: 'Мой купон'
}
```
</details>
<details>
<summary>:computer: Пример</summary>

```js
Cart.add({
  items: {
    123456: 2,
    123457: 1
  },
  comments: {
    123457: 'Мой комментарий'
  },
  coupon: 'Мой купон'
});
```
</details>

---

### delete

> Удалить позиции из корзины

<details>
<summary>:memo: Параметры</summary>

```js
/**
 * items {Array} массив id вариантов к удалению
 */
 {
   items: [160549240, 160549242]
 }
```
</details>
<details>
<summary>:computer: Пример</summary>

```js
Cart.delete({
  items: [160549240, 160549242]
})
```
</details>

---

### clear

> Полностью очистить корзину


<details>
<summary>:computer: Пример</summary>

```js
Cart.clear();
```
</details>

---

### remove

> Удадить из корзины заданное кол-во товаров

<details>
<summary>:memo: Параметры</summary>

```js
/**
* items {Array}  объект с параметрами variant_id: quantity
*/
{
  items: {
    138231315: 1,
    138231316: 1
  }
}
```
</details>
<details>
<summary>:computer: Пример</summary>

```js
Cart.remove({
  items: {
    138231315: 1,
    138231316: 1
  }
})
```
</details>

---

### set

> Устанавливает кол-во товаров в корзине для каждой позиции

<details>
<summary>:memo: Параметры</summary>

```js
/**
* items {Array}  объект с параметрами variant_id: quantity
*/
{
  items: {
    138231315: 1,
    138231316: 1
  }
}
```
</details>
<details>
<summary>:computer: Пример</summary>

```js
Cart.set({
  items: {
    138231315: 1,
    138231316: 1
  }
})
```
</details>

---

### setCoupon

> Устанавливает купон

<details>
<summary>:memo: Параметры</summary>

```js
/**
* coupon {string}  код купона
*/
{
  coupon: 'Мой купон'
}
```
</details>
<details>
<summary>:computer: Пример</summary>

```js
Cart.setCoupon({
  coupon: 'Мой купон'
})
```
</details>

---

### getOrder

> Получить состав корзины

<details>
<summary>:computer: Пример</summary>

```js
var order = Cart.getOrder();
console.log(order);
```
</details>
