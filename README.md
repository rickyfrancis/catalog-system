# catalog-system

A catalogue application for recording and searching entries, built for a
university office. Users sign in, add entries, then search and page through them.

Written in 2021 and 2022.

## What it does

- Create, edit and view catalogue entries
- Search entries, with paging through the results
- Register an account, with the address confirmed by an emailed link
- Reset a forgotten password by email, using a verification code before setting
  a new one

## Stack

| Area | Choice |
| --- | --- |
| Frontend | React, Redux, React Bootstrap |
| Backend | Node.js, Express |
| Database | MongoDB with Mongoose |
| Auth | JSON Web Tokens, bcrypt for hashing |
| Validation | Joi |
| Email | Nodemailer |
| Security headers | Helmet |

## Layout

```
client/          React app
models/          Mongoose models: User and Entry
routes/api/      auth, users and entries endpoints
server-catalog.js  Express server
api-requests/    .rest files for trying the endpoints by hand
```

The `api-requests/` folder holds request files for the REST Client editor
extension, which is how the endpoints were tested during development.

## Running it locally

```bash
npm install
cd client && npm install && cd ..
```

Create a `.env` file in the project root with your MongoDB connection string, a
JWT secret, and SMTP credentials for the account and password emails.

Then start both halves:

```bash
npm run dev
```

## Status

Delivered and no longer maintained.
