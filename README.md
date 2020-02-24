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


## Solution
To find the driving ingredients for each cuisine, I tried two methods: word frequency and impotant features.

### Word Frequency
Basically, the more often the ingredients are used, the more important they are to the cuisine. I used nltk to find the most frequently used ingredients for each cuisine. For example, the driving ingredients for Italian food are:

<p align="center"><img src="https://github.com/qianzhangut/recipe2cuisine/blob/master/importance_nltk.png" width="500"/></p>

However, it is difficult to identify the commonly used ingredients in all cuisines, such as salt, water, pepper, etc. This is hard to outsourced team to hand label the recipes.

### Important Features 

Generally, importance provides a score that indicates how useful or valuable each feature was in the construction of the boosted decision trees within the model. The more an attribute is used to make key decisions with decision trees, the higher its relative importance. The important features can be considered as the driving ingredients for the cuisines. 








| Mexican          		| Southern_US       | Indian        	  | Chinese         | 	Moroccan		|
| ------------- 		| -------------     | -------------       | -------------   |------------- 		| 
|corn tortillas         | buttermilk        | garam masala        |soy sauce        |ground cumin       |
|flour tortillas        | butter            | ground turmeric     |corn starch      |ground cinnamon    |
|salsa                  | chopped pecans    | cumin seed          |sesame oil       |chickpeas          |
|avocado                | baking powder     | curry powder        |hoisin sauce     |olive oil          |
|jalapeno chilies       | all-purpose flour | tumeric             |oyster sauce     |ground ginger      |
