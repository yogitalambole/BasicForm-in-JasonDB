# JsonPowerDB

## "This project is all about basics of JsonPowerDB (JPDB) and how to use JPDB for CRUD operations." 

### About JsonPowerDB:

- JsonPowerDB is a Real-time, High Performance, Lightweight and Simple to Use, Rest API based Multi-mode DBMS. JsonPowerDB has ready to use API for Json document DB, RDBMS, Key-value DB, GeoSpatial DB and Time Series DB functionality. JPDB supports and advocates for true serverless and pluggable API development.

### Benefits of using JsonPowerDB

- Simplest way to retrieve data in a JSON format.
- Schema-free, Simple to use, Nimble and In-Memory database.
- It is built on top of one of the fastest and real-time data indexing engine - PowerIndeX.
- It is low level (raw) form of data and is also human readable.
- It helps developers in faster coding, in-turn reduces development cost.

## Release History
1. Generate Token - JsonPowerDB
2. Add Chrome Extension - Talend API Tester
3. Use commands - PUT, GET, UPDATE, REMOVE.
4. Use JsonPowerDB in Webpage
5. Create Html form
6. Add script - FormValidation
7. Add script - function of PUT, GET, UPDATE, REMOVE.

## Illustrations
JsonPowerDB is a Database Server with Developer friendly REST API services. It's a High Performance, Light Weight, Ajax Enabled, Serverless, Simple to Use, Real-time Database. Easy and fast to develop database applications without using any server side programming / scripting or without installing any kind of database.
Whether it's a Dynamic Website or a Mobile App or some Data Analytics Portal, the development is real fun and fast. Nothing better than trying it yourself. What all you need is a basic understanding of HTML, CSS, Bootstrap, and Javascript.

## Scope of Functinalities
- Minimum Development Cost
- Minimum Time to Market
- Minimize the complexity of interoperability of different applications
- Maximum data processing performance
- Technology Futuristic
	- Fills gap from database to big-data
	- Pluggable with new algorithms
	- Pluggable and user defined API
- Minimize Total Cost of Ownership

## Examples of use
- Any software application that needs backend database
	- Dynamic web applications/Mobile/Desktop Apps
- All RDBMS Use-cases
- All Document DB Use-cases
- All Key-Value DB Use-cases
- Use-cases that needs GeoSpatial/Time-series Analytics
- Best suited to real-time application for data analytics
- Improve existing application reporting / analytics performance
- Live working HTMl templates

## Project status

### Dashboard:

![Dashboard](https://github.com/yogitalambole/BasicForm-in-JasonDB/blob/main/JPDB/dashboard.png)

### Web form with functional buttons :

![form](https://github.com/yogitalambole/BasicForm-in-JasonDB/blob/main/JPDB/form.png)

### Table of contents:

![Index Page](https://github.com/yogitalambole/BasicForm-in-JasonDB/blob/main/JPDB/index.png)

### Competitive Landscape
|Feature| MongoDB | MySQL | Redis | HBase | Influx DB | JasonPowerDB |
|--|--|--|--|--|--|--|
| Document DB | ✔️ | ❌ | ❌ | ❌ | ❌ | ✔️ |
| Key-Value DB | ❌ | ❌ | ✔️ | ❌ | ❌ | ✔️ |
| RDBMS | ❌ | ✔️ | ❌ | ❌ | ❌ | ✔️* |
| GeoSpatial | ❌ | ❌ | ✔️ | ❌ | ❌ | ✔️ |
| Time Series DB | ❌ | ❌ | ❌ | ❌ | ✔️ | ✔️ |
| Wide Column Stores | ❌ | ❌ | ❌ | ✔️ | ❌ | ✔️* |

## Features
-Nimble, simple to use, in memory, real time.
-Schema free - easy to maintain.
-Serverless support - fast development - cuts time to market.
-Built around the world's fastest indexing engine PowerIndex.
-Webservices API - Low Dev Cost.
-Multiple Security Layers.
-A single instance - Million Indexes.

## Basic commands

### Insert Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "PUT",
		<<"dbName": <"database-name">,>>
		<<"rel": <"relation-name">,>>
		<<"colsAutoIndex": <boolean-value>,>>
		<<"templateStr": <jsonTemplateStr>,>>
		"jsonStr": <jsonDataStr>
	}
	```
- Code Sample
	```
	{
		"token": "608862679|6881615562961411263|608862579",
		"cmd": "PUT",
		"dbName": "StudentDB",
		"rel": "student",
		"jsonStr": {
			"name": "user",
			"email": "user@gmail.com"
		}
	}
	```
- Demo
![Demo of Insert Command](/images/gif/insert.gif)


### Retrieve Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/irl 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "GET",
		"dbName": <"database-name">,
		"rel": <"relation-name">,
		"jsonStr": {
			<"ColumnName":"JsonValue">
    	}
	}
	```
- Code Sample
	```
	{
		"token": "608862679|6881615562961411263|608862579",
		"cmd": "GET",
		"dbName": "StudentDB",
		"rel": "student",
		"jsonStr": {
			"name": "user"
		}
	}
	```
- Demo
![Demo of Insert Command](/images/gif/retrieve.gif)


### Update Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "UPDATE",
		"dbName": <"database-name">,
		"rel": <"relation-name">,
		"jsonStr": {
			<"recordNo">: {
				<"ColumnName": "NewJsonValue">|<"New-ColumnName": "New-Column-Value">
			}
		}
	}
	```
- Code Sample
	```
	{
		"token": "90937075|-31948812362179105|90938333",
		"cmd": "UPDATE",
		"dbName": "StudentDB",
		"rel": "student",
		"jsonStr": {
			"2":{
				"name": "Test Student",
				"email":"teststudent@gmail.com",
				"mobile": 7098162348
			}
		}
	}
	```
- Demo
![Demo of Insert Command](/images/gif/update.gif)


### Remove Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "REMOVE",
		"dbName": <"database-name">,
		"rel": <"relation-name">,
		"record": <record_number | [recNo1, recNo2....]>
	}
	```
- Code Sample
	```
	{
		"token": "401400726|-363956312424328770|401400726",
		"cmd": "REMOVE",
		"dbName": "StudentDB",
		"rel": "student",
		"record": 1
	}
	```
- Demo
![Demo of Insert Command](/images/gif/remove.gif)
