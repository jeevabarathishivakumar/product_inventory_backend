# product_inventory_backend
🛍️ Product Inventory Management - Backend
This is the backend API for the Product Inventory Management App built using Node.js, Express, and MongoDB (Mongoose).
It provides a set of RESTful endpoints to manage a list of products with server-side validation.

📦 Features
REST API for product CRUD operations

MongoDB schema with validation

Modular route and controller structure

Environment-based configuration using .env

CORS enabled for frontend integration

Auto-reload with nodemon during development

📁 Project Structure
server/
├── controllers/
│   └── ProductControllers.js
├── models/
│   └── Product.js
├── routes/
│   └── productRoutes.js
├── .env
├── index.js
├── package.json
🛠️ Setup Instructions
1. Clone the Repository
git clone https://github.com/your-username/product-inventory-app.git
cd product-inventory-app/server
2. Install Dependencies
npm install
3. Create .env File
Create a .env file in the server/ directory with your MongoDB connection:

env
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/productdb
PORT=5000
Replace <username> and <password> with your MongoDB Atlas credentials.

4. Run the Server
# For production
node index.js

# For development (with auto-reload)
npx nodemon index.js
The backend API will be running at:
📍 http://localhost:5000/api/products

🔗 API Endpoints
Method	Route	Description
GET	/api/products	Get all products
GET	/api/products/:id	Get product by ID
POST	/api/products	Create a new product
PUT	/api/products/:id	Update existing product
DELETE	/api/products/:id	Delete a product

✅ Validation Rules
Handled via Mongoose schema:

name: required, string, minimum length 3

price: required, number, must be > 0

category: required, string

stock: required, number, must be ≥ 0

createdAt: auto-generated timestamp

🔧 Tools & Libraries
Express: Server framework

Mongoose: MongoDB ODM with schema validation

dotenv: Load environment variables

nodemon: Dev auto-restart

cors: Enable CORS for frontend connection
