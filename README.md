## Setup

**Note:** For this exercise, we have provided an `.env` file with the database connection string. Normally, you would not commit this file to version control. We are doing it here for simplicity and given that we are using a local SQLite database.

## Migrations

Before running the migrations, we need to create a database. We can do this by running the following command:

```bash
npm run migrate:latest
```

## Running the server

In development mode:

```bash
npm run dev
```

In production mode:

```bash
npm run start
```

## Updating types

If you make changes to the database schema, you will need to update the types. You can do this by running the following command:

```bash
npm run generate-types
```

## Requirements

**Administrators should be able to:**

- **Screening**. create new viewing screenings for watching a movie that has a timestamp and a provided allocated number of tickets
- Optional requirement: delete viewing screenings while they are empty
- Optional requirement: change a screening's ticket allocation as long as it is not lower than the number of reserved tickets

**Users should be able to::**

- **Movie**. get a list of movies with their title and year by providing a list of their IDs (e.g., /movies?id=1,2,3)
- **Screening**. get a list of screenings available for booking. Screenings should include session information (timestamp, number of tickets, number of tickets left) and movie: (title and year).
- **Ticket**. get a list of bookings (tickets) they have booked
- **Ticket**. create a booking (ticket) for movie screening that has some tickets left

## Technical requirements

- User and administrator inputs should be validated.
- Database schema changes must be done using migrations.
- Application code should have unit and integration tests. 80% - 95% test coverage.
- Commits should follow the Conventional Commits standard.
