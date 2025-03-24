# Text-to-SQL Streamlit App

This is a **Streamlit-based web application** that allows users to interact with an **SQLite database** using natural language. The application leverages **LangChain** with the **Groq API** to convert English queries into SQL commands and retrieve results from the database.

---

## Features
- Convert **natural language queries** into **SQL statements**.
- Retrieve and display **data** from an SQLite database.
- Interactive **Streamlit UI** for a smooth user experience.
- Uses **LangChain's Groq API** for SQL generation.

---

## Installation

### **1. Clone the repository**
```sh
git clone https://github.com/your-username/text-to-sql-app.git
cd text-to-sql-app
```

### **2. Create a Virtual Environment (Optional but Recommended)**
```sh
python -m venv venv
source venv/bin/activate   # On macOS/Linux
venv\Scripts\activate      # On Windows
```

### **3. Install Dependencies**
```sh
pip install -r requirements.txt
```

---

## Environment Variables
Create a `.env` file in the root directory and add your **Groq API key**:
```sh
GROQ_API_KEY=your_groq_api_key_here
```
Or set it in your terminal:
```sh
export GROQ_API_KEY=your_groq_api_key_here  # macOS/Linux
set GROQ_API_KEY=your_groq_api_key_here     # Windows
```

---

## Running the Application

### **1. Initialize the Database**
Before running the app, execute the following Python script to **create the SQLite database and insert sample data**:
```sh
python setup_database.py
```

### **2. Start the Streamlit App**
```sh
streamlit run app.py
```

This will open the app in your web browser.

---

## File Structure
```
text-to-sql-app/
│── app.py               # Main Streamlit App
│── setup_database.py    # Creates and populates the SQLite database
│── requirements.txt     # Python dependencies
│── .env                 # Environment variables (API key)
│── README.md            # Project documentation
```

---

## Example Queries
| Natural Language Query | Generated SQL Query |
|------------------------|----------------------|
| How many students are there? | `SELECT COUNT(*) FROM STUDENT;` |
| Show all students in Data Science. | `SELECT * FROM STUDENT WHERE COURSE='Data Science';` |
| What are the marks of Student1? | `SELECT MARKS FROM STUDENT WHERE NAME='Student1';` |

---

## License
This project is licensed under the **MIT License**.

---

## Author
Developed by **Khizar Hussain(Refered by Online)**

---

## Contributing
Feel free to fork this repository and submit pull requests with improvements! 🚀
