<h1>RandomIdeas App</h1>

This is a fullstack application for sharing random ideas. It is a project in my Modern JS From The Beginning course.

This app includes a Node.js/Express REST API that uses MongoDB for a database. The client-side is built with Webpack.

![alt text](https://github.com/bradtraversy/randomideas-app/blob/main/assets/screen.png)

<h2>Usage</h2>

Install Dependencies
Install dependencies on the front-end and back-end

```bash
npm install
cd client
npm install
```

<h2>Back-end/Express Server</h2>

```bash
npm start
```
or

```bash
npm run dev (Nodemon)
```

Visit http://localhost:5000

<h2>Front-end/Webpack Dev Server</h2>  

```bash
cd client
npm run dev
```
Visit http://localhost:3000

To build front-end production files

```bash
cd client
npm run build
```

The production build will be put into the public folder, which is the Express static folder.

<h2>Environment Variables</h2>

Rename .env-example to .env and add your MongoDB URI to the .env file.

```bash
MONGO_URI=your_mongodb_uri
```

<h2>REST Endpoints</h2>

<h3>Ideas</h3>

| Endpoint |	Description |	Method |	Body |
| --- | --- | --- | --- |
| /api/ideas |	Get all ideas |	GET |	None |
| /api/ideas/:id |	Get idea by id |	GET |	None |
| /api/ideas |	Add idea |	POST |	{ text, tag, username } |
| /api/ideas/:id |	Update idea |	PUT |	{ text, tag, username } |
| /api/ideas/:id |	Delete idea | DELETE |	username |

When updating or deleting, the username must match the username of the idea creator.
