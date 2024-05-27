# Stocks Portfolio Management Application

Note: The project uses Lombok. 
Please install the Lombok plugin. **In IntelliJ: File->Settings...->Plugins - search 'Lombok'**



Implement a basic stock portfolio tracker application starting from the example provided in package.

The aplication should provide following functionalities:
- Authentication (Login) - finish the login implementation. Currently, the credentials are not verified; anyone can access the application.

![login image](./docs/login.png)

- View market stocks and their current value - this feature is implemented and can be used as reference for next exercises;

![market image](./docs/market.png)

- View user portofolio owned stocks
    - View owned stocks in a table view similar to Market;
    - For each owned stock display in table followings: symbol, quantity, price per unit, total price of the position;
    - Also add available funds (cash).

![portfolio image](./docs/portfolio.png)

- Buy stock:
    - Implement "Buy" button functionality;
    - Buy is limited by available cache funds (stored in Portfolio class, attribute "cash");

![buy image](./docs/buy.png)

- Sell stock
    - Create user interface similar to Buy interface
    - Symbol dropdown button should display only stocks owned by user;
    - When the sell is completed, the available funds should increase with the value of the transaction;

![sell image](./docs/sell.png)
 

### Implementation notes

Note 1 - Stock symbols are hardcoded in StockMarketQueryService      private String[] symbols = new String[] {"INTC", "BABA", "TSLA", "AIR.PA", "MSFT", "AAPL", etc.}; You can add your own symbol as long as correspond to some real market symbols.

Note 2 - For getting financial market information the application use https://financequotes-api.com/ library:

        <dependency>
            <groupId>com.yahoofinance-api</groupId>
            <artifactId>YahooFinanceAPI</artifactId>
            <version>3.15.0</version>
        </dependency>

## Create UML Class diagram and insert it bellow.

----- UML CLASS DIAGRAM -------
![Alt Text](https://raw.githubusercontent.com/arianacasandra/Java/main/Stocks%20Portfolio%20Management%20Application/ex2.jpg)

Add a layer of persistence to your application:
- Save the accounts in a file on the disk.
- Save the user's portfolios on the disk. Keep in mind that you can have multiple users.
- You can use either Java's native serialization support or the JSON format.
