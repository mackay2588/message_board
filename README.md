
## Message Board Application
this is a simple message board application to practice the use of AngularJS and PostgreSQL

* Read **ALL** instructions before you start
* MUST use Angular and PostgreSQL
* Name your database: `message_board`
* Your Front End should have two inputs. One for the user's name, the other for the user's message. Additionally, there should be a submit button,
* When the submit button is clicked, you must send the name and message from the inputs to the server to be written to an SQL Database
* Once the message has been successfully written to the database, display all messages on the DOM,
* If the application page is reloaded, all previous messages should appear.

### Setup

Name your database: `message_board`

```SQL
CREATE TABLE "messages" (
  "id" serial primary key,
  "name" varchar(120),
  "message" varchar(240)
);

INSERT INTO "messages" ("name", "message")
VALUES ('Dane', 'The busses were really slow today!');
```


I did the tables differently 

CREATE TABLE "messages" (
	"id" SERIAL PRIMARY KEY not null,
	"message" VARCHAR(500) not null,
	"user_id" INT
);

CREATE TABLE "users" (
	"id" SERIAL PRIMARY KEY not null,
	"name" VARCHAR(255) not null
);
