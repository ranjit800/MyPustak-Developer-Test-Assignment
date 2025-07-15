# MyPustak Developer Assignment – Book Listing App

This project is a simple Book Listing application built using Django REST Framework for the backend and React Native (Expo CLI) for the frontend.

---

## Project Structure

```
MyPustak/
├── book-backend/   # Django REST API
├── book-app/       # React Native App (Expo)
```

---

## Backend – Django REST API

**Location:** `book-backend/`

### Features

- `GET /books/` – Returns a list of books (hardcoded)
- `POST /order/` – Accepts book ID and customer name, returns order confirmation

### How to Run

1. Open terminal and navigate to the backend folder:
   ```bash
   cd book-backend
   ```

2. Activate the virtual environment (Windows):
   ```bash
   env\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the Django server:
   ```bash
   python manage.py runserver
   ```

### API Endpoints

- **GET `/books/`**

  Returns a static list of books:
  ```json
  [
    { "id": 1, "title": "Clean Code", "author": "Robert C. Martin" },
    { "id": 2, "title": "Atomic Habits", "author": "James Clear" },
    { "id": 3, "title": "Deep Work", "author": "Cal Newport" }
  ]
  ```

- **POST `/order/`**

  Example request body:
  ```json
  {
    "book_id": 1,
    "customer_name": "John Doe"
  }
  ```

---

## Frontend – React Native App (Expo CLI)

**Location:** `book-app/`

### Features

- Displays a list of books fetched from the backend
- Tapping a book navigates to an order form
- User can enter their name and place an order
- Shows success or error messages based on response

### How to Run (on Android Emulator)

1. Navigate to the frontend folder:
   ```bash
   cd book-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start your Android Emulator manually.

4. Run the app:
   ```bash
   npm run android
   ```

### Important Note

For Android emulator, use this base URL in `axios`:
```js
http://10.0.2.2:8000/
```

This allows the emulator to communicate with your local Django server.

---

## Highlights

- Clean and readable code with comments
- Organized folder structure following best practices
- Proper API integration with error handling
- Simple and functional UI
- No database used; book data is hardcoded
- No authentication required

---

## Submission

- All code is pushed to GitHub
- This `README.md` is included with instructions for both backend and frontend
- Completed within the required timeline

---

Developed by [Ranjit Jana]('https://github.com/ranjit800/MyPustak-Developer-Test-Assignment')
