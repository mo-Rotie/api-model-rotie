# mo-Rotie ML API

Team C241-PS264| Bangkit Capstone Project 2024

```markdown
# Prerequisites

Before running the application, make sure you have the following installed on your machine:

- [Python](https://www.python.org/)

# Tech We Use

- Flask
- Tensorflow
```

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/mo-Rotie/api-model-rotie.git
   ```

2. Navigate to the project directory:

   ```bash
   cd roti-api-ml
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

To start the Express.js server and run the database setup:

```bash
python main.js
```

## API Endpoints

### 1. Connect to Model

- **Method:** `POST`
- **Path:** `/`
- **Description:** endpoint for connect to model
- **Response Body:**
  ```json
  {
    "status": {
      "code": 200,
      "message": "Connected to mo-Rotie"
    }
  }
  ```

### 2. Predict mold on bread

- **Method:** `POST`
- **Path:** `/predict`
- **Description:** endpoint for predict mold on bread
- **Request Body (form-data):**
  ```form-data
    image = Image (*jpg/png/jpeg)
  ```
- **Response Body:**
  ```json
  {
    "status": {
      "code": 200,
      "data": {
        "classType": "Roti Tidak Berjamur",
        "percentage": 99
      },
      "message": "Success predicting"
    }
  }
  ```
- **Error Respone:**

  Error Invalid Format File

  ```json
  {
    "status": {
      "code": 400,
      "message": "Invalid file format. Please upload a JPG, JPEG, or PNG image."
    }
  }
  ```
