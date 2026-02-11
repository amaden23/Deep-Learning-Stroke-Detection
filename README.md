
# Brain Stroke Detection from CT Images

This project aims to detect the presence of strokes in Brain CT images using Deep Learning techniques.
We utilize **Transfer Learning** with the **VGG16** architecture, pre-trained on ImageNet weights.

## Project Structure
- **Brain_Stroke_Detection.ipynb:** The main Jupyter Notebook containing all code, training logic, and evaluation metrics.
- **best_stroke_model.keras:** The saved model weights with the highest validation accuracy (~95%).
- **requirements.txt:** List of Python libraries required to run this project.
- **results/:** Folder containing evaluation plots (Confusion Matrix, ROC Curve, Training History).

## Dataset
The model is trained on a dataset of DICOM images classified into:
- **Stroke (İnme Var)**
- **No Stroke (İnme Yok)**

## Methodology
1. **Preprocessing:** Brain Windowing (Center=40, Width=80) and Normalization.
2. **Model:** VGG16 (Frozen Base) + Custom Classification Head.
3. **Training:** Initial training followed by Fine-Tuning specific blocks.

## How to Run
1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Open the `.ipynb` file in Jupyter Lab, Google Colab, or VS Code.
4. Update the `DATA_DIR` path if necessary and run the cells.
