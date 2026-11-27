# NutriPedia

## Description

**NutriPedia** identifies fruits and vegetables from photos and shows estimated calories and nutrients for the portion you enter. Photo recognition covers **36 produce categories**, and manual nutrition lookup covers **56 foods**, including papaya, avocado, and strawberries.

## Demo

See how NutriPedia analyzes a photo, lets you correct the suggested match, and updates the calorie estimate when you change the portion weight.

<!-- Upload your demo recording here. -->

## Core Technology

| Technology | Role |
| --- | --- |
| TensorFlow.js | Runs the image recognition model in the browser. |
| USDA FoodData Central | Supplies reference values for calories, carbs, fiber, protein, and fat. |
| React | Displays the photo preview, prediction, and nutrition results. |
| Express | Serves the frontend and model files. |

## How It Works

1. **Upload a photo.** NutriPedia displays its best supported match and the model’s confidence score.
2. **Check the match.** The nutrition panel selects the predicted food automatically. If the match is wrong, choose the correct food from the dropdown. You can also use the dropdown without uploading a photo.
3. **Enter the portion weight.** The lookup starts at **100 g**. Change the weight to update the calorie and nutrient estimates.

## Example Output

| Food | Portion | Estimated calories |
| --- | ---: | ---: |
| Apple | 100 g | 52 |
| Apple | 150 g | 78 |
| Papaya | 100 g | 43 |

The nutrition panel also shows **carbs, fiber, protein, and fat**. Select papaya manually in the nutrition dropdown.

## Key Features

- Photo recognition for 36 fruits and vegetables
- Manual nutrition lookup for 56 foods
- Calorie and nutrient estimates that update with portion weight
- Responsive layout for desktop and mobile
- Bundled model and nutrition data for recognition and lookup without an API key

## Purpose

NutriPedia helps you identify produce, compare nutrition values, and estimate what a measured portion contains.

## Run Locally

Install Node.js and npm, then run these commands from the project folder.

```bash
npm ci
npm ci --prefix frontend
npm run build --prefix frontend
npm start
```

Open `localhost:3002` in your browser.

## Project Structure

| Path | Contents |
| --- | --- |
| `frontend/` | React interface and browser-based image recognition |
| `models/model_inception/` | Bundled model and weight files |
| `app.js` | Express server |
| `frontend/src/Components/produceNutrition.json` | Nutrition values per 100 g and USDA reference IDs |

**Designed and built by Sami Ahmed Mohammed** (`samiahmed14`).

