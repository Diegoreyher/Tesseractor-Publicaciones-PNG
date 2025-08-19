# 🖼️ Proyecto OCR con Tesseract

<div align="center">

## Descripción

Este proyecto permite extraer texto de imágenes utilizando **OCR** con **Tesseract**.  
Incluye funciones para buscar palabras específicas como "usado" o términos relacionados con repuestos/refacciones en screenshots.

</div>

---

## 💻 Requisitos

Necesitas tener instalado Tesseract OCR en tu máquina:

https://github.com/tesseract-ocr/tesseract

Ajusta la ruta de Tesseract OCR según tu instalación:

pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'

Crea un archivo `requirements.txt` con el siguiente contenido:

```txt
pytesseract==0.3.10
Pillow==10.3.0
selenium==4.21.0
numpy==1.26.4
opencv-python==4.11.0.86  # Compatible con numpy 1.26.4
pdf2image==1.17.0  # Si quieres leer PDFs escaneados

## Además, necesitas tener instalado Tesseract OCR en tu máquina:
https://github.com/tesseract-ocr/tesseract


