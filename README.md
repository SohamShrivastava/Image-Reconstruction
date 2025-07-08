# Image Reconstruction using Random Fourier Features (RFF) and Matrix Factorization (MF)

This project compares two techniques for image reconstruction:  
- **Random Fourier Features (RFF)** – a nonlinear approximation method using kernel-inspired embeddings.  
- **Matrix Factorization (MF)** – a linear low-rank approximation using gradient descent.

Developed as part of an ML course assignment at IIT Gandhinagar.

---

## Objectives

- Reconstruct images using partial or noisy data with two distinct ML techniques.
- Compare the accuracy of both methods using RMSE and PSNR metrics.
- Analyze trade-offs between **nonlinear feature mapping** (RFF) and **low-rank structure modeling** (MF).

---

## Methods

### 1. RFF-Based Image Reconstruction
- Used Random Fourier Features to map pixel coordinates \((x, y)\) into a high-dimensional feature space.
- Applied **Linear Regression** to learn RGB mappings.
- Visualized reconstructed vs. original images.

** Results:**  
- RMSE: `0.1025`  
- PSNR: `19.78 dB`

---

### 2. Matrix Factorization (with Gradient Descent)
- Represented the image as a product of two low-rank matrices: \( U \cdot V^T \approx \text{Image} \).
- Used gradient descent to learn both matrices.
- Reconstructed image side-by-side with original.

** Results:**  
- RMSE: `0.0619`  
- PSNR: `24.17 dB`

---

## Understanding RMSE and PSNR

###  RMSE (Root Mean Squared Error)
- Measures the average difference between original and reconstructed pixel values.
- **Lower RMSE** indicates better reconstruction accuracy.
- Sensitive to large errors — even a few incorrect pixels can raise RMSE.

###  PSNR (Peak Signal-to-Noise Ratio)
- Compares the maximum possible pixel value with the reconstruction error.
- **Higher PSNR** means better image quality and less visible distortion.
- PSNR > 30 dB: High-quality  
  PSNR between 20–30 dB: Moderate quality  
  PSNR < 20 dB: Noticeable degradation
  
###  Interpretation of Results
- **Matrix Factorization** produced a lower RMSE and higher PSNR, indicating a more accurate reconstruction.
- **RFF-based method** still preserved essential image features and demonstrated potential for nonlinear reconstructions, especially when high-frequency information is present.

---

##  References

- [SIREN Notebook – RFF](https://github.com/nipunbatra/ml-teaching/blob/master/notebooks/siren.ipynb)  
- [Matrix Factorization Notebook](https://github.com/nipunbatra/ml-teaching/blob/master/notebooks/movie-recommendation-knn-mf.ipynb)

---

##  Collaborators

- [Aditya Jain](https://github.com/AdityaJain2373) 
- [Vansh Kumar](https://github.com/VanshOnGit)

--
