# Quiz-JEEE

This project demonstrates the use of **cryptographic techniques** to secure online quizzes, such as those used for JEE (Joint Entrance Examination) preparation. By leveraging cryptographic algorithms, we can ensure the integrity, authenticity, and confidentiality of quiz data, preventing cheating and unauthorized access.

## Features

1. **Shamir's Secret Sharing**:
   - Used to split sensitive data (e.g., answer keys) into multiple parts (shares).
   - Only a threshold number of shares are required to reconstruct the original data, ensuring security and fault tolerance.

2. **Public Key Cryptography**:
   - Used to sign and verify quiz submissions, ensuring that the data has not been tampered with.
   - Ensures that only authorized users can submit answers or access sensitive information.

## Cryptographic Techniques Used

### 1. Shamir's Secret Sharing
- **Purpose**: Securely split sensitive data (e.g., quiz answer keys) into multiple parts.
- **How It Works**:
  - The answer key is split into multiple "shares."
  - A minimum number of shares (threshold) is required to reconstruct the key.
  - This ensures that no single person can access the answer key without collaboration.
- **Use Case in Quizzes**:
  - The answer key can be split among multiple administrators. Only when a predefined number of administrators agree can the key be reconstructed, preventing unauthorized access.

### 2. Public Key Cryptography
- **Purpose**: Ensure the authenticity and integrity of quiz submissions.
- **How It Works**:
  - A private key is used to sign quiz submissions.
  - The corresponding public key is used to verify the signature, ensuring that the submission is authentic and has not been altered.
- **Use Case in Quizzes**:
  - Each quiz taker is assigned a unique key pair.
  - Submissions are signed with the private key and verified by the server using the public key, ensuring that the submission is genuine and belongs to the correct user.

## How Cryptography Prevents Cheating in Online Quizzes

1. **Data Integrity**:
   - Cryptographic signatures ensure that quiz questions and answers cannot be tampered with during transmission.

2. **Authentication**:
   - Public key cryptography ensures that only authorized users can access the quiz or submit answers.

3. **Secure Answer Storage**:
   - Shamir's Secret Sharing ensures that the answer key is securely stored and can only be accessed by authorized personnel.

4. **Tamper-Proof Submissions**:
   - Signed submissions prevent users from altering their answers after submission.

## How to Use This Project

### Prerequisites
- Install [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/).
- Install dependencies using the following command:
  ```bash
  npm install


### Dependencies
Shamir's Secret Sharing: For splitting and reconstructing secrets.
@solana/web3.js: For generating key pairs.
tweetnacl: For signing and verifying messages.
tweetnacl-util: For encoding and decoding data.