# Fetching API in React

## 📌 Overview

This project demonstrates how to fetch data from an external API in React using the `fetch()` method and React Hooks. The fetched product data is stored in state and can be displayed dynamically in the user interface.

## 🎯 Objectives

- Understand API fetching in React.
- Learn how to use the `fetch()` method.
- Use `useState()` to store API data.
- Use `useEffect()` to fetch data when a component mounts.
- Handle API errors using `.catch()`.
- Display fetched products dynamically.

## 🛠️ Technologies Used

- React.js
- JavaScript (ES6+)
- HTML
- CSS
- Fake Store API
- Vite

## 📚 Key Concepts

### 1. What is an API?

An API (Application Programming Interface) allows two applications to communicate and exchange data.

### 2. What is `fetch()`?

The `fetch()` method sends a request to a URL and retrieves a response from a server.

Example:

```javascript
fetch("https://fakestoreapi.com/products")
  .then((res) => res.json())
  .then((data) => console.log(data))
  .catch((error) => console.error(error));
```

### 3. What is `useState()`?

The `useState()` hook stores data in a component's state. When the state changes, React updates the UI.

```jsx
const [products, setProducts] = useState([]);
```

- `products` stores the fetched products.
- `setProducts` updates the product state.
- `[]` represents the initial empty array.

### 4. What is `useEffect()`?

The `useEffect()` hook performs side effects, such as fetching data from an API.

```jsx
useEffect(() => {
  // Fetch API data
}, []);
```

The empty dependency array `[]` means the effect runs after the component's initial render.

### 5. Handling API Responses

```javascript
fetch("https://fakestoreapi.com/products")
  .then((res) => res.json())
  .then((data) => {
    console.log(data);
    setProducts(data);
  })
  .catch((error) => {
    console.error("Error fetching data:", error);
  });
```

- `fetch()` requests product data.
- `res.json()` converts the response body into JSON.
- `setProducts(data)` stores the products in state.
- `.catch()` handles errors encountered during the request or response processing.

## 🔄 How It Works

1. The React component renders.
2. `useEffect()` runs after the initial render.
3. `fetch()` requests product data from the Fake Store API.
4. The response is converted into JSON.
5. `setProducts()` stores the fetched data.
6. React re-renders the component with the updated data.
7. The products can be displayed using `.map()`.

## 🌐 API Used

Fake Store API:

https://fakestoreapi.com/products

This API provides sample e-commerce product data, including product IDs, titles, prices, images, and categories.

## 💡 Key Learning Outcomes

- Fetching external data in React.
- Managing state using `useState()`.
- Running API requests using `useEffect()`.
- Handling promises with `.then()` and `.catch()`.
- Dynamically rendering API data.
- Understanding basic API error handling.

## 🏁 Conclusion

Fetching APIs is an essential skill in React development. By combining `fetch()`, `useState()`, and `useEffect()`, we can retrieve external data, store it in state, and display it dynamically in a React application.
