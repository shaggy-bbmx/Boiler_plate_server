# Boiler_plate_server
This is boiler plate code for setting up server in node js:----------------------------------------
Type following command in cli
-----------------------------------------------------------------
npm init
npm i express
npm i body-parser
npm i mongodb@5.0
npm i ejs
npm i mongoose
--------------------------------------------------------------------

Copy paste following code in app.js
----------------------------------------------------------------
const express = require("express");
const app = express();
const bodyParser = require("body-parser");
const ejs = require("ejs");
const mongoose=require("mongoose");


app.set('view engine', 'ejs');
app.use(bodyParser.urlencoded({extended: true}));
app.listen(3000, function() {
    console.log("Server started on port 3000");
});

app.get("/",(req,res)=>{
    res.send("sgaar");
});
