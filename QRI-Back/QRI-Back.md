# QRI-Back

## Database Models

### Store

- **id**: int - the id of the store (auto increment)
- **name**: str - the name of the store
- **address**: str - address of the store
- **inventory**: List[Item] - list of items located in the store

### Item

- **id**: int - the id of the item (auto increment)
- **name**: str - the name of the item
- **brand**: Optional[Brand] - brand of the item
- **locationStore**: Optional[str] - the location of the item in the store
- **locationSupplier**: Optional[str] - the location of the item at the supplier's store
- **amount**: int - the amount of the item

### Brand

- **id**: int - the id of the brand (auto increment)
- **name**: str - the name of the brand
- **listSupplier**: List[Supplier] - list of suppliers that sell this brand

### Supplier

- **id**: int - the id of the supplier (auto increment)
- **name**: str - the name of the supplier
- **address**: Optional[str] - the address of the supplier if one exists
- **phone**: Optional[str] - the phone number of the supplier
- **URL**: Optional[str] - supplier's website
- **inventory**: List[Item] - list of items that he supplier offers

### Order

- **id**: int - the id of the order (auto increment)
- **name**: Optional[str] - the name of the order
- **lastOrder**: datetime - time of the latest order
- **orderAmount**: int - amount to order
- **items**: List[Item] - list of items to order
- **suppliers** List[Supplier] - list of suppliers to order from

## Database Handlers

### Base Model

- **new()**:
- **delete()**:
- **getID()**:
- **getName()**:
- **setName()**:

### Store

- **getAddress()**:
- **setAddress()**:
- **getInventory()**:
- **addItemInventory()**:
- **removeItemInventory()**:

### Item

- **addItem(string name, string brand, string locationStore, string locationSupplier, int[] amount)**: 
- **removeItem()**: 
- **getBrand**:
- **setBrand**:
- **getLocationStore**:
- **setLocationStore**:
- **getLocationSupplier**:
- **setLocationSupplier**:
- **getAmount**:
- **setAmount**:

### Brand

- **getListSuppliers()**:
- **addListSupplier()**:
- **removeListSupplier()**:

### Supplier

- **getAddress()**:
- **setAddress()**:
- **getPhone()**:
- **setPhone()**:
- **getURL()**:
- **setURL()**:
- **getInventory()**:
- **setInventory()**:
- **addItemInventory()**:
- **removeItemInventory()**:

### Order

- **getItemList()**:
- **addItemList()**:
- **removeItemList()**:
- **getSupplierList()**:
- **addSupplierList()**:
- **removeSupplierList()**:
- **getLastOrder()**:
- **getOrderAmount**:
- **setOrderAmount**: