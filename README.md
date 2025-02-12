# Image-to-HTML-Model-Development
The goal of this assignment is to develop a deep learning model that takes an image as input and generates the corresponding HTML code. The dataset used for this task is WebSight from Hugging Face, which consists of images and their corresponding HTML representations.
Here's a **README.md** file for your project:  


## 📌 Overview  
This project focuses on developing a deep learning model that takes an **image as input** and generates the corresponding **HTML code**. The model is trained on the **WebSight dataset** from Hugging Face, which consists of image-HTML pairs.  

##  Objective  
- Convert images into HTML using **Vision-Language Models**.  
- Compare different approaches (CLIP-GPT2, BLIP, CNN-BiLSTM).  
- Evaluate model performance using **BLEU Score** and **Token-Level Accuracy**.  

## 📂 Dataset  
- **Source:** Hugging Face [WebSight Dataset](https://huggingface.co/datasets)  
- **Structure:** Each entry consists of an **image** and its **corresponding HTML code**.  
- **Preprocessing:**  
  - HTML is **tokenized** before training.  
  - Images are resized and normalized for input into models.  

## Approach  

###  Model Selection  
Three models were explored:  
1. **CLIP-GPT2:** Uses CLIP for image encoding and GPT-2 for HTML generation.  
2. **BLIP:** Treats HTML as a caption and generates structured HTML using a transformer-based architecture.  
3. **CNN-BiLSTM:** Extracts image features using CNN and generates sequences using BiLSTM.  

### Implementation Steps  
1. **Data Preprocessing**  
   - Tokenized HTML using a **transformer-based tokenizer**.  
   - Converted images into tensors for model training.  
2. **Model Training**  
   - Used **pre-trained models** for feature extraction and sequence generation.  
   - Trained for **2 epochs** with **batch size 4**.  
   - Optimized using **AdamW** optimizer.  
3. **Evaluation Metrics**  
   - **BLEU Score**: Measures the accuracy of generated HTML.  
   - **Token-Level Accuracy**: Checks how closely the generated tokens match the actual HTML.  
   - **Structural Validity**: Ensures the output is syntactically correct.  
4. **Deployment & Testing**  
   - Models were tested using **Google Colab**.  
   - Trained models were saved as **.pth files**.  

## 📊 Results  

| Model        | BLEU Score (Approx.) |
|-------------|------------------|
| **CLIP-GPT2** | 0.42 |
| **BLIP**      | 0.56 |
| **CNN-BiLSTM** | 0.38 |

###  Best Performing Model: **BLIP**  
BLIP outperformed the other models with a BLEU score of **0.56**, making it the best choice for image-to-HTML conversion.  

##  Next Steps  
- Fine-tune the models for more **epochs** to improve accuracy.  
- Implement **Beam Search** instead of greedy decoding.  
- Deploy the model via **Gradio** or **Flask** for real-time testing.  

## 📁 Repository Structure  
```
├── data/                  # Preprocessed dataset  
├── models/                # Trained models  
├── notebooks/             # Colab notebooks for training/testing  
├── scripts/               # Python scripts for training and evaluation  
├── results/               # Evaluation results and visualizations  
├── README.md              # Project documentation  
```

## 📌 How to Run  
1. Clone the repository:  
   ```bash
   git clone https://github.com/viggu3sd/Image-to-HTML-Model-Development.git
   cd Image-to-HTML-Model-Development
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the **Google Colab notebook** provided in the repository.  

## ✉️ Contact  
For any queries, feel free to reach out:  
- **Vignesh **  
- **Email:** phyvignesh3@gmail.com


