# XP-System

This school project is for my teacher to have students log in and check out their XP and assignments.
This website application is not available online, this is just a locally run website at our school.

For a full tutorial on website functionality check out `DOCUMENT.md`.

If you'd like to use this yourself, you'll need to create a teacher, it must be done by a site admin.

There is no default site admin so you will need to set one up.
To set up a site admin, you'll need to create the site admin in the database in a collection called users,
and insert a document via MongoDB Compass. Format the document as shown:
`{
  "role": "Admin",
  "name": your name,
  "email": your email,
  "password": your encrypted password
 }`

Replace `your name` with the name you specify, `your email` with the email you would like to use to login,
and replace `your encrypted password` with your [Encrypted Password](#Encrypting-Your-Password)

The ID for your admin document should be auto generated by MongoDB Compass when you `insert` the document.

### Requirements :
1.  [Node.js](https://nodejs.org/en/)
1.  [MongoDB](https://docs.mongodb.com/manual/administration/install-community/)

### Getting Started with Code  :
1. Set up [MongoDB](#Setting-up-MongoDB) on your computer.
2. Clone repo from https://github.com/Braeden57/XP-System.git
3. Run `npm install` to install dependencies.
4. Duplicate `.env.example` and rename the new file to `.env`. Edit to your configurations.
1. Run `npm start` to boot up server.
1. Go to http://localhost:8080. Or Whatever you set it to in the `.env` file.

### Setting up MongoDB
1. Install mongodb and follow the setup steps.
1. [Step by step instructions](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows)

### Accessing the Database
1. Locally this will use any db you set the DB_URI to in the `.env` file.
1. You can use MongoDB compass app to view the db and edit any information stored.
2. Or connect it to an external db by changing the DB_URI in the `.env` to your db key.

### Encrypting Your Password
1. To encrypt your password while creating the admin account. Go into the `config` folder,
1. follow the instructions in encrypt.js and run encrypt.js via node `node encrypt.js`
