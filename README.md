### GET /products

Sort of the item by name or created_At

**Query Params**

`name` - string, will fuzzy search using `LIKE '%name%'`
`created_At` - timestamp, will match exactly

**Sample Response** 

``
[
    {
        "id": 10,
        "name": "Chelsea",
        "created_At": 10/8/2004
    }
]
``


---
### GET /products
List product, can be searched or sorted
**Query Params**
`sorting` - string, possible selections are:
1. name_asc
2. name_desc
3. date_asc
4. date_desc
5. price_asc
6. price_desc
**Sample Response** 
```
[
    {
        "id": 2,
        "name": "All",
        "price": 42,
        "created_date": "DD-MM-YYYY"
    }
]
```
---
### GET /product
List product, can be searched or sorted
**Query Params**
`product` - string, will fuzzy search using `LIKE '%name%'`
`items` - number, will match exactly
**Sample Response** 
```
[
    {
        "id": 6,
        "product": "Football Jersey",
        "price": 24
    }
]
```


---


### Post /line_items

Post data into the DB after checkout

**Query Params**

`id` - int, 
`quantity` - int, will post the quantity 
`total_price` - float, will post the total price
`created_at` - timestamp, will post the created_at
`product_id` - int, will post the product id
`purchase_id` - int, will post the purchase id
**Sample Response** 

``
[
    {
        "id": 50,
        "quantity": 5,
        "total_price": "1250.00",
         "created_date": "DD-MM-YYYY"
        "product_id": 12,
        "purchase_id": 15
    }
]
``

---

### Delete /products/{id}
Delete data for products

**Sample Response** 

``
{
    "message": "Successfully deleted"
}
``

---

### post /products
Create product
**Query Params**
`adding` - string, possible selections are:
1. name
2. price
3. created_date
**Sample Response** 
``
[
    {
        "id": 2,
        "name": "Arsenal",
        "price": 32,
        "created_date": "DD-MM-YYYY"
    }
]

---

### post /products
Update product
**Query Params**
`updating` - string, possible selections are:
1. name
2. price

**Sample Response** 
```
[
    {
        "name": "Arsenal",
        "price": 32,
        
    }
]

