# Support Tickets API

A simple RESTful API for managing support tickets, built with Node.js. This project demonstrates building a server from scratch using only native Node.js modules, without any external frameworks.

## Features

- **CRUD Operations:** Create, Read, Update, and Delete support tickets.
- **Status Filtering:** List tickets based on their status (e.g., `open`, `closed`).
- **File-based Database:** Uses a simple JSON file for data persistence.
- **Middleware Architecture:** Handles JSON parsing and request routing cleanly.
- **Dynamic Routing:** Supports routes with path parameters (e.g., `/tickets/:id`).

## Technologies Used

- [Node.js](https://nodejs.org/)

## Getting Started

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed on your machine.

### Installation & Running

1.  Clone the repository:

    ```sh
    git clone https://github.com/Batavoo/support-tickets
    cd support-tickets
    ```

2.  This project has no external dependencies, so there's no need to run `npm install`.

3.  Start the development server:
    ```sh
    npm run dev
    ```
    The server will start on `http://localhost:3333` and will automatically restart on file changes.

## API Endpoints

The base URL for all endpoints is `http://localhost:3333`.

| Method   | Path                   | Description                                   | Request Body (JSON)                                                         |
| :------- | :--------------------- | :-------------------------------------------- | :-------------------------------------------------------------------------- |
| `POST`   | `/tickets`             | Creates a new support ticket.                 | `{ "equipment": "string", "description": "string", "user_name": "string" }` |
| `GET`    | `/tickets`             | Lists all tickets.                            | N/A                                                                         |
| `GET`    | `/tickets?status=open` | Lists all tickets with a specific status.     | N/A                                                                         |
| `PUT`    | `/tickets/:id`         | Updates a ticket's equipment and description. | `{ "equipment": "string", "description": "string" }`                        |
| `PATCH`  | `/tickets/:id/close`   | Closes a ticket and adds a solution.          | `{ "solution": "string" }`                                                  |
| `DELETE` | `/tickets/:id`         | Deletes a ticket.                             | N/A                                                                         |
