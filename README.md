# Complete intro to SQL with Editor

[Complete intro to SQL](https://sql.holt.courses/) is one of the best SQL courses out there. Brian Holt is a great teacher.

The problem is it requires familiarity with node.js, Docker, and other services.

We have removed these dependencies by connecting the databases to a browser based code editor. You will be able to use this editor to query the database. This will help you focus on just learning SQL and avoid any other complexities.

We use [SQLPad's](https://github.com/sqlpad/sqlpad/tree/master) (legacy) web browser SQL code editor. Everything is already configured.

## Setup Instructions

### Prequisites
1. Install yarn. You can run this anywhere in Terminal
```
brew install -g yarn
```

2. Clone this repo
```
cd ~/tutorials/modern_university/
git clone https://github.com/Modern-University/sql-with-editor.git
```
### Initiate app
1. Move into the `initiate-app` directory if you aren't already in there:
```
cd ~/tutorials/modern_university/sql-with-editor/initiate/app
```

The first time you run this, make sure you are on a good internet connection.
The first time this runs, it will take about 3-5 minutes

2. Start the app!
```
docker-compose pull
docker-compose build
docker-compose up
```
You will see a lot of messages being logged to your terminal.

You will know everything is ready once the messages stop and the last one says something like this:
>app-db-1      | 2024-03-10 14:14:07.723 UTC [1] LOG:  database system is ready to accept connections

This means we are ready!

Visit http://localhost:3000 to get started!

The next time you start the app, it should be much faster and the last message will be something like:
> app-sqlpad-1  | {"level":30,"time":"2024-03-10T14:19:35.503Z","pid":1,"hostname":"sqlpad","name":"sqlpad-app","msg":"Welcome to SQLPad! Visit http://localhost:3000 to get started"}

## Reset
If we need to start over for any reason, we will need to reset everything.
```
docker-compose down -v
```
Afterwards, you can start at "Initiate App 2. Start the app!"

## License
MIT
