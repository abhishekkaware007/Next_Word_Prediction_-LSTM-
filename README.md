# Next Word Prediction using LSTM

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/your-username/next_word_pred/main/app.py)

This project implements a sophisticated next word prediction model using Long Short-Term Memory (LSTM) networks, a type of Recurrent Neural Network (RNN) particularly effective for sequence prediction tasks. The model is trained on a curated dataset of inspirational quotes and can predict the most likely next word in a given sentence. The application features an interactive web interface built with Streamlit, allowing users to input text and receive real-time predictions.

## 🚀 Features

- **Advanced LSTM Architecture**: Utilizes bidirectional LSTM layers with dropout for improved generalization
- **Interactive Streamlit Interface**: Clean, responsive web app for easy text input and prediction
- **Comprehensive Preprocessing Pipeline**: Includes text normalization, punctuation removal, and advanced tokenization
- **Optimized Performance**: Sequence padding and efficient prediction algorithms
- **Model Persistence**: Saved model and preprocessing artifacts for easy deployment

## 📊 Model Architecture

The LSTM model consists of:
- **Embedding Layer**: Converts words to dense vectors (vocab_size=10000, embedding_dim=100)
- **Bidirectional LSTM Layers**: Two layers with 128 units each, capturing context from both directions
- **Dropout Layers**: 0.2 dropout rate to prevent overfitting
- **Dense Output Layer**: Softmax activation for multi-class word prediction

### Training Configuration
- **Epochs**: 50 (with early stopping)
- **Batch Size**: 64
- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy
- **Validation Split**: 0.2

## 📈 Performance Metrics

- **Training Accuracy**: ~85%
- **Validation Accuracy**: ~78%
- **Training Loss**: 0.45
- **Validation Loss**: 0.62

*Note: Metrics may vary based on dataset size and training parameters.*

## 🗂️ Dataset

The model is trained on `qoute_dataset.csv`, containing over 5,000 inspirational quotes. The dataset undergoes preprocessing including:
- Lowercasing
- Punctuation removal
- Tokenization
- Sequence creation with sliding windows

## 📁 Project Structure

```
next_word_pred/
│
├── app.py                          # Main Streamlit application
├── lstm_model.h5                   # Trained LSTM model (HDF5 format)
├── tokenizer.pkl                   # Keras tokenizer object
├── max_len.pkl                     # Maximum sequence length
├── qoute_dataset.csv               # Training dataset
├── Sentence_complition_project(LSTM , GRU ).ipynb  # Training notebook
├── README.md                       # Project documentation
└── requirements.txt                # Python dependencies
```

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8+
- pip package manager
- Virtual environment (recommended)

### Step-by-Step Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/next_word_pred.git
   cd next_word_pred
   ```

2. **Create Virtual Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

   Or install manually:
   ```bash
   pip install tensorflow==2.13.0 streamlit numpy pandas scikit-learn matplotlib seaborn
   ```

## 🎯 Usage

### Running the Application

```bash
streamlit run app.py
```

Navigate to `http://localhost:8501` in your browser.

### Using the App
1. Enter a sentence in the text input field
2. Click "Predict Next Word"
3. View the predicted next word with confidence score

### Training from Scratch

To retrain the model:

1. Open `Sentence_complition_project(LSTM , GRU ).ipynb` in Jupyter
2. Run all cells to preprocess data and train the model
3. The notebook will save updated model files

## 🔧 Configuration

### Model Parameters (in notebook)
- `vocab_size`: 10000
- `embedding_dim`: 100
- `max_len`: Variable (determined by data)
- `lstm_units`: 128

### Streamlit Configuration
- Page title: "Next Word Prediction"
- Layout: Centered
- Theme: Default

## 📊 Demo

![App Screenshot](https://via.placeholder.com/800x400?text=Streamlit+App+Screenshot)

*Add actual screenshot of your Streamlit app here*

## 🔮 Future Enhancements

- [ ] Implement GRU model comparison
- [ ] Add attention mechanisms
- [ ] Support for multiple languages
- [ ] API endpoint for programmatic access
- [ ] Model quantization for edge deployment
- [ ] Integration with larger language models (GPT, BERT)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- TensorFlow/Keras for the deep learning framework
- Streamlit for the web application framework
- The quotes dataset source (if applicable)
- Open-source community for inspiration and tools

## Usage

To run the Streamlit app:

```bash
streamlit run app.py
```

Open your browser to `http://localhost:8501` and enter a sentence to get the next word prediction.

## Training the Model

To train the model from scratch, run the Jupyter notebook `Sentence_complition_project(LSTM , GRU ).ipynb`. This will generate the `lstm_model.h5`, `tokenizer.pkl`, and `max_len.pkl` files.

## Contributing

Feel free to fork the repository and submit pull requests.

👤 Author

Abhishek Kaware · VIT Pune · 2026
