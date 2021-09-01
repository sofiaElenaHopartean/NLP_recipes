# NLP_recipes

Notes and observations on what needs improvement, the current state of the model, requirements:

- Training data preparation: although current model accuracy is high, more attention is needed on individual "Ingredient" matching with "Directions" content. There is a plot that shows that there is ~1 ingredient/recipe that is not found. There are multiple causes. For example, the ingredient is written differently in "Directions" vs "Ingredients" ex: "half and half" vs "half-and-half", "sugar" vs "white sugar", or some "Directions" just don't contain ingredients.  
- Predictions: the model makes predictions on each word in the sentence for (S/B/I/E)-INGREDIENT or O. Obs. It should predict positioning. Positioning is determined programmatically after model output. More time is needed to finetune positioning. Also, the positioning is relative to "Directions" after cleanup, they should be relative to initial  "Directions". 
- model supports concurrency during inference through batching 
