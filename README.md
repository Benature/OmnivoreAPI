# OmnivoreQL: Omnivore API client for Python

![OmnivoreQL Icon](https://github.com/yazdipour/OmnivoreQL/assets/8194807/d51d462d-4f5a-4031-980e-1faa5ca3f6e0)

This is a Python client for the [Omnivore API](https://omnivore.app).

[![GitHub stars](https://img.shields.io/github/stars/yazdipour/omnivoreql.svg?style=social&label=Star)](https://github.com/yazdipour/omnivoreql/stargazers)
[![Github Sponsor](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/yazdipour)

[![Tests](https://github.com/yazdipour/OmnivoreQL/actions/workflows/test.yml/badge.svg)](https://github.com/yazdipour/OmnivoreQL/actions/workflows/test.yml)
[![PyPI version](https://badge.fury.io/py/omnivoreql.svg)](https://pypi.org/project/omnivoreql/)

## How to use

To use omnivoreql in your Python project, you can follow these steps:

Install the omnivoreql package using pip:

```bash
pip install omnivoreql
```

Import the package into your project and Create a new instance of the client:

```python
from omnivoreql import OmnivoreQL

omnivoreql_client = OmnivoreQL("your_api_token_here")
```

Use the methods of the OmnivoreQL class to interact with the Omnivore API. 

```python
profile = omnivoreql_client.get_profile()

result = omnivoreql_client.save_url("https://www.google.com")

articles = omnivoreql_client.get_articles()

username = profile['me']['profile']['username']
slug = articles['search']['edges'][0]['node']['slug']
articles = omnivoreql_client.get_article(username, slug)

labels = omnivoreql_client.get_labels()
subscriptions = omnivoreql_client.get_subscriptions()
```

## Contributing

* If you want to contribute to this project, you can follow steps in [CONTRIBUTING.md](CONTRIBUTING.md) file.
* Main Omnivore graphql schema is in [schema.graphql](https://github.com/omnivore-app/omnivore/blob/main/packages/api/src/schema.ts) file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.