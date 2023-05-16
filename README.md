# Junior Backend Developer candidate test

## Intro

One of Apexlab's strategic partners, Olvasoegylet.io sent us a request for a book catalog application. They would like to have a public collection of books for their customers. You are the chosen one who may write POC (proof of concept) purely back-end (Node) JavaScript (Typescript) application which they could use to provide data for their various mobile application eg.: Book Renter.

## Technical guideline

### Generic

Please, pay attention to:

- Use English language (both readMe and code)
- Outlined, readable, clean code (not 1 file)
- Do not reinvent the wheel, you can use external libraries for whatever reason but make it simple
- As a test interface provide some kind of (graphql) playground
- Proper code formatting is more than welcome

### Business goal

As it is a POC (Proof of concept) we like to create an MVP (Minimum Viable Product) solution with the main functionalities. The app should be:

- Easy to consume
- Publicly available (no registration/authorization required, but deployed)
- Store data (in underlying database)
- Provide fast and reliable response on Book and Author requests
- Include mock data in the deployed app (seeding)
- Flexible (ready for future extensions)

### Functional requirements (tech. ACs)

#### Operations

- Required
  - CRUD operations on Books and Authors <em>(Create - Read - Update - Delete)</em>
    - Authors must be unique based on email
    - Books title and ISBN must be unique
  - Get Books grouped by Authors
- Optional <em>(bonus)</em>
  - Create Author with multiple Books
  - Get Author with their Books in a single request
  - Create Book with Multiple Authors
  - Introduce the Category model in Books
    - Get by category

#### Models:

- Required
  - Book
    - title <em>(string)</em>
    - author <em>(relation)</em>
    - description <em>(string)</em>
    - ISBN <em>(string)</em>
    - published <em>(boolean)</em>
  - Author
    - name <em>(string)</em>
    - email <em>(unique string)</em>
    - books <em>(relation)</em>
- Optional <em>(bonus)</em>
  - Category <em>(book category)</em>
    - name <em>(string)</em>
    - description <em>(string)</em>

### Tooling

The Council of Elder Architects decided to use the following tooling, but the rest is up to you.

- Required
  - Private git repository (with commit history)
  - Typescript, NodeJs v.16+
  - Dockerized database (recommended DB: postgreSQL, Docker is required)
  - Prisma ORM
  - GraphQL (with playground)
  - Your favorite Host service (Render, AWS, Heroku, Netlify, etc.)
- Recommendation
  - Apollo Server (with type-graphql)
  - Write tests

### Bonus

We know writing a homework/test is time consuming and tedious procedure but we highly recommend you to write efficient tests for your confidence (80% - 20%). Attaching a readMe file is also a good habit and useful for everyone who will see your code.

Git is our friend, don't be afraid to use it! And also, don't forget to remove your unused code, unnecessary comments, and console logs!

Happy Coding! 🚀
