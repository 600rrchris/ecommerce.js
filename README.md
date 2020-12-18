Ecommerce JS
1. Create folder structure
    1. Create root folder as Ecommercejs
    2. Add frontend and backend folder
    3. create src folder in frontend
    4. create index.html with heading Ecommerce JS in src
    5. run npm init in frontend folder
    6. npm install live-server
    7. add start command as liver-server src --verbose
    8. run npm start

2. Design Website
    1. create style.css
    2. link style.css to index.html
    3. create div.grid-container
    4. create header, main and footer
    5. style html, body
    6. style grid-container, header, main and footer

3. Create Static Home Screen
    1. create ul.products
    2. create li
    3. create div.product
    4. add .product-image, .product-name, .product-brand, .product-price
    5. style ul.products and internal divs
    6. duplicate 2 times to show 3 products

4. Render Dynamic Home Screen
    1. create data.js
    2. export and array of 6 products
    3. create screen/HomeScreen.js
    4. export HomeScreen as an object with render() method
    5. implement render()
    6. import data.js
    7. return products mapped to lis insdie an ul
    8. create app.js
    9. link it to index.html as module
    10. set main id to main_container
    11. create router() function
    12. set main_container innerHTML to HomeScreen.render()
    13. set load event of winder to router() function

5. Build Url Router
    1. create routes as route:screen object for home screen
    2. create utils.js
    3. export parseRequestURL()
    4. set url as hash address split by slash
    5. return resource  id and verb of url
    6. update router()
    7. set request as parseRequestURL()
    8. build parseUrl and compare with routes
    9. if route exists render it, else render Error404
    10. create screens/Error404.js and render error message

6. Create Node.JS Server
    1. run npm init in root folder
    2. rpm install express
    3. create server.js
    4. add start command as node backend/server.js
    5. require express
    6. move data.js from frontend to backend
    7. create route for /api/products
    8. return products in data.js
    9. run npm start

7. Load Products From Backend
    1. edit HomeScreen.js
    2. make render async 
    3. fetch products from '/api/products' in render()
    4. make router() async and call await HomeScreen.render()
    5. use cors on backend

8. Add Webpack
    1. cd Frontend
    2. npm install -D webpack webpack-cli webpack-dev-server
    3. npm unintall live-server
    4. "start": "webpack-dev-server --mode development --watch-content-base --open"
    5. move index.html, style.css and images to frontend folder
    6. rename app.js to index.js
    7. update index.html
    8. add <script src="main.js"></script>before </body>
    9. npm start
    10. npm install axios
    11. change fetch to axios in HomeScreen

9. Insatll Babel For ES6 Syntax
    1. npm install -D babel core, cli, node, preset-env
    2. Create .baelrc and set presets to @babel/preset-env
    3. npm insatll -D nodemon
    4. set start: nodemon --watch backend --exec babel-node backend/server.js
    5. convert require to import in server.js
    6. npm start

10. Enable Code Linting
    1. npm install -D eslint 
    2. instal VSCode eslint extension
    3. create .eslintrc and set module.exports for env to node
    4. set VSCode setting for editor.codeActionsOnSave source.fixAll.eslint to true
    5. check result for linting error
    6. npm install eslint-config-airbnb-base and eslint-plugin-import
    7. set extends to airbnb-base
    8. set parserOptions to ecmaVersion 11 and sourceType to module
    9. set rules for no-console to 0 to ignore linting error

11. Install VSCode Extension
    1. JavaSscript (ES6) code snippets
    2. ES7 React/Redux/GraphQL/React-Native snippets
    3. Prettier - Code formatter
    4. HTML&LESS grammar injections
    5. CSS Peek

12. Create Rating Component
    1. create components/Rating.js
    2. create div.rating
    3. link to fontawesome.css in index.html
    4. define Rating object with render()
    5. if !props.value return empty div
    6. else use fa fa-star, fa-sar-half-o and fa-star-o
    7. lasdt span for props.text || ' '
    8. style div.rating, span and last span
    9. Edit HomeScreen
    10. Add div.product-rating and use Rating component

13. Product Screen
    1. get product id from request 
    2. implement /api/product/:id api
    3. send Ajax request toproduct api
    4. create back to restult link 
    5. create div.details with 3 columns 
    6. column 1 for product image
    7. column 2 for product information
    8. column 3 form product action
    9. style .detial and all columns 
    10. create add to cart button with add-button id
    11. after_render() to add event to the button 
    12. redirect user to cart/:product_id

14. 

15.

16. Add to Cart Action
    1. create CartScreen.js
    2. parseRequestUrl
    3. getProduct(request.id)
    4. addToCart
    5. getCartItems
    6. cartItems.find
    7. if existItem update qty
    8. else add item
    9. setCartItems

17. Cart Screen UI 
    1. cartItems = getCartItems()
    2. create 2 columns for cart items and cart actiion
    3. cartItems.length === 0 ? cart is empty
    4. show item image, name qty and price
    5. cart action
    6. Subtotal 
    7. Proceed to Checkout button
    8. Add CSS Style

 18. Update and Delete Cart Items
    1. add   
    2. after_render()
    3. add change event to qty select
    4. getCartItems() and pass to addToCart()
    5. set force to true to addToCart()
    6. create rerender() as (component, areaName = 'content')