{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Student Meal Planner (XML + DTD)\
\
## Decision\
Track my daily meals \'97 what I ate, when, portion size, and nutrition \'97 so I can balance diet with training and academic schedule.\
\
## Signals\
- Date (YYYY-MM-DD)\
- Meal type (breakfast, lunch, dinner, snack)\
- Dish name (string)\
- Calories (kcal)\
- Protein (grams)\
- Portion size (small, medium, large)\
- Optional tag (vegetarian, vegan, gluten-free)\
\
## Gaps\
- DTD can\'92t enforce numeric ranges for calories/protein.\
- Doesn\'92t calculate daily totals or nutrient balance.\
- No info on source (home-cooked, cafeteria, restaurant).\
\
## Risk\
- Missing or incorrect nutrition data leads to bad diet tracking.\
- Enum drift (e.g., adding \'93brunch\'94) would break validation.\
- Wrong date format makes meal logs unusable for analysis.\
\
## Stewardship\
- Owner: myself\
- Stored in GitHub repo for class + portfolio use\
- Retained for current semester only\
\
## Data Domain\
Primary: Student Meal Tracking  \
Adjacent: Nutrition / Fitness  \
\
## Broken XML Explanation\
The `broken.xml` file fails validation because it:\
- Is missing the required `id` attribute,\
- Uses invalid enum values (`mealType="brunch"`, `portion="extraLarge"`),\
- Has the wrong child element order (`calories` appears before `dish`).\
}