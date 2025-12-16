# 🥗 AI Nutrition Coach

An intelligent nutrition analysis application powered by Google Gemini AI that provides detailed nutritional assessments of food images. Simply upload a photo of your meal, and get instant insights into calories, macronutrients, portion sizes, and health recommendations.

![Python Version](https://img.shields.io/badge/python-3.11.3-blue.svg)
![Flask](https://img.shields.io/badge/flask-3.0.0-green.svg)
![Google Gemini](https://img.shields.io/badge/Google-Gemini%201.5-orange.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🌟 Features

- **🖼️ Image-Based Analysis**: Upload food images for instant nutritional breakdown
- **🔍 AI-Powered Recognition**: Automatically identifies food items using Google Gemini 1.5 Flash
- **📊 Detailed Nutritional Info**: Get comprehensive data on:
  - Calorie estimation
  - Portion sizes
  - Macronutrients (Protein, Carbs, Fats)
  - Vitamins and Minerals
  - Health evaluation
- **💬 Custom Queries**: Ask specific questions about the food
- **🎨 User-Friendly Interface**: Clean, responsive web interface
- **🔒 Secure**: Environment variable-based API key management

## 🚀 Demo

This project demonstrates how cutting-edge AI can simplify complex tasks like calorie estimation and nutrition assessment, offering tech-savvy health enthusiasts and dietetics professionals an innovative tool to promote healthier lifestyle choices.

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.8 or higher (tested on Python 3.11.3)
- pip (Python package manager)
- A Google Gemini API key ([Get one here](https://aistudio.google.com/app/apikey))

## 📁 Project Structure

```
AI NUTRITION COACH/
│
├── static/              # Static files (CSS, JavaScript, images)
│   └── style.css        # Application styling
│
├── templates/           # HTML templates
│   └── index.html       # Main application page
│
├── venv/                # Virtual environment (not tracked in git)
│
├── .env                 # Environment variables (not tracked in git)
├── .env.example         # Example environment file
├── .gitignore           # Git ignore file
├── app.py               # Main Flask application
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation (this file)
```

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/sheraztariq22/AI-Nutrition-Coach
cd AI-NUTRITION-COACH
```

### 2. Create Virtual Environment

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

1. Copy the example environment file:
   ```bash
   cp .env.example .env
   ```

2. Edit `.env` and add your API keys:
   ```env
   GOOGLE_API_KEY=your_google_gemini_api_key_here
   FLASK_SECRET_KEY=your_random_secret_key_here
   ```

3. **Get your Google Gemini API Key**:
   - Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Sign in with your Google account
   - Click "Create API Key"
   - Copy and paste it into your `.env` file

4. **Generate a Flask Secret Key** (optional but recommended):
   ```python
   python -c "import secrets; print(secrets.token_hex(32))"
   ```

### 5. Run the Application

```bash
python app.py
```

The application will start on `http://localhost:5000`

## 💻 Usage

1. **Open your browser** and navigate to `http://localhost:5000`

2. **Upload a food image**:
   - Click the file upload button
   - Select an image of your meal (JPEG, PNG, etc.)

3. **Optional**: Add a custom query like:
   - "Is this meal suitable for a keto diet?"
   - "How much protein is in this meal?"
   - "What vitamins does this provide?"

4. **Click Submit** to get your nutritional analysis

5. **Review Results**:
   - Food identification
   - Portion sizes and calories
   - Total calorie count
   - Nutrient breakdown
   - Health evaluation
   - Important disclaimer

## 🔧 Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `GOOGLE_API_KEY` | Your Google Gemini API key | Yes |
| `FLASK_SECRET_KEY` | Secret key for Flask sessions | Yes |

### Supported Image Formats

- JPEG/JPG
- PNG
- GIF
- BMP
- WebP

## 📦 Dependencies

```
google-generativeai>=0.8.0  # Google Gemini AI SDK
Pillow>=10.1.0              # Image processing
flask>=3.0.0                # Web framework
requests>=2.32.0            # HTTP library
python-dotenv>=1.0.0        # Environment variable management
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
5. Push to the branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request

## 🐛 Troubleshooting

### Error: "GOOGLE_API_KEY environment variable is not set"

**Solution**: Make sure your `.env` file exists and contains the API key. Verify with:
```bash
# Check if .env file exists
ls -la .env

# View contents (be careful not to share this!)
cat .env
```

### Error: "ModuleNotFoundError"

**Solution**: Install all dependencies:
```bash
pip install -r requirements.txt
```

### Port Already in Use

**Solution**: Change the port in `app.py`:
```python
if __name__ == "__main__":
    app.run(debug=True, port=5001)  # Change to any available port
```

### API Rate Limits

Google Gemini has rate limits on the free tier. If you encounter rate limit errors:
- Wait a few minutes before trying again
- Consider upgrading to a paid plan for higher limits

## 🔒 Security Notes

- ✅ Never commit your `.env` file to version control
- ✅ Use environment variables for all sensitive data
- ✅ Rotate API keys regularly
- ✅ Use different API keys for development and production
- ✅ Keep your `requirements.txt` updated

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

Your Sheraz Tariq 

Project Link: [https://github.com/sheraztariq22/AI-Nutrition-Coach](https://github.com/sheraztariq22/AI-Nutrition-Coach)

## 🙏 Acknowledgments

- [Google Gemini AI](https://ai.google.dev/) for providing the powerful multimodal AI model
- [Flask](https://flask.palletsprojects.com/) for the web framework
- [Pillow](https://python-pillow.org/) for image processing capabilities
- All contributors and users of this project

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Troubleshooting](#-troubleshooting) section
2. Open an issue on GitHub
3. Contact the maintainer

## 🔮 Future Enhancements

- [ ] Add meal tracking history
- [ ] Export reports as PDF
- [ ] Multi-language support
- [ ] Dietary restriction filters (vegan, gluten-free, etc.)
- [ ] Meal recommendations based on health goals
- [ ] Integration with fitness trackers
- [ ] Mobile app version
- [ ] Barcode scanning for packaged foods

---

⭐ If you find this project helpful, please consider giving it a star on GitHub!

**Made with ❤️ and AI**