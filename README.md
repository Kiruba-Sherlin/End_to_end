# End_to_end

COMPANY: CODTECH IT SOLUTIONS

NAME: KIRUBA SHERLIN. A

INTERN ID: CT04DH2074

DOMAIN: DATA SCIENCE

DURATION: 4 WEEKS

MENTOR: NEELA SANTOSH

Description:

🛠 Tools & Technologies Used:

1. Programming Language
     Python – for model training, API development, and data handling.

3. Libraries & Frameworks
     Pandas – Data manipulation and analysis.

     Scikit-learn – Machine learning model training (RandomForestClassifier) and dataset loading (load_iris).

     Pickle – Saving and loading the trained ML model.

     Flask – Lightweight web framework to create API endpoints for predictions.

     NumPy – Handling numerical arrays for model input.

4. Dataset
     Iris Dataset – Built-in dataset from scikit-learn containing flower measurements and species labels.

5. Development Tools
     VS Code / PyCharm – Code editor for development (any Python IDE).

     Command Line / Terminal – Running Python scripts and Flask server.

6. Deployment & Serving
     Flask Server – Serves model predictions via HTTP API.

   This project demonstrates the complete lifecycle of a machine learning application, from data loading and model training to model persistence and deployment using a web-based interface. It is designed to classify Iris flower species based on their physical measurements, providing an accessible yet powerful example of how machine learning models can be integrated into real-time applications.

The workflow begins with the Iris dataset, a classic dataset widely used for introductory machine learning experiments. This dataset contains 150 samples, each described by four numerical features: sepal length, sepal width, petal length, and petal width. The target variable represents the species of the flower, which can be one of three classes: Setosa, Versicolor, or Virginica. The dataset is loaded using the load_iris() function from the scikit-learn library and converted into a pandas DataFrame for ease of handling.

For the classification task, the project employs the Random Forest Classifier, an ensemble learning algorithm well-known for its robustness and accuracy. The model is trained on the dataset using default hyperparameters. Once the training is complete, the trained model is serialized and saved in a .pkl file format using Python’s built-in Pickle module. This step ensures that the model can be reused without retraining, which is crucial for deployment in production environments. The saved model is stored inside a model directory, which is created automatically if it does not already exist.

The second part of the project focuses on model deployment through a Flask web application. Flask, a lightweight web framework in Python, is used to create a RESTful API for serving predictions. At application startup, the saved model (iris_model.pkl) is loaded into memory. The Flask application defines two routes:

/ Route (GET) – This optional route renders an index.html template, which could serve as a simple web-based user interface for manual input.

/predict Route (POST) – This is the core API endpoint. It accepts JSON-formatted requests containing four numeric values corresponding to the flower’s measurements. The input values are passed to the model, and a prediction is generated. The output is returned in JSON format, indicating the predicted class as an integer (0, 1, or 2), corresponding to the three species.

The API includes basic error handling to return clear JSON error messages if the input format is invalid or if any other issue occurs during prediction. This makes the application more robust and user-friendly.

In practical terms, the /predict endpoint can be consumed by any client application capable of making HTTP requests, including web apps, mobile apps, or IoT devices. This makes the solution versatile and adaptable to different deployment scenarios.

Overall, this project encapsulates the essential steps in creating a deployable machine learning application: data preparation, model training, model persistence, API development, and prediction serving. While the Iris dataset and Random Forest algorithm make the example approachable for learning purposes, the same principles and architecture can be applied to more complex datasets and models for real-world use cases.

JSON – Data format for request and response in the API.

