# HCQuery

### What it does

HCQuery is a predictive model for detecting hydroxychloroquine (HCQ) retinopathy using Optical Coherence Tomography (OCT) B-scans. It takes an OCT image as input and outputs a **Likelihood of Retinopathy Score (LRS)**, a continuous value representing the model's confidence in the presence of retinopathy.

This repository contains:
- The trained PyTorch model (`hcquery_model.pt`)
- A Jupyter Notebook (`hcquery_classifier.ipynb`) for running inference
- Supporting code and dependency information

### How to use it

1. Clone this repository:
   ```bash
   git clone https://github.com/peterwoodward-court/hcquery.git
   cd hcquery

2. Install dependencies:
    ```bash
    pip install -r requirements.txt

3. Prepare files
   - Place the pretrained model in the project directory 
   - Prepare a folder containing the OCT images you wish to analyse

4. Launch JupyterLab, and open and run the cells in hcquery_classifier.ipynb
   - Ensure you update the file paths to your appropriate directory
   
   **Input**
   - Accepts a single OCT image or a folder of images (see notebook for examples).
   - Expected image format: .png, .tiff or .jpg, greyscale
   
   **Output**
   The script will:
   - Process all images in the specified directory.
   - Print the predicted probability of HCQ retinopathy for each image.
   - Save the results to a text file
 
 ### Dependencies
 
 - Python ≥ 3.8
 - PyTorch ≥ 1.10
 - torchvision
 - Pillow
 - efficientnet-pytorch
 
 See `requirements.txt` for exact versions
 
 ### Caveats

 This tool is for exploratory research only and is not intended for clinical use.
 
 ### Citation
 
 Woodward-Court, Peter, et al. "Deep-learning algorithm for the diagnosis and prediction of hydroxychloroquine retinopathy: An International, multi-institutional study." 
 Ophthalmology Retina (2025). https://doi.org/10.1016/j.oret.2025.06.003

 ### License

 This is provided under an MIT license.
