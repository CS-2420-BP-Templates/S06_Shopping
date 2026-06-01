# S06_Shopping
Use a linkedlist (or a Doubly Linked List) to add items and calculate tax.
In a typical e-commerce application, a shopping cart requires frequent additions,
removals, and modifications of items. Using a linked list allows for efficient O(1)
insertions and deletions without the overhead of resizing arrays or shifting memory blocks.

### Key Features
* **Add Item to Cart:** Insert a new product or increase the quantity if it already exists.
* **Remove Item:** Delete a product entirely from the cart by its Product ID.
* **Update Quantity:** Traverse the cart to find a specific item and modify its quantity.
* **View Cart:** Display all items currently in the cart along with a calculated total price.
* **Clear Cart:** Safely deallocate all memory and empty the cart.

---

## 🛠️ Data Structure Design
The core of this project relies on a custom Linked List implementation rather than `std::list`.

### The Node (`CartItem`)
Each node in the list represents a unique item in the shopping cart:
```cpp
struct CartItem {
    int productId;
    std::string name;
    double price;
    int quantity;
    CartItem* next; // Point to the next item (and *prev if doing a Doubly Linked List)
};