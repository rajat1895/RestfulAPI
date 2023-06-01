# Basic Arithmetic API with Flask and Flask-RESTful

This API has endpoints for performing basic arithmetic operations including addition, subtraction, multiplication, and division. The codebase is built on Flask, a micro web framework written in Python, and uses the Flask-RESTful extension for quickly building REST APIs.

## Installation

Ensure that you have Python 3.6 or later installed on your system. You can download Python from [here](https://www.python.org/downloads/).

To run this project, you need to install the required dependencies. Install them with:

```bash
pip install flask flask-restful

## API Usage

The API has the following endpoints:

- `POST /add`: This endpoint receives a JSON object with two keys: `x` and `y` (both integers). It adds the two numbers together and returns the result. An example of a valid request body is:

    ```json
    {
        "x": 5,
        "y": 3
    }
    ```

- `POST /subtract`: This endpoint receives a JSON object with two keys: `x` and `y` (both integers). It subtracts `y` from `x` and returns the result. An example of a valid request body is:

    ```json
    {
        "x": 5,
        "y": 3
    }
    ```

- `POST /multiply`: This endpoint receives a JSON object with two keys: `x` and `y` (both integers). It multiplies `x` by `y` and returns the result. An example of a valid request body is:

    ```json
    {
        "x": 5,
        "y": 3
    }
    ```

- `POST /division`: This endpoint receives a JSON object with two keys: `x` and `y` (both integers). It divides `x` by `y` and returns the result. If `y` is 0, it returns an error. An example of a valid request body is:

    ```json
    {
        "x": 5,
        "y": 3
    }
    ```
    
Each endpoint checks if `x` and `y` are included in the posted data, and returns a status code indicating the result of the operation. The status codes are as follows:

- 200: Successful operation
- 301: `x` or `y` is not in the posted data
- 302: `y` is 0 during a division operation

