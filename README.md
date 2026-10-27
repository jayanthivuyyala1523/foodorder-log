# 🍽️ Food Order Log

### Track Your Food Orders. Manage Your Spending. Enjoy Every Bite.

Food Order Log is a food-order management web application that helps users organize their food orders, track spending, categorize cuisines, and monitor delivery status through a clean and user-friendly interface.

🔴 **Live Demo:** https://foodorder-log-xi.vercel.app/

📂 **GitHub Repository:** https://github.com/jayanthivuyyala1523/foodorder-log

---

## ✨ Features

- 🍕 **Food Menu** — Explore a curated selection of food items across multiple cuisines.
- 📝 **Order Management** — Add new orders and update existing order details.
- 🗑️ **Delete Orders** — Remove orders with a confirmation step.
- 💰 **Spending Tracker** — View the combined bill amount for recorded orders.
- 🍜 **Cuisine Filtering** — Organize orders by cuisine category.
- ↕️ **Sorting Options** — Sort orders to make reviewing them easier.
- 🚚 **Delivery Tracking** — Track whether an order has been delivered.
- 📅 **Order Dates** — Record and review when orders were placed.
- 📊 **Order Overview** — View your orders and spending information.
- 📱 **Responsive Interface** — Designed for a convenient experience across different screen sizes.
- 🔄 **Database Integration** — Store and retrieve order information using MongoDB.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| React | Frontend user interface |
| Vite | Development server and build tooling |
| JavaScript | Application logic |
| CSS | Styling and responsive layouts |
| Node.js | Backend runtime |
| Express.js | REST API |
| MongoDB | Persistent order storage |
| Mongoose | MongoDB object modeling |
| Vercel | Frontend deployment |

## 🍽️ Cuisine Categories

The application includes a selection of food items from different culinary traditions:

- 🇮🇳 Indian Biryani
- 🥞 South Indian
- 🍕 Italian & Pizza
- 🍜 Chinese & Asian
- 🌮 World Favorites

## 🚀 Getting Started

Follow these steps to run the project locally.

### 1. Clone the repository

```bash
git clone https://github.com/jayanthivuyyala1523/foodorder-log.git
cd foodorder-log
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create the environment files required by your frontend and backend.

For the Vite frontend, create a `.env` file in the project root:

```env
VITE_API_URL=http://localhost:3000
```

For the backend, configure the MongoDB connection string using the environment variable expected by the backend:

```env
mongodb_url=your_mongodb_connection_string
PORT=3000
```

Replace the example database connection string with your own MongoDB connection string. Never commit real credentials, database passwords, or API keys to GitHub.

### 4. Start the frontend

```bash
npm run dev
```

Vite will display the local development URL in your terminal.

### 5. Start the backend

Run the backend from its directory after installing its required dependencies and configuring its environment variables.

```bash
cd backend
npm install
node server.js
```

Ensure MongoDB is accessible and the backend is running before testing database-dependent features.

## 🔌 API Endpoints

The Express backend exposes REST endpoints for managing food orders.

| Method | Endpoint | Description |
|---|---|---|
| GET | `/orders` | Retrieve orders |
| GET | `/orders/total` | Calculate total spending |
| GET | `/orders/:id` | Retrieve an order by ID |
| POST | `/orders` | Create a new order |
| PUT | `/orders/:id` | Update an existing order |
| DELETE | `/orders/:id` | Delete an order |

### Query Parameters

- `cuisine` — Filter orders by cuisine.
- `sort=bill` — Sort orders by bill amount in ascending order.

By default, orders are sorted by order date, newest first.

## 🌐 Deployment

**Live application:** https://foodorder-log-xi.vercel.app/

The frontend is deployed on Vercel. To deploy your own version, import the GitHub repository into Vercel and configure the appropriate build settings and environment variables.

For production use, ensure that:

- The backend API is deployed and publicly reachable over HTTPS.
- `VITE_API_URL` points to the deployed API rather than `localhost`.
- MongoDB connection credentials are configured securely on the backend.
- CORS is configured to permit requests from the deployed frontend.
- The database is accessible from the backend hosting environment.

> Note: The frontend deployment and backend/database availability are separate. Confirm that the API and database are configured correctly for all features to work in production.

## 📁 Project Structure

```text
foodorder-log/
├── backend/
│   └── server.js
├── config/
│   └── db.js
├── controllers/
│   └── orderscontroller.js
├── middleware/
│   └── errorhandler.js
├── models/
│   └── orders.js
├── public/
├── src/
│   ├── assets/
│   ├── App.jsx
│   ├── App.css
│   ├── index.css
│   └── main.jsx
├── index.html
├── package.json
├── package-lock.json
└── README.md
```

The repository also includes a Streamlit-based application file, `streamlitapp.py`, for a separate Streamlit interface.

## 🔐 Security

- Keep database credentials in environment variables or hosting secrets.
- Exclude `.env` files from version control.
- Never publish passwords, private API keys, or database connection strings.
- Restrict database access and configure appropriate production security controls.

## 🎯 Project Goals

Food Order Log demonstrates practical full-stack development concepts, including:

- Component-based frontend development.
- RESTful API design.
- CRUD operations.
- Database integration.
- Environment-based configuration.
- Deployment and production setup.

## 👩‍💻 Author

**Vuyyala Jayanthi**

GitHub: [@jayanthivuyyala1523](https://github.com/jayanthivuyyala1523)

## 📄 License

No license has been specified yet. Unless a license is added to this repository, reuse and redistribution are subject to the applicable copyright rules.

---

⭐ If you find this project useful, consider giving the repository a star!

**Try the application:** https://foodorder-log-xi.vercel.app/

**Explore the source code:** https://github.com/jayanthivuyyala1523/foodorder-log
