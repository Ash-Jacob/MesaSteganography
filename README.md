# Secure Legal Document Steganography

A Python-based desktop application that hides a legal document inside an
image using **Least Significant Bit (LSB) steganography**. It can
optionally encrypt the document with **AES-256-GCM**, extract it later,
and verify the recovered document's integrity using **SHA-256**.

The project is implemented in the Jupyter Notebook
`secure_legal_doc_steganography.ipynb`.

## Features

-   Hide a document inside a cover image.
-   Optionally protect the hidden document with a password.
-   Extract the hidden document from the generated stego image.
-   Verify document integrity after extraction using a SHA-256 digest.
-   Display image quality measurements, including PSNR and SSIM, and
    performance measurements for embedding/extraction.
-   Export evaluation results to CSV (where supported by the application
    interface).

## Requirements

-   Python installed on your computer
-   Jupyter Notebook, JupyterLab, or another app that can open `.ipynb`
    notebook files
-   A desktop environment, because the project opens a graphical
    application window

## How to Run

1.  Install **Python** if it is not already installed:
    https://www.python.org/downloads/
2.  Install **Jupyter Notebook** by following the instructions here:
    https://jupyter.org/install\
    Alternatively, open the notebook in an app that supports `.ipynb`
    files, such as Visual Studio Code with its Python and Jupyter
    extensions.
3.  Open `secure_legal_doc_steganography.ipynb` in Jupyter Notebook or
    your preferred notebook app.
4.  If the notebook asks you to install the required libraries, run that
    installation cell and wait for it to finish.
5.  Run the notebook cells from top to bottom.
6.  Run the final cell to launch the application window.

## How to Use the Application

1.  Select a cover image.
2.  Select the document you want to hide.
3.  Enter a password if you want to encrypt the document.
4.  Run the hide/embed option and save the generated image. Use PNG to
    preserve the hidden data.
5.  To recover the document, select the generated image and use the
    extract option. Enter the same password if encryption was enabled.

## Visuals

### GUI Interface

The application interface for embedding and extracting legal documents.

<p align="center">
  <img width="671" alt="GUI Interface" src="https://github.com/user-attachments/assets/97cf7b16-8017-43ad-b6a2-346607a6e548" />
  <img width="671" alt="GUI Interface in Progress" src="https://github.com/user-attachments/assets/3c1bf0e7-d98a-4f1f-b9b0-57dd87b1740c" />
</p>

### Original Image vs. Stego-Image

A side-by-side comparison of the original image and the stego-image containing the hidden document. The differences are virtually imperceptible to the human eye.

<p align="center">
  <img width="100%" alt="Original Image vs. Stego-Image Comparison" src="https://github.com/user-attachments/assets/09ac337e-8516-4e4b-86e6-5d25b1546233" />
</p>

### Image Difference Analysis

When the original and stego-images are overlaid, the differences remain difficult to notice. Applying a pixel-wise hue-difference threshold makes these differences more visible.

<p align="center">
  <img width="100%" alt="Overlay and Pixel-wise Hue Difference" src="https://github.com/user-attachments/assets/78b33f20-9307-4370-96b4-0cee1331cd5b" />
</p>

## Notes

-   Use the generated **PNG** image without editing, resizing, or
    converting it. JPEG compression and image-editing apps can damage
    the hidden data.
-   The cover image must be large enough to store the document. If it is
    too small, choose a larger image or a smaller document.
-   Keep your password safe if you use encryption.
-   Run the notebook on your own computer. Some online notebook services
    cannot display desktop application windows.
-   This is an academic/demo project. Test it with non-sensitive sample
    documents before relying on it for real legal or confidential
    material.
-   In a real world scenario, it is ideal to use a cover image that is
    taken locally by the user. So as to avoid finding the original image
    available online which can compromise the secrecy of the stego-image.


