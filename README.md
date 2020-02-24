# Recipe2Cuisine

## Task
This is a data challenge I completed in 4 hours at Insight. The data is a small training set of about 39,000 recipes with labeled cuisines. The task is to design and execute a method to predict the cuisine of a recipe given only its ingredients. Also, I need to find the driving ingredients to characterize each major cuisine, so that I can write a guideline for an outsourced team to hand label the remaining unlabled recipes.


## EDA
The data has 39774 non-null rows of recipes, 2 columns: cuisine and ingredients. 
| 			     		| id		    | cuisine		| ingredients   |
| ------------- 		| ------------- | ------------- | ------------- |
| 0						| 10259      	| greek			| [romaine lettuce, black olives, grape tomatoes...  |
| 1				  		| 25639         | southern_us   | [plain flour, ground pepper, salt, tomatoes, g...  |
| 2		 				| 20130         | filipino      | [eggs, pepper, salt, mayonaise, cooking oil, g... |
| 3						| 22213         | indian        | [water, vegetable oil, wheat, salt]  |
| 4		 				| 13162         | indian        | [black pepper, shallots, cornflour, cayenne pe...  |

There are totally 20 classes of cuisines, and Italian food has the most recipes. The distributin of cuisine types is

<p align="center"><img src="https://github.com/qianzhangut/recipe2cuisine/blob/master/cuisine.png" width="500"/></p>









| Mexican          		| Southern_US       | Indian        	  | Chinese         | 	Moroccan		|
| ------------- 		| -------------     | -------------       | -------------   |------------- 		| 
|corn tortillas         | buttermilk        | garam masala        |soy sauce        |ground cumin       |
|flour tortillas        | butter            | ground turmeric     |corn starch      |ground cinnamon    |
|salsa                  | chopped pecans    | cumin seed          |sesame oil       |chickpeas          |
|avocado                | baking powder     | curry powder        |hoisin sauce     |olive oil          |
|jalapeno chilies       | all-purpose flour | tumeric             |oyster sauce     |ground ginger      |
