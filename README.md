# Stock Tracker

## Server Side
**The REST API was built with ASP .NET Core WebAPI and uses MS SQL Server to store data.
This API is meant to pair with a React client to allow users to track their favorite stocks with up to date information
and make comments about those stocks for future reference.**

**Installation and Setup**
1. Make sure you have ASP .NET 8 installed and work with this command ```dotnet --version```.
2. Make sure you have MS SQL Server and SQL Server Management Studio downloaded.
3. Clone this repository with ```git clone```, and navigate to the server file of this project.
4. Navigate into SQL Server and create a database table with the name ```finshark```:
   ![image](https://github.com/sunnypatel314/StockTracker/assets/110628037/3540053b-1c84-4662-846b-cec5df8600e7)
5. Copy your devices name by right clicking the database and selecting ```Properties```:
   ![image](https://github.com/sunnypatel314/StockTracker/assets/110628037/818a56a2-7bca-4325-a53f-5b7691e050ca)
6. Go into the ```appsettings.json``` in the root directory and change the device name.
   Replace '''LAPTOP-8EL6DSJK''' with your device name:
   ![image](https://github.com/sunnypatel314/StockTracker/assets/110628037/91d78323-bcf4-4e31-a5fa-89fcadbfa64a)
7. In the command line, make sure you are in the root of the project and run ```dotnet restore```.
   This will install all dependencies needed for this project.
8. Next, run ```dotnet watch run```. This will launch the API at this url : ```http://localhost:5290/swagger/index.html```.
   This project uses Swagger to test APIs, and perform Create, Read, Update, and Delete operations.

Endpoints: 
1. ```api/stock``` (GET): Returns all stocks in "Stocks" table with the constraints of the query object.
2. ```api/stock/{id:int}``` (GET) Returns a particular stock given its ID.
3. ```api/stock``` (POST): Creates a stock based on input value given (Symbol, Company Name, Purchase, LastDiv, Industry, and Market Cap).
4. ```api/stock/{id:int}``` (PUT): Updates a stock based on its ID and an input given (Symbol, Company Name, Purchase, LastDiv, Industry, and Market Cap).
5. ```api/stock/{id:int}``` (DELETE): Deletes a stock based on the ID given.
6. ```api/comment``` (GET): Returns all comments.
7. ```api/comment/{id:int}``` (GET): Returns the comment with the given ID.
8. ```api/comment/{stockId:int}``` (POST): Creates a comment given the ID of the stock it belongs under, and given the body of the comment (Title, Content).
9. ```api/comment/{id:int}``` (PUT): Updates a comment based on its given ID, and a body of the comment (Title, Content).
10. ```api/comment/{id:int}``` (DELETE): Deletes a comment based on its given ID.



    

