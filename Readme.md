python3.11 -m venv my_env
source my_env/bin/activate

pip install ibm-watsonx-ai==1.1.20 image==1.5.33 flask requests==2.32.0

Exercise 1:
model_id = "ibm/granite-vision-3-2-2b"

Exercise 2:
params = TextChatParameters()
params = { 
    "temperature": 0.7,
    "max_tokens": 800
}

model = ModelInference(
    model_id=model_id,
    credentials=credentials,
    project_id=project_id,
    params=params
)

AI Calorie Coach project! By building this application, I've successfully explored the powerful capabilities of the Llama 4 Maverick 17B 128E Instruct FP8 model and integrated it with AI-driven technologies to deliver practical, real-world solutions for dietary management. I've gained hands-on experience in encoding images, constructing effective prompts for generative models, and presenting nutritional data in a user-friendly format.

This project demonstrates how cutting-edge AI can simplify complex tasks like calorie estimation and nutrition assessment, offering tech-savvy health enthusiasts and dietetics professionals an innovative tool to promote healthier lifestyle choices. As AI continues to advance, your understanding of multimodal models and their real-world applications will be invaluable in leveraging technology for positive impacts on everyday life.
