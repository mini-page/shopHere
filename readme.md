# 🛒 Shopping Page (Tailwind CSS + JavaScript)

## 🚀 Overview
This project is a modern **Shopping Page** built with **HTML, Tailwind CSS, and JavaScript**. It dynamically fetches product data from an API, displays products in a responsive grid, and includes a search bar with real-time filtering.

---

## 📌 Features

✅ **Dynamic Product Display** – Fetches and displays products from `dummyjson.com/products` API.
✅ **Search Functionality** – Allows users to search for products by title.
✅ **Datalist Suggestions** – Provides predefined product suggestions in the search bar.
✅ **Stock Indicator** – Displays real-time stock availability using color-coded dots.
✅ **Discount Calculation** – Shows both original and discounted prices.
✅ **Wishlist Button** – Adds a heart icon to mark favorite products.
✅ **Responsive Design** – Optimized for all screen sizes using Tailwind CSS.

---

## 🛠️ Tech Stack

- **HTML5** – Structure and semantic elements
- **Tailwind CSS** – Styling and responsive design
- **JavaScript** – Fetch API, DOM manipulation, and event handling
- **Font Awesome** – Icons for UI enhancements

---

## 📂 File Structure

```
📦 Shopping Page
├── 📄 index.html       # Main shopping page
├── 📜 README.md       # Project documentation
└── 📂 assets          # (Optional) Folder for images & additional files
```

---

## 🔧 Setup & Usage

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/mini-page/shopHere.git
cd shopHere
```

### 2️⃣ Open in Browser
Simply open `index.html` in your favorite browser.

### 3️⃣ Modify Products List
To manually edit product suggestions, update the `<datalist>` in `index.html`:
```html
<datalist id="product-suggestions">
    <option value="Apple"></option>
    <option value="Banana"></option>
    <option value="Milk"></option>
    <option value="Eggs"></option>
</datalist>
```

---

## 🎯 How It Works

### 🔹 Fetching Products from API
The products are dynamically fetched from `dummyjson.com/products` using JavaScript.
```js
async function fetchProducts() {
    const response = await fetch('https://dummyjson.com/products');
    const data = await response.json();
    displayProducts(data.products.slice(0, 8));
}
```

### 🔹 Search Functionality
Filters product cards based on user input.
```js
searchInput.addEventListener("input", () => {
    const query = searchInput.value.toLowerCase();
    document.querySelectorAll("#product-container > div").forEach(card => {
        card.style.display = card.querySelector("h2").textContent.toLowerCase().includes(query) ? "block" : "none";
    });
});
```

---

## 📌 Future Improvements
- 🛍️ **Add Cart Functionality** – Enable users to add/remove items from a cart.
- 🌐 **API Enhancement** – Fetch more product details dynamically.
- 🎨 **Better UI/UX** – Improve styling and animations.

---

## 📝 License
This project is **free to use** for educational purposes.

---

💡 *Happy Coding!* 🚀

