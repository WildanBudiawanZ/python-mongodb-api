# python-monngo-api

## Build an Image
```
docker build -t IMAGE_NAME .
```

## Build a container
```
docker-compose up -d
```

## Add sample documents

```java script

// Membuat Collection customers
db.createCollection('customers');

// Membuat Collection products
db.createCollection('products');

// Membuat Collection orders
db.createCollection('orders');

// Insert document customers
db.customers.insertOne({
    _id: "khannedy",
    name: "Eko Kurniawan Khannedy"
});

// Insert document products
db.products.insertMany([
    {
        _id: 1,
        name: "Indomie Ayam Bawang",
        price: new NumberLong(2000)
    },
    {
        _id: 2,
        name: "Mie Sedap",
        price: new NumberLong(2000)
    }
]);

// Insert document orders
db.orders.insertOne({
    _id: new ObjectId(),
    total: new NumberLong(8000),
    items: [
        {
            product_id: 1,
            price: new NumberLong(2000),
            quantity: new NumberInt(2)
        },
        {
            product_id: 2,
            price: new NumberLong(2000),
            quantity: new NumberInt(2)
        }
    ]
})

```
