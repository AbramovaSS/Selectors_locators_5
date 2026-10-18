# Домашнее задание. Селекторы и локаторы

## Написать CSS- и XPath-локаторы для веб-элементов тестового стенда SmartShop:

1. Список названий товаров

````
.products-grid div[data-name]
````
````
//div[contains(@class, 'products-grid')]//div[@data-name]
````

2. Список цен товаров 

````
.products-grid div[data-price]
````
````
//div[contains(@class, 'products-grid')]//div[@data-price]
````

3. Название товара с ценой 25

````
.products-grid .product-card:has([data-price="25"]) [data-name]
````

````
//div[@class='product-card' and @data-price='25']/h4
````

4. Цена товара с названием "Стакан"

````
.products-grid .product-card:has([data-name="Стакан"]) [data-price]
````

````
//div[@class="product-card" and @data-name="Стакан"]/div[contains(text(), "₽")]
````

5. Список карточек товаров в корзине

````
#cart-items .cart-item
````

````
//div[@id="cart-items"]/div[@class="cart-item"]
````

6. Кнопка корзины

````
#open-cart-btn
````

````
//*[@id="open-cart-btn"]
````
