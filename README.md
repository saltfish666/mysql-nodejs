mysql - nodejs 学习笔记

## 操作
[Imgur](https://i.imgur.com/Z3Bo79I.png)
[Imgur](https://i.imgur.com/EXUeDCu.png)
```
const mysql  = require('mysql');  
 
const connection = mysql.createConnection({     
  host     : 'localhost',             
  port     : '3306',                   
  database : 'danci', 
  user     : 'root',              
  password : '926443', 
}); 

let sql = 'show tables';
connection.query(sql,function (err, result) {
    if(err){
      console.log('[SELECT ERROR] - ',err.message);
      return;
    }
    console.log(result)
});

sql = 'select * from know';
connection.query(sql,function (err, result) {
    if(err){
      console.log('[SELECT ERROR] - ',err.message);
      return;
    }
    console.log(result)
});

sql = 'select * from know';
connection.query(sql,function (err, result) {
    if(err){
      console.log('[SELECT ERROR] - ',err.message);
      return;
    }
    console.log(result)
});

sql = 'INSERT INTO  know (danci,mean) VALUES("fire","火")';
connection.query(sql,function (err, result) {
    if(err){
      console.log('[SELECT ERROR] - ',err.message);
      return;
    }
    console.log(result)
});
```
