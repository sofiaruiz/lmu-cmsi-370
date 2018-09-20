## Application Description
> The app I will be making is an iOS app that gives a user nutrition information on the food they are eating. The app will allow users to search for recepies with ingredients they may have at home and give them a complete list of macros for that recepie and it will also suggest recepies with similar ingredients, it will allow users to scan a barcode/type in a food to find the nutrition of it (like calories, carbohydrates, etc.), and it will allow users to input a whole recepie and will give them the nutrition of their recepie back.

### Web Service(s) Used
> I will be using a few API's by Edamam. 
The first one is a recepie search API. The Edamam Recepie Search API is accessed by sending https requests on URLs. The base URL for the search is https://api.edamam.com/search. There are a few required parameters for the GET request URL. These include: q, which is a query text that the user would input (for example q=chicken), your api ID and key. There is also quite a few of optional parameters which you can see on the documentation for the API https://developer.edamam.com/edamam-docs-recipe-api.
The second is a nutrition analysis API. This API uses Natural Language Processing so that food entities from an unstructured text can be extracted. For this API a POST request is used to submit the recepie content (the ingredients and recepie title). The API will return will return nutritional analysis based on the information the user provides. The requred parameters for the request are: the name of the recepie, the ingredients (which is an array of strings), and your API ID and key. There are a few other parameters which can be included. These can be found on the documentation page for the API: https://developer.edamam.com/edamam-docs-nutrition-api
The last one is a food database. This API provides the nutrition data for generic and packaged foods, and restaurant meals. It also uses uses Natural Language Processing so that food entities from an unstructured text can be extracted. Searches can be made by keywords, food name, or a barcode. The base URL is: https://api.edamam.com/api/food-database/parser. A user is given a GET request and either a UPC (barcode) or ingredient need to be entered for the request to be valid. You also need your API ID and key to use the API. For more information the documentation can be found here: https://developer.edamam.com/food-database-api-docs.

## Top-Level Design/Layout
> Screen that first comes out when you open the app (title screen):
![Image of Screen](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/5%20-%20Screen%201.png)

> Home Screen:

![Image of Screen2](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/6%20-%20Screen%202%20copy.png)

> Barcode Scanner Screen:

![Image of Screen3](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/4%20-%20Screen%203.png)

> Food search screen:

![Image of Screen4](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/2%20-%20Screen%204.png)

> Recepie input screen:

![Image of Screen5](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/1%20-%20Screen%205.png)

> Saved recepies screen:

![Image of Screen6](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/3%20-%20Screen%206.png)

## Usage Scenarios
> A usage scenario is a mini-story that highlights how a user would accomplish a certain task in your front end. Provide at least two. Make sure to provide the following information per scenario: (a) the task that the user will perform, (b) the relevant user interface elements for performing this task, and (c) a brief narrative on how the user would perform this task with those user interface elements. Mock up, animate, or annotate your scenarios liberally.

### Searching for "generic" food
> User would click on the search button at the bottom of the screen:
![Image of Screen2](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/6%20-%20Screen%202%20copy%202.png)

> The user would then be tacken to the search food screen (as seen above). When the user is on that screen there will be "common food searches" available for them to click on (something like: cooked rice, apple, banana, Cliff bar) which will redirect them automatically to the nutrition analysis page for that specific food. If the food they are looking for is not in the common foods, they can input a search query that would take them to the nutrition analysis page for the food they inputed. Which would kind of look like:
![Image of Screen7](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/4%20-%20Screen%207.png)


### Searccing for a recepie
> To search for "something to cook" the user would need to input an ingredient (i.e. chicken) on the search bar at the top of the home screen. After they have inputed a search query they would be taken to another screen where there would be multiple recepies that contain that ingredient with the calories and number of ingredinets that are used for each recepie displayed. 
![Image of Screen8](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/Screen%208-%20State%201%20(1).png)

> Once the user is on this screen they would choose one of the recepies and click on it. After clicking on a recepie the user is taken to another screen where it takes them to a page where they can see the recepie with its ingredients and the nutritional analysis of the recepie. 
![Image of Screen9](https://github.com/sofiaruiz/lmu-cmsi-370/blob/master/Screen%209-%20State%201.png)

## Design Rationale
> State why your design is the way it is: relevant priorities, mental models, interaction design concepts, guidelines, principles, theories, etc. _Cite relevant references as needed._

## Usability Metric Forecast
> If implemented then tested, what would be your design’s strong metrics? Weak metrics? Explain your choices.

## References
> Cite formally if/where applicable, as you would with any other research paper.
