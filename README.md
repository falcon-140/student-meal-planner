# Student Meal Planner (XML + DTD)

## Decision
Track my daily meals — what I ate, when, portion size, and nutrition — so I can balance diet with training and academic schedule.

## Signals
- Date (YYYY-MM-DD)
- Meal type (breakfast, lunch, dinner, snack)
- Dish name (string)
- Calories (kcal)
- Protein (grams)
- Portion size (small, medium, large)
- Optional tag (vegetarian, vegan, gluten-free)

## Gaps
- DTD can’t enforce numeric ranges for calories/protein.
- Doesn’t calculate daily totals or nutrient balance.
- No info on source (home-cooked, cafeteria, restaurant).

## Risk
- Missing or incorrect nutrition data leads to bad diet tracking.
- Enum drift (e.g., adding “brunch”) would break validation.
- Wrong date format makes meal logs unusable for analysis.

## Stewardship
- Owner: myself
- Stored in GitHub repo for class + portfolio use
- Retained for current semester only

## Data Domain
Primary: Student Meal Tracking  
Adjacent: Nutrition / Fitness  

## Broken XML Explanation
The `broken.xml` file fails validation because it:
- Is missing the required `id` attribute,
- Uses invalid enum values (`mealType="brunch"`, `portion="extraLarge"`),
- Has the wrong child element order (`calories` appears before `dish`).
