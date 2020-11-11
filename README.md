# URL SHORTENER
This is a simple URL Shortener implementated in django and graphene(GraphQL for Python).


**Installation**

1. Clone the Repo:-

  ```git clone https://github.com/ashish493/url_shortener```

2. Install the dependencies:-

  ```pip install -r requirements.txt```

3. Run the flask server in the app directory:-

  ```python manage.py runserver```

4. Open ```http://localhost:8000/graphql``` in your web browser.

Once the server is running our API, we can send the queries through the graphql API in the form as shown.


```
mutation {
  createUrl(fullUrl:"https://summerofcode.withgoogle.com/archive/2020/projects/5699259774533632/") {
    url {
      id
      fullUrl
      urlHash
      clicks
      createdAt
    }
  }
}
```

The API is designed to take the input url along with some other parameters. It will then convert the url into hashes using MD5 Hash and then store the links in the database.

However, MD5 Hash is not recommend for use in the production servers because of the [MD5 Collision Vulnerability](https://en.wikipedia.org/wiki/MD5#Collision_vulnerabilities).

Since, it is a fully backend oriented project, I haven't created any type of frontend for this project. If anyone is interested in creating and contributing one, feel free to make a pull request. 


## Acknowledgement

I have used some of code snippets from the official docs of [graphene-python](https://docs.graphene-python.org/projects/django/en/latest/installation/#csrf-exempt)



