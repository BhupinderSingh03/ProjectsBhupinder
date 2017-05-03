# Shop API

##Technologies used: 
Java, Spring boot, Rest , Jpa repository, h2 in memory database, google api, Lombok plugin, mockito for junit, maven, jdk8, json. 

## how to start
1) Unzip the folder
2) Please use an IDE Eclipse or intellij for integrated development environment
3) Please Import this project as a maven project in to your IDE
4) Please build your project using maven ( clean install )
5) Please run Application.java file under package src/main/java/shops.ShopInfo
6) Application will initialize the h2 in memory database
7) Application is up now

I have exposed below three restful webServices: 
1) Adding the shop address
2) Get all addresses to see the saved addresss
3) Get the closest location address by their lattitude and longitude

## adding the shop address:
Please start adding addresses in to the in memory database using below Rest url and json Request. (Use postman or rest client to hit)    

post : http://localhost:1111/shop/store      
request:   {     "shopNumber": "1",     "shopName": "53453",     "shopAddresses":"Cusrow Baug Colony, Apollo Bandar, Colaba, Mumbai",     "postCode": "Maharashtra 400001"   } 


Please change the shopAddresses mentioned in above request to save the addresses with different lattitude and longitude.   Please keep changing the shopNumber in every adding request. Because its a primary key in h2 database. Otherwise previous address will get overridden by new one.


## Getting all the saved addresses:   Once you are done with adding the addresses in to the database. You can see all saved addresses with their latttude and longitude by hitting below url:  

Get : http://localhost:1111/shop/store  


## get the closest location address by their lattitude and longitude: Now you can get the closest location  by sending lattitude and longitude in query param.   Please hit below url with query param:  

Get : http://localhost:1111/shop/store?lat=24.9191775&lng=89.82895359999999


##  Description:
1) Spring boot application
2) used jpa repository to store the data in h2 database
3) Used Lombok to remove getter setter methods (@Setter @Getter). 
4) Used google api to get the lattitude and longitude of an address.
5) written the junit test cases using mockito
