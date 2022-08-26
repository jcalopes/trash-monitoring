# TrashTalker


:articulated_lorry: Trash Monitoring System   :articulated_lorry:

## **Description**


This project aims to manage the level of trash in each container placed all over the cities. The data coming from distance sensores installed in each container is used to manage the existing trash rgarding a zone, city or even bigger place. This information is transformed and offered in dashboard to the end-user supporting the decision making. 
It also try to optimize the routes carried out by trucks to collect trush by giving smart routes avoiding them to do useless extra miles in places. We can save costs and time and ultimately save our planet as well.



## **How to configure**

To execute properly the project you need perfomr the following steps:
1. Check the connection string used at (Backend/TrashTalker/appSettings.Development.json):  
    `"DBConnection": "Server=localhost;Database=trashTalker;User=sa;Password=MyPass@word"`
2. Start a container with mysql image with the folowing properties:  
    `docker run -e "ACCEPT_EULA=1" -e "MSSQL_SA_PASSWORD=MyPass@word" -e "MSSQL_USER=sa" -p 1433:1433 -d --name=sql mcr.microsoft.com/mssql/server:2019-latest`
3. Override the credentials placed at config.cs. Probably you will have to configured some account regarding Arduino Cloud, Google API and so forth.
4. Start the container: `docker start sql`
5. Start backend project: `dotnet build` e `dotnet run`. Here you need to have installed .NET.
6. Install dependencies and start frontedn application: `npm install` e deseguida `npm start`
  

## **Tech Stack**

* **Angular** - Frontend Framework.
* **.NET** - Backedn Framework.
* **SQL** - SQL Databses,
* **Arduino IOT Cloud** - Cloud Service provided by Arduino to manage IOT Devices.


## **Team**


* João Lopes
* Tiago Leite
* João Bragança
* Micael Sampaio
* Flávio Costa




