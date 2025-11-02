### Intelligent Code Decoder

This repository holds a collection of Python scripts demonstrating robust computer vision techniques for decoding various 1D and 2D codes, including PDF417, Data Matrix, Barcodes, QR Codes, Aztec, and MaxiCode.

The scripts are designed to decode images **as is**, requiring no manual pre-manipulation or image editing, and serve as the solution for the "AI without ML Part 2" assessment.

### 🛠️ Prerequisites

  * Python 3.8+
  * **Docker:** Required for scripts that use the ZXing Java CommandLineRunner for robust decoding (e.g., `decode_pdf417.py`).

### ⚙️ Setup and Installation

Follow these steps to set up your environment and run the decoders:

#### 1\. Activate the Virtual Environment

It is critical to run this project within its isolated environment.

```bash
# In the repository root directory:
.\venv\Scripts\Activate.ps1
```

*(If you are on Linux/macOS, use `source venv/bin/activate`)*

#### 2\. Install Dependencies

With the environment active, install all required Python libraries:

```bash
pip install -r requirements.txt
```

#### 3\. Prepare External Dependencies

For the most robust decoding (like PDF417, which often utilizes the powerful ZXing library):

  * **Ensure Docker is running** on your system.
  * **Place the necessary ZXing JAR files** (e.g., `javase-3.5.0.jar`, `core-3.5.0.jar`, etc.) into the script's directory, as they are mounted into the Docker container during execution for decoding barcodes like the PDF417.

### 🏃 How to Run a Decoder Script

Once your environment is set up, you can execute any of the decoding scripts by simply providing the image name (or ensuring the image is named as expected by the script).

For example, to run the PDF417 decoder:

```bash
cd PDF417 code
python decode_pdf417.py
```