# FastAPI API Test Automation

This project is a FastAPI-based web service that provides basic mathematical operations, along with automated API testing using Pytest and GitHub Actions.

## Features
- **FastAPI Server**: Provides endpoints for addition, subtraction, and multiplication.
- **Automated Testing**: Uses `pytest` for API test automation.
- **CI/CD Integration**: Automated tests run on GitHub Actions.

## Project Structure
```
📂 test_automation
├── 📂 .github/workflows        # GitHub Actions CI/CD workflow
│   ├── api-tests.yml           # API test automation workflow
├── 📂 venv                     # Virtual environment (ignored in Git)
├── apiserver.py                # FastAPI application
├── test_automation.py          # API test cases using pytest
├── test_automation_test.py     # Additional test cases
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

## Setup Instructions
### 1️⃣ Clone the Repository
```sh
git clone https://github.com/ritu-pixel/test_automation.git
cd test_automation
```

### 2️⃣ Create and Activate Virtual Environment
```sh
python -m venv venv  # Create virtual environment
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate  # Windows
```

### 3️⃣ Install Dependencies
```sh
pip install -r requirements.txt
```

### 4️⃣ Run FastAPI Server
```sh
uvicorn apiserver:app --host 0.0.0.0 --port 8000 --reload
```
- Visit API docs at: [http://localhost:8000/docs](http://localhost:8000/docs)

### 5️⃣ Run Pytest Locally
```sh
pytest -v
```

## GitHub Actions - Automated Testing
- The `.github/workflows/api-tests.yml` file defines a workflow that runs tests automatically on every push or pull request.
- Check the status of workflows under the **Actions** tab in GitHub.

## API Endpoints
| Method | Endpoint           | Description        |
|--------|------------------|--------------------|
| GET    | `/`              | Welcome message   |
| GET    | `/add/{a}/{b}`    | Add two numbers   |
| GET    | `/subtract/{a}/{b}` | Subtract numbers |
| GET    | `/multiply/{a}/{b}` | Multiply numbers |

## Contributing
1. Fork the repository
2. Create a new branch: `git checkout -b feature-branch`
3. Commit changes: `git commit -m 'Add new feature'`
4. Push to GitHub: `git push origin feature-branch`
5. Open a pull request 🚀

## License
This project is licensed under the MIT License.

---
**Author:** [Ritu Rajput](https://github.com/ritu-pixel)

