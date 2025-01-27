# NodeJs
### Nodemon
- It is one of the devdependencies for the backend it will automatically restart our local server whenever it detect the changes we did not do manually.
```js
require('dotenv').config();

const express = require('express');
const expressLayout = require('express-ejs-layouts');

const app = express();
const PORT = 7000 || process.env.PORT;

app.use(express.static('public'));
// Templating Engine
app.use(expressLayout);
app.set('layout','./layouts/main');
app.set('view engine','ejs');

app.get('',(req,res)=>{
    res.send("hello World");
});


app.listen(PORT,()=>{
    console.log(`App listening onport ${PORT}`);
});
```
- In the package.json file all the needed dependencies are installed like dotenv, express, ejs, express-layout, etc...
- Then in the script section add the dev as the nodemon app.js
- so we run using the command like "npm run dev".
- require means we get all the needed modules.
- Loads environment variables from a .env file into process.env. Useful for managing sensitive information like API keys.
- in our case .env containe package.json
- Then we get express and expresslayout.
