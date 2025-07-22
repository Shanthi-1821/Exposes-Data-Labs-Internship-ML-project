Overview

This project uses a Machine Learning model to authenticate users based on typing behavior and allows only authenticated users to encrypt and send messages. The messages are securely decrypted by the receiver. Unauthorized users are blocked from accessing the encryption process.


---

Dataset Used

Dataset Source: Kaggle (Keystroke Dynamics)

Link: https://www.kaggle.com/datasets/carnegiecylab/keystroke-dynamics-benchmark-data-set

---

Tools & Libraries Used

Python 3

Scikit-learn

Pandas, NumPy

Cryptography (Fernet)

Matplotlib

Google Colab

---

How It Works

Data Preprocessing: Clean the dataset, label users as real or fake

Model Training: Split data and train ML model for authentication

User Authentication: Predict if the user is authorized

Encryption: If authenticated, encrypt message using Fernet

Decryption: Decrypt the message for authorized receivers

Hashing (optional): Ensure message integrity

---

ML Model Details

Algorithm: Random Forest Classifier

Input Features: Typing durations, delays

Target: 1 for authenticated user, 0 for others

Accuracy: ~100% (on test set)

---

Demo

Run the full notebook on Google Colab

Input a message manually or select from file

Get encrypted and decrypted results

View real/fake user authentication in action

---

Key Functionalities

Upload Dataset (.csv) from local machine

Preprocess Data and label a specific user (e.g., s027) as the real user

Train a Machine Learning Model (Random Forest Classifier)

Authenticate User (real or fake)

Encrypt Message using Fernet (symmetric AES encryption)

Decrypt Message on receiver side if authenticated

---

Dataset Format

Columns: subject, sessionIndex, rep, H.period, DD.period.t, UD.period.t, etc.

Real user label is set based on the subject column (e.g., 's027' is real, others are fake)

---

Future Enhancements

Real-time user typing input capture (instead of static data)

GUI-based front end or integration with a messaging platform

Add hashing or digital signature for integrity verification

---

Sample Outputs

User Authenticated. Proceeding to encrypt message...

Encrypted: gAAAAABi..

Decrypted: This is a confidential message.

Authentication Failed. Message encryption blocked.

---

By - Shanthi S






