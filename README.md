# Zomato-Gen-AI
🍽️ Overview
This project implements a Restaurant Chatbot powered by Retrieval-Augmented Generation (RAG), built using Gradio, FAISS, and the Transformers library. The bot can answer questions related to restaurants, such as vegetarian options, spice levels, and gluten-free items, based on the context extracted from restaurant menus.

⚙️ Technologies Used
Python: Language for implementation

Gradio: User Interface

FAISS: Efficient similarity search for fast retrieval of restaurant data

Transformers: Hugging Face models (DPR for retrieval, FLAN-T5 for generation)

Torch: For model inference and handling computations on GPU/CPU

📦 Prerequisites
Before running the application, ensure you have the following installed:

Google Colab: You can run the project directly on Colab.

🔧 Setup Instructions
You can run the project directly on Google Colab by following these steps:

Open the Colab Notebook:

Click on the link to open the Colab notebook: [Colab Notebook Link](https://colab.research.google.com/drive/1sSfCjAoAZLIisDnwbYAS4WGwa3D0XBmj?usp=sharing)

Upload Your Data Files:

Ensure that you have uploaded the required files, such as the data_json (restaurant data) and any other necessary files like your FAISS index.

Install Required Libraries: The following libraries need to be installed in the Colab environment. You can install them by running the below cell:

python
Copy
Edit
!pip install gradio transformers torch faiss-cpu
Run the Notebook Cells:

Follow the instructions in the notebook to load your data, create the FAISS index, and run the chatbot model.

If necessary, ensure to execute these key steps:

Load the data_json file.

Generate the context embeddings and FAISS index.

Run the Gradio-based interface for the chatbot.

📝 Project Files and Structure
Colab Notebook: The notebook where the chatbot is implemented.

restaurant_dpr_index.faiss: FAISS index for fast similarity search.

restaurant_texts.pkl: Pickle file containing the preprocessed restaurant data.

requirements.txt: List of required Python libraries.

README.md: This file, with setup and usage instructions.

🚀 Usage
Run the Colab Notebook:

Once you've opened the notebook and uploaded the data, you can run all the cells in order to set up the chatbot.

Ask Questions: After running the notebook, you can use the Gradio-based chatbot interface to ask questions about the restaurant, such as:

"Which restaurant has the best vegetarian options?"

"Do you have gluten-free dishes?"

The chatbot will retrieve relevant restaurant data from the FAISS index and generate a detailed answer based on the context of the restaurant menus.

💻 Code Overview
Colab Notebook:

This file contains the Gradio interface and the answer_query function.

The answer_query function takes a user query, retrieves the relevant restaurant data using the FAISS index, and generates an answer using the FLAN-T5 model.

🧑‍💻 Modifying the Chatbot
Update the FAISS Index:

If you want to add new restaurant data or update the context, you can modify the restaurant_texts.pkl file and reindex the FAISS index.

Adding More Data:

The data (restaurant details and menu items) are stored in restaurant_texts.pkl. You can modify this data structure to add new restaurant information, such as vegan options, spice levels, etc.

Tuning the Model:

If you want to improve the response quality, you can experiment with different models or adjust the num_beams and max_length parameters in the generate function of FLAN-T5.

#🎥 Demo Video
Check out the demo of the Restaurant Chatbot in action:

Watch the demo video here
https://drive.google.com/file/d/1Bp9PZGi0VCvPWJSOXHCnsLL7m3KnYIGD/view?usp=sharing

🔄 Troubleshooting
Error: No module named 'faiss'

Ensure you've installed faiss-cpu in your environment. If you're on GPU, use faiss-gpu instead.

Gradio UI doesn't load:

Ensure that the Gradio interface is running on the correct port (7860 by default) and that no firewall is blocking access.

Model performance:

If the model is slow or giving incorrect answers, you may need to experiment with different models or recheck the context data for errors.

🔗 Contributing
Feel free to fork the repository, make changes, and create pull requests if you'd like to improve the project!
