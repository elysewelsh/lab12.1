# 📋 Recipe Discovery

A basic web server serving homepage and contact page for The Daily Grind coffee shop.

## 💻 Technologies Used

* **Node.js** 
* **Express.js**
* **HTML**

## ✨ Features

* **Serves Pages:** serves home and contact page

## ⚙️ Installation

To run this project locally, execute the following commands in your terminal:

```bash
# Clone the repository
git clone https://github.com/elysewelsh/lab12.1.git

# Navigate into the directory
cd daily-grind-server

# Install dependencies (Express, nodemon, etc.)
npm install

# Start the local development server
npm run dev
```

## 📖 References

* **Project References:** 
    - https://perscholas.instructure.com/courses/3086/pages/module-12-node-and-express?module_item_id=2452837

## 💖 Acknowledgements

Permission has been given to use my repository as reference material to anyone in class.

## 🧘 Reflections

1. What is the difference between res.send() and res.sendFile()? When would you use one over the other?
  >If I were just sending a string of text, I would use res.send(). If I were serving an entire HTML file, I would use res.sendFile().
2. Why is the path module necessary when serving files? What could go wrong if you just used a relative path like 'public/index.html'?
  >Depending on where you run the node command from, Express may not know the specific file you're referring to. The path module is necessary to create reliable, foolproof paths. (https://perscholas.instructure.com/courses/3086/pages/module-12-node-and-express?module_item_id=2452837)
3. How would you add a third page (e.g., a menu page) to this server? What steps would you take?
  >1. Create the menu page (menu.html) in the public folder.
  >1. Add boilerplate HTML in menu.html and insert text and assets like images or links
  >1. Create CSS styling in menu.css or generic styles.css
  >1. Link the stylesheet to menu.html
  >1. Add this code to the server.js file: 
    >```
    >app.get('/menu', (req, res) => {res.sendFile(path.join(__dirname, 'public/menu.html'))})
    >```
  >1. View the site and test functionality