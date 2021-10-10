# API
**Etherlambos API V 0.2**
----
  <_Returns data about an Etherlambo. Returns model, location of graphics and additional information in order for a third party to properly display the Etherlambo._>

* **URL**

  <_API/lambo/_>

* **Method:**
  
  <_The request type_>

  `GET`
  
*  **URL Params**


   **Required:**
 
   `id/[integer]`


* **Data Params**

  <_None_>

* **Content:** 	`{
    "attributes": [
        {
            "trait_type": "Upgrade No.:1",
            "value": "Modified exhaust system Race"
        },
        {
            "trait_type": "Upgrade No.:2",
            "value": "Improved engine electronic"
        },
        {
            "trait_type": "Upgrade No.:3",
            "value": "stroker kit \"devil\""
        },
        {
            "trait_type": "Upgrade No.:4",
            "value": "Side vents"
        },
        {
            "trait_type": "Upgrade No.:5",
            "value": "Hood scoops"
        },
        {
            "trait_type": "Upgrade No.:6",
            "value": "Large rear wing"
        },
        {
            "trait_type": "Top Speed (km/h)",
            "value": 520
        },
        {
            "trait_type": "Max. Power (hp)",
            "value": 1055
        },
        {
            "trait_type": "Accelaration (0 to 100 km/h in sec)",
            "value": 1.75
        },
        {
            "trait_type": "Chassis",
            "value": "Carbon Fiber Monocoque"
        },
        {
            "trait_type": "Aerodynamics",
            "value": "Adjustable rear wing; chin spoiler with splitter"
        },
        {
            "trait_type": "Colour",
            "value": "Bitcoin-Gold"
        }
    ],
    "description": "Satoshi Bitcoin Supercar",
    "external_url": "https://www.etherlambos.io/index.php?lambo=112",
    "image": "https://www.etherlambos.io/API/render/lambo_112.png",
    "name": "Satoshi Serial No.: 12"
}`
 
* **Sample Call:**

    https://www.etherlambos.io/API/lambo/id/112

* **Token Metadata:**

* "name": 
`Represents the base model of the Etherlambo and the serial number for each model.`
* "image": `contains the path to the corresponding graphics regarding base and customized options.`
* "external_url": `represents the direct link to the etherlambos.io website.` 
* "description": `Description of the model.`
* "attributes": `lists all attributes as traits`
* "trait_type": `contains trait_type and value of each individual lambo.`
