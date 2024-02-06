# Poll-Containerization
Containerize and define the deployment of a web poll application.

The application is composed of 5 elements: <br/>
- Poll, a Flask Python web application that gathers votes and push them into a Redis queue. <br/>
- A Redis queue, which holds the votes sent by the Poll application, awaiting for them to be 
consumed by the Worker. <br/>
- The Worker, a Java application which consumes the votes being in the Redis queue, and stores
them into a PostgreSQL database. <br/>
- A PostgreSQL database, which (persistently) stores the votes stored by the Worker. <br/>
- Result, a Node.js web application that fetches the votes from the database and displays result. <br/>

![image](https://github.com/loupmesquita/Poll-Containerization/assets/57537562/94dc6f41-4b6e-4d80-98b3-9fe311795953)


