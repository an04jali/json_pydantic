# JSON Information Extraction using Groq + Pydantic

Extract structured information from unstructured text using the **Groq LLM API** and **Pydantic**. This project demonstrates how to convert natural language into validated JSON objects with the help of a schema.

## 🚀 Features

- Extracts structured information from customer tickets.
- Uses **Groq Llama 3.3 70B Versatile** model.
- Enforces a predefined JSON schema using **Pydantic**.
- Parses and validates the generated JSON.
- Easily extensible for resumes, invoices, forms, and documents.

## 🛠️ Tech Stack

- Python
- Groq API
- Pydantic
- python-dotenv
- JSON

## 📂 Project Structure

```
.
├── json_pydantic.py
├── .env
├── .gitignore
└── README.md
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/an04jali/json_pydantic.git
cd json_pydantic
```

Install dependencies:

```bash
pip install -r requirements.txt
```

or

```bash
pip install groq python-dotenv pydantic
```

## 🔑 Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
```

> **Note:** Never commit your `.env` file to GitHub.

## ▶️ Run

```bash
python json_pydantic.py
```

## 📌 Example Input

```text
Hello My name is Pratyush.

Yesterday I broke up with my girlfriend.

I have an iPhone which is not working.

My email is abc@gmail.com.
```

## 📌 Example Output

```json
{
  "name": "Pratyush",
  "email": "abc@gmail.com",
  "issue": "iPhone not working"
}
```

## 🧠 How It Works

1. Define a schema using **Pydantic**.
2. Convert the schema into JSON Schema.
3. Pass the schema to the Groq LLM through the system prompt.
4. Ask the model to return only JSON.
5. Parse the JSON response.
6. Validate it using the Pydantic model.


## 📚 Learning Outcomes

- Prompt Engineering
- Structured Output Generation
- Pydantic Schema Validation
- JSON Parsing
- Environment Variable Management
- Groq API Integration



## 📄 License

This project is for educational purposes.
