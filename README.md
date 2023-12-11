
# POC RabbitMQ

## First step Installation 

Install Docker for RabbitMQ and Mysql 

```bash
docker-compose up -d --build
```

and 

```bash
npm install
```

## Config Database in file consumer.js
for sample use Database name is Test and Table name is Orders


```javascript
const connection = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "rootpassword",
  database: "Test",
});
```

## Next step Run Consumer. 

```bash
node consumer.js
```

## Next step Run producer for test insert data in table. 

```bash
node producer.js
```

## Check queues in RabbitMQ Broker 

http://localhost:15672

username : test

password : password


