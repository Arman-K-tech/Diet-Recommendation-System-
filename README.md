🛠️ Key FeaturesDual-Model Support: Includes both a RandomForestRegressor and a TensorFlow/Keras Neural Network for caloric prediction.
Dynamic Meal Planning: A greedy optimization algorithm that selects food items based on protein-to-calorie ratios.
Automated Data Cleaning: Robust preprocessing pipeline to merge disparate food and nutrition datasets.
Interactive UI: A user-friendly web interface powered by Gradio for real-time recommendations.
📊 How It Works:
1. Caloric PredictionThe system calculates the Basal Metabolic Rate (BMR) using the Mifflin-St Jeor Equation:$$BMR = 10 \times weight (kg) + 6.25 \times height (cm) - 5 \times age (y) + s$$(Where $s$ is +5 for males and -161 for females).
   The AI models then learn to map these biological features plus activity levels to precise caloric targets.
2. Recommendation EngineThe engine filters the nutrition_distriution.csv based on the user's goal:
   Weight Loss: Prioritizes foods with the highest protein_per_kcal.
   Weight Gain: Prioritizes foods with the highest kcal_per_100g.

   💻 Tech StackLanguage:
    PythonML/DL: Scikit-Learn, TensorFlow, KerasData
    Analysis: Pandas, NumPy
    Deployment: Gradio (Web UI)
    Serialization: Joblib (for scalers and models)
   
   📁 Repository StructureDiet Recommendation System.ipynb: The main development notebook containing data cleaning, model training,and the Gradio app.food.csv: Dataset containing food item names.
   
  Nutrition_distriution.csv: Detailed nutritional facts for food items.diet_model.keras,
  Pre-trained Deep Learning model.scaler_x.pkl & scaler_y.pkl: Preprocessing scalers for input/output normalization.
