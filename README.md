# Community SavvyAI Backend Setup

This repository contains the backend code for the **Community SavvyAI** project built using Flask. Follow the steps below to set up the project and database on your local machine.

## Prerequisites

Ensure the following are installed on your machine:
- [Python 3.8+](https://www.python.org/downloads/)
- [MongoDB Compass](https://www.mongodb.com/try/download/compass)
- MongoDB Server running on `localhost:27017`

---

## Setting Up the Backend

1. **Clone the Repository**  
   Clone this repository to your local machine:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Install Dependencies**  
   Use `pip` to install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Environment Variables**  
   Create a `.env` file in the root directory with the following content:
   ```env
   MONGO_URI=mongodb://localhost:27017
   FLASK_ENV=development
   SECRET_KEY=<your-secret-key>
   ```

4. **Run the Flask Application**  
   Start the development server:
   ```bash
   python app.py
   ```
   The server will be available at `http://127.0.0.1:5000`.

---

## Setting Up MongoDB Database

### 1. Install and Configure MongoDB Compass
- Download and install MongoDB Compass from [here](https://www.mongodb.com/try/download/compass).
- Connect to your local MongoDB server using:
  ```
  mongodb://localhost:27017
  ```

### 2. Create Database and Collections
- Create a database named: `Community_Savvyai`.
- Under the `Community_Savvyai` database, create the following collections:
  - `GAQ`
    - Subcollections: `easy`, `medium`, `hard`
  - `NPTEL_Course_Details`
    - Subcollection: `2024_WA`

### 3. Import Data into Collections
- Download the data files from the provided [Google Drive link](#).
- For each collection:
  1. Select the collection in MongoDB Compass.
  2. Click **Add Data** > **Import File**.
  3. Select the JSON file corresponding to the collection and click **Import**.

---

## Using Third-Party APIs (e.g., MistralAI)

This project integrates with third-party APIs like **MistralAI**. To set up access:
1. Visit [MistralAI's website](https://mistralai.com) to create an account.
2. Generate an API key from the dashboard.
3. Add the API key to your `.env` file:
   ```env
   MISTRAL_API_KEY=<your-api-key>
   ```

---

## Running the Application

After completing the setup, you can test the application by visiting:
```
http://127.0.0.1:5000
```

Ensure the MongoDB server is running and the required collections are correctly populated.

---

## Support

If you encounter any issues, feel free to raise an issue in this repository or contact the maintainers.
