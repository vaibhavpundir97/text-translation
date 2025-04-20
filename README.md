# Transformer‑Seq2Seq Text Translation

This repository demonstrates how to build a transformer‑based sequence‑to‑sequence model for text translation using TensorFlow and Keras. The project loads a parallel corpus of input–output sentence pairs, preprocesses the data by tokenizing and adding start/end tokens, and trains a custom Transformer model from scratch. At the end, the notebook shows how to decode new sentences and compute accuracy on held‑out data.

## 📂 Repository Structure

```
├── dataset/
│   ├── train_input
│   ├── train_output
│   └── ...
├── transformer_seq2seq_translation.ipynb
├── requirements.txt
└── README.md
```

- **dataset/**  
  All raw data files. Place your parallel corpus files (e.g., one file per language or one file with tab‑separated sentence pairs) here.
- **transformer_seq2seq_translation.ipynb**  
  The main Jupyter notebook implementing data loading, preprocessing, model definition, training, and evaluation.
- **requirements.txt**  
  Python dependencies required to run the notebook.
- **README.md**  
  This file.

## 🚀 Getting Started

1. **Clone the repository**  
   ```bash
   git clone https://github.com/vaibhavpundir97/transformer-seq2seq-text-translation.git
   cd transformer-seq2seq-text-translation
   ```

2. **Create a virtual environment and install dependencies**  
   ```bash
   python3 -m venv venv
   source venv/bin/activate       # macOS/Linux
   # .\venv\Scripts\activate      # Windows
   pip install -r requirements.txt
   ```
3. **Launch and run the notebook**  
   ```bash
   jupyter lab
   # or
   jupyter notebook
   ```
   Open `transformer_seq2seq_translation.ipynb` and run cells in order.

## 📖 Notebook Highlights

- **Data Loading & Preprocessing**  
  - Read raw text files  
  - Split into train/validation/test  
  - Tokenize, vectorize, and add special `[start]` / `[end]` tokens  

- **Model Definition**  
  - Custom Transformer encoder–decoder built with `tf.keras.layers`  
  - Scalable to different vocabulary sizes and sequence lengths  

- **Training**  
  - Checkpointing the best model weights  
  - Training progress visualization via built‑in Keras callbacks  

- **Inference**  
  - A decoding loop that generates translated sentences token‑by‑token  
  - Final test accuracy computation

## 🛠 Dependencies

Listed in `requirements.txt`, for example:

```
tensorflow>=2.8
numpy
scikit-learn
```

## 🎯 Results

After training (e.g., 100 epochs), the model achieves a test accuracy of **99.84%** on held‑out data. You can further:

- Increase model depth or heads  
- Adjust learning rate schedule  
- Expand vocabulary size

## 🔗 References

- Vaswani et al., “Attention Is All You Need” (2017)  
- TensorFlow Transformer tutorials: https://www.tensorflow.org/tutorials/text/transformer
