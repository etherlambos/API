# API
**Etherlambos API V 0.1**
----
  <_Returns data about an Etherlambo. Returns model, location of graphics and additional information in order for a third party to properly display the Etherlambo._>

* **URL**

  <_API/getlambo.php_>

* **Method:**
  
  <_The request type_>

  `GET`
  
*  **URL Params**


   **Required:**
 
   `id=[integer]`


* **Data Params**

  <_None_>

* **Success Response:**
  
  <_"status" : "ok" - everything worked well_>
    
    **Content:** 	`{"status":"ok","model":4,"serialno":12,"name":"Charlie","base":"svg-charlie\/charlie_base.png","options":["svg-charlie\/charlie_frontsplitter.png","svg-charlie\/charlie_rearwing.png","svg-charlie\/charlie_frontlips.png"],"display":["front","back","front"],"path":"http:\/\/www.etherlambos.io\/"}`
 
* **Error Response:**

	 <_"status" : "some error occurred" - 
	Customizations & Serial No could not be retrieved. 
	While requesting data from the next node some timeout error occurred. The fields
	"model", "base" as well as "options" & "display" provide the correct base information regarding this lambo._>

    **Content:** `{"status":"some error 	occurred.","model":2,"serialno":0,"name":"Satoshi","base":"svg-satoshi\/satoshi_base.png","options":["svg-satoshi\/satoshi_rearwing.png"	],"display":["back"],"path":"http:\/\/www.etherlambos.io\/"}`

  OR

 	<_"status" : "lambo not found." - id of lambo does not exist_>

    **Content:** `{"status":"lambo not 	found.","model":0,"serialno":0,"name":"","base":"","options":[],"display":[],"path":"http:\/\/www.etherlambos.io\/"}`

* **Sample Call:**

    http://etherlambos.io/API/getlambo.php?id=214

* **Token Metadata:**

* "model": 
`represents the base model of the Etherlambo. For example 1 would be model Vitalik, 2 would be model Satoshi.`
* "serialno": `represents the unique serial number of each lambo model. Model Satoshi has for example a limited supply of 100 tokens. Every token has its own unique serial number reaching from 1 - 100. The same goes for other models.`
* "name": `represents the name of the model.` 
* "base": `path of the model base graphic.`
* "options": `contains the path to the corresponding graphics regarding base and customized options.`
* "display": `contains information on how to properly put the graphics together (e.g. via svg).`
`front means - in front of the base graphic
back means - behind the base graphic
Other than that no specific order needs to be considered when putting together the graphics.`
* "path": `base URL for retrieving graphics.`
