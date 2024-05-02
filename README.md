1. Clone the repository

```bash
$ git clone https://github.com/Ranjithr-007/Task-Api.git
```
  2. Install the requirements

```bash
$ pip install -r requirements.txt
```
  3. Run migration

```bash
$ python manage.py migrate
```

  4. Run the server

```bash
$ python manage.py runserver
```

## API Endpoints

The following API endpoints are available for managing tasks:

### 1. Create a Task

- **URL**: ``
- **Method**: POST
- **Parameters**: None
- **Request Body**:

  ```json
  {
    "owner": "<int>"
    "title": "Task Title",
    "description": "Task Description"
  }
  ```

- **Response**:

  - Status: 201 CREATED
  - Body:

    ```json
    {
      "owner": "1"
      "title": "Task Title",
      "description": "Task Description"
    }
    ```

### 2. Get All Tasks

- **URL**: ``
- **Method**: GET
- **Parameters**: None
- **Response**:

  - Status: 200 OK
  - Body:

    ```json
    [
      {
        "owner": "1"
        "title": "Task Title",
        "description": "Task Description"
      },
      ...
    ]
    ```

### 3. View a Task

- **URL**: `/tasks/<int:pk>/`
- **Method**: GET
- **Parameters**:
  - `pk`: The ID of the task
- **Response**:

  - Status: 200 OK
  - Body:

    ```json
    {
      "owner": "1"
      "title": "Task Title",
      "description": "Task Description"
    }
    ```

### 4. Update a Task

- **URL**: `/tasks/<int:pk>/`
- **Method**: PUT
- **Parameters**:
  - `pk`: The ID of the task
- **Request Body**:

  ```json
  {
    "owner": "1"
    "title": "Updated Task Title",
    "description": "Updated Task Description"
  }
  ```

- **Response**:

  - Status: 200 OK
  - Body:

    ```json
    {
      "owner": "1"
      "title": "Updated Task Title",
      "description": "Updated Task Description"
    }
    ```

### 5. Delete a Task

- **URL**: `/tasks/<int:pk>/`
- **Method**: DELETE
- **Parameters**:
  - `pk`: The ID of the task
- **Response**:

  - Status: 204 NO CONTENT
