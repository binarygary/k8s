# K8s microservice experiment

The intent of this is to create a bunch of microservice that can be deployed to a kubernetes cluster.

## Project structure
Generally, some services will run and pass updates into a message bus (redis streams).
Overkill, but a good way to play with kubernetes and microservices.

### TickerRetriever
A service that runs once a week and checks to see if there are new tickers to add to the database.

### TickerUpdater
Pretty general service that runs continually to update the ticker data.

### HistoryRetriever
A service that runs frequently to check for new history data to add to the database.

### RuleSetApplier
Somehow this will run and apply rulesets to the data.

### Admin
Used by Frontend to get data.

### StaticFrontend
A static frontend that will be used to display data.
