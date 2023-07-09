- Create venv
    `python3 -m venv ./venv`
    `. venv/bin/activate`

- Add serverless-python-requirements
    `serverless plugin install -n serverless-python-requirements`

- Install pandas and numpy
    `pip3 install pandas numpy`
    `pip freeze > requirements.txt`

- Configure serverless.yml
    ```
    custom:
        pythonRequirements:
            dockerizePip: true
            slim: true
            zip: true
    ```
    ```
    package:
        exclude:
            - node_modules/**
            - venv/**
    ```