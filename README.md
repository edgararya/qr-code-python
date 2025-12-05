# 📱 Simple QR Code Generator (Colab Edition)

A simple Python script to generate standard QR Codes (Black & White). This project is **optimized for Google Colab**, allowing you to run it directly in your browser without any local Python installation.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Colab](https://img.shields.io/badge/Google_Colab-Compatible-orange)

## 🌟 Features
* **Google Colab Ready:** The script runs immediately with built-in library installation commands.
* **Standard Design:** Clean, high-contrast, and reliable black-and-white QR Code.
* **Instant Preview:** The generated QR Code appears directly on the Colab screen.
* **Auto Save:** Automatically saves the result as an image file (`.png`).

## 🚀 How to Run (Google Colab)

Since this script contains Colab-specific commands (like `!pip install`), it is recommended to run it in Google Colab.

1.  Open **[Google Colab](https://colab.research.google.com/)**.
2.  Create a **New Notebook**.
3.  Copy the code from the `qr_standar.py` file in this repository.
4.  Paste it into a code cell in Colab.
5.  Click the **Play** button (▶️).

## 🛠️ Main Code

```python
!pip install qrcode[pil]

import qrcode
from IPython.display import display

# Target Data/URL
data = "https://github.com/edgararya"

# QR Configuration
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=10,
    border=4,
)
qr.add_data(data)
qr.make(fit=True)

# Generate & Display
img = qr.make_image(fill_color="black", back_color="white")
display(img)

# Save File
img.save("edgararya.png")
```

<br>

## 📂 Output

Once executed, an image file named `edgararya.png` will appear in the **Files** panel (folder icon) on the left side of the Colab screen, ready for download.

---

## 👤 Author
* **Edgar Arya** - [GitHub Profile](https://github.com/edgararya)

---
*This project was created for Python learning purposes on Google Colab.*
