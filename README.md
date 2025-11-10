# Flask API Overview

## Endpoints
  - `GET /hello`: returns a JSON greeting payload `{"message": "Hello, World!"}` 
  - `POST /echo`: accepts any JSON body and echoes it back with a `201 Created` response, allowing you to verify request handling.

## Tests
  - `test_app.py` contains two pytest tests that tests both routes using Flask's test client, ensuring the responses match the expected status codes and payloads.

## Issues
I had some issues with the implementation: 
- the Linting tests failed the first time, I had to modify both app.py and test_app.py file to pass the tests
- the CodeQL failed multiple times. I had to allow the github actions to both read and write in the settings for it to work. I also had to change the version to v2 because it kept giving me errors that v1 was depracated
- In the test.yml file, I had to change the python-version: [3.10, 3.11, 3.12] because it wasn't working. All I had to do was wrap the floats in quotes for it to work

GitHub Repository Link: https://github.com/Abdullah-Mohammed-OTU/AdvWebDev_Activity8