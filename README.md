# Facial-Gestures
simple supervised classification of facial gestures using Teachable Machine.

# What is the model classifying?
The model classifies six different facial gestures.

# What dataset are you using?
I used a dataset downloaded from Kaggle (https://www.kaggle.com/datasets/mykhailokosiuk/facial-gestures)

# What are the classes in the model?
- Neutral  
- Smiling  
- Wink Left  
- Wink Right  
- Closed Eyes  
- Mouth Open  

# How many examples per class did you use?
- Neutral: 100  
- Smiling: 100  
- Wink Left: 100  
- Wink Right: 100  
- Closed Eyes: 100  
- Mouth Open: 100 

For each class, I used:
- 50 male faces  
- 50 female faces 

# What meta-parameters did you use for training?
- Epochs: 50  
- Batch size: 16  
- Learning rate: 0.001  

---

# Strategies for Good Performance
- Kept the dataset balanced: 100 examples per class, split 50 male / 50 female.
- Included racial diversity to avoid bias toward one type of face.
- Captured examples from slightly different angles and perspectives to improve generalization.
- Collected some variation in facial expressions so the model wouldn’t just memorize a single pattern.
  
# When the Model Fails
- The model sometimes fails when the lighting is very dim or too bright, or when the camera angle is very different from the training images
  
# Difficult Classes to Train
- Wink Left vs Wink Right
The model often confused these two classes because the images were just flipped versions of each other, so it couldn’t reliably distinguish left from right.
- Neutral vs Smiling
The neutral face was sometimes misclassified as smiling, likely because subtle smiles or slight facial movements in neutral expressions confused the model.

# Increasing the Number of Classes
Yes, performance got harder to maintain as we added more classes. With only 2–3 gestures the model was very accurate, but with 6 classes, some probabilities became closer and misclassifications increased. This is because the model had to split its “attention” among more categories with the same number of training examples.

# Robustness to Environment
- The model is not very robust to changes in environment:
- Different lighting conditions affect performance strongly.
- Busy backgrounds can distract the classifier.
- Clothing and accessories (e.g., hats, masks, glasses) also confuse it.
- This suggests that the dataset needs more diverse examples to make the model more robust.
  
# Surprising Results
- The model learned Mouth Open and Neutral very well, even with a relatively small number of examples.
- These gestures are visually distinct (for Mouth Open) or consistent (for Neutral), making them easier for the model to detect than subtle differences like winks.
