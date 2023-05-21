# Streaming Database 🎥🍿

<p align="center">
    <a href="https://github.com/stephaniearismendi/Streaming-Database/actions/workflows/test.js.yml">
        <img alt="Tests" src="https://github.com/stephaniearismendi/Streaming-Database/actions/workflows/test.js.yml/badge.svg">
    </a>
    <a href='https://coveralls.io/github/stephaniearismendi/Streaming-Database?branch=main'>
        <img src='https://coveralls.io/repos/github/stephaniearismendi/Streaming-Database/badge.svg?branch=main' alt='Coverage Status' /></a>
</p>


This project is a database of movies and series from streaming platforms that can be queried through a REST API. The goal is to make it easy to access information about the content available on different streaming platforms such as Netflix, HBO, Amazon Prime Video, etc.

## Features

- The database contains information about more than 10,000 movies and series of different genres, languages and countries.
- The REST API allows you to query by title, year, genre, platform, rating, etc.
- The REST API returns the results in JSON format with the relevant data of each movie or series.
- The database and the API run on a Node.js server with Express.js and MongoDB.

## Installation

To install and run this project on your local machine, you need to have Node.js, npm and MongoDB installed. Then, follow these steps:

1. Clone this repository on your local machine using the command `git clone https://github.com/stephaniearismendi/Streaming-Database.git`.
2. Enter the project folder using the command `cd Streaming-Database`.
3. Install the project dependencies using the command `npm install`.
4. Start the server using the command `npm start`.
5. You can now access the API at `http://localhost:3000/api`.

## Usage

To use the API, you can make HTTP requests to different routes depending on what you want to query. For example, the route `/api/movies` returns all the movies in the database, and the route `/api/movies/:id` returns the movie with the specified id. There are also routes for series and for filtering by different criteria. You can see the file `server.js` to see all the available routes and how the requests are handled.

Here are some examples of how to use the API with curl:

- To get all the movies in the database:

```bash
curl http://localhost:3000/api/movies
```

- To get a specific movie by id:

```bash
curl http://localhost:3000/api/movies/60a7c9b6f8c6a9d9f8f4d4e1
```

- To get all the movies from Netflix:

```bash
curl http://localhost:3000/api/movies?platform=Netflix
```

- To get all the series with a rating higher than 8:

```bash
curl http://localhost:3000/api/series?rating[gte]=8
```

You can also use tools like Postman or Insomnia to test the API more easily.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

