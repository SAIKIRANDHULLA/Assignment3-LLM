# Assignment3-LLM

**Sentiment Analysis Model for Movie Reviews with BERT**
# Introduction
This project focuses on developing a sentiment analysis model using BERT (Bidirectional Encoder Representations from Transformers) to classify movie reviews into sentiment categories. The goal is to create an accessible web-based interface where users can input movie reviews and instantly receive sentiment predictions.

# Dataset
The dataset used in this project consists of movie reviews in the form of sentences. It includes:

# Training Data (train.csv): Contains 100,694 sentences with two columns:
**review_text:** The review sentence.
**class_index:** The sentiment label (1 = Very Bad, 2 = Bad, 3 = Neutral, 4 = Good, 5 = Very Good).
**Test Data (test.csv):** Contains 25,174 sentences with the same structure as the training data.
**Methodology**
**Data Preparation**
The data was preprocessed and tokenized using BERT's tokenizer, which converts the text into a format suitable for model input.

**Model Selection and Training**
**Model:** The BERT model was used for sequence classification with five sentiment classes.
**Training:** The model was fine-tuned on the training dataset for two epochs, with evaluation conducted at each epoch. A learning rate of 2e-5 and a batch size of 16 were used.
**Environment:** Training was conducted on a GPU to accelerate the process, with mixed precision training enabled.
**Model Deployment**
Web Application: A Flask-based web application was developed to allow users to input movie reviews and receive sentiment predictions.
Hosting: The application was deployed using ngrok to make it accessible via a public URL, as the development environment was Google Colab.
**Challenges Encountered**
**Long Training Time: **The training process took approximately 1.5 hours.
**GPU Constraints:** Adjustments to batch sizes were necessary due to GPU memory limitations.
**Indexing Errors:** Issues in mapping model outputs to sentiment labels during deployment required debugging.
**Deployment Issues:** Network connectivity and environment configuration challenges in Google Colab affected deployment.
**Future Improvements**
**Optimize Training Time: **Explore more efficient models or use more powerful GPUs.
**Improve Memory Management: **Optimize batch sizes and explore techniques like gradient accumulation.
**Robust Deployment:** Consider using a production-ready server or cloud platform for more stable deployment.
**Enhanced Error Handling:** Implement better error handling and logging for quick issue resolution.
**Conclusion**
This project demonstrates the development and deployment of a sentiment analysis model using BERT, integrated into a web application for real-time sentiment predictions on movie reviews. While suitable for demonstration, future work could focus on improving model accuracy, scalability, and adding features like multilingual support.
