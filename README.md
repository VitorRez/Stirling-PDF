# Stirling – Guia Completo de Instalação e Execução Local

Este documento descreve como baixar o projeto do repositório e executá-lo localmente utilizando:

./gradlew bootRun

Não é necessário Docker ou Kubernetes.

------------------------------------------------------------

📌 PRÉ-REQUISITOS DO SISTEMA

Instale TODAS as dependências abaixo antes de executar o projeto.

------------------------------------------------------------

1️⃣ Java (Obrigatório)

Requerido: Java 17 ou superior (recomendado 17 LTS)

Verificar:
java -version

Instalar (Ubuntu/Debian):
sudo apt update
sudo apt install openjdk-17-jdk

------------------------------------------------------------

2️⃣ Git

sudo apt install git

------------------------------------------------------------

3️⃣ Tesseract (OCR PDF)

sudo apt install tesseract-ocr
sudo apt install tesseract-ocr-por   # opcional idioma português

Verificar:
tesseract --version

------------------------------------------------------------

4️⃣ OCRmyPDF (OCR PDF)

sudo apt install ocrmypdf

Verificar:
ocrmypdf --version

------------------------------------------------------------

5️⃣ qpdf (Repair / Compress PDF)

Requerido: versão 11 ou superior (recomendado 12)

sudo apt install qpdf

Verificar:
qpdf --version

------------------------------------------------------------

6️⃣ rar (PDF → CBR)

sudo apt install rar

------------------------------------------------------------

7️⃣ WeasyPrint (HTML/URL/Markdown/EML → PDF)

Dependências do sistema:
sudo apt install python3-pip python3-dev \
    libcairo2 libpango-1.0-0 libpangocairo-1.0-0 \
    libgdk-pixbuf-2.0-0 libffi-dev shared-mime-info

Instalar:
pip install weasyprint

Verificar:
weasyprint --version

------------------------------------------------------------

8️⃣ unoconvert (File → PDF)

Instalar LibreOffice:
sudo apt install libreoffice

Instalar unoconv:
pip install unoconv

Verificar:
unoconv --version

------------------------------------------------------------

9️⃣ ebook-convert (PDF ↔ EPUB / Ebook)

Faz parte do Calibre.

sudo apt install calibre

Verificar:
ebook-convert --version

------------------------------------------------------------

🔟 OpenCV (Python) – Extract Image Scans

pip install opencv-python

Verificar:
python3 -c "import cv2; print(cv2.__version__)"

------------------------------------------------------------

1️⃣1️⃣ Ghostscript

sudo apt install ghostscript

Verificar:
gs --version

------------------------------------------------------------

1️⃣2️⃣ Poppler Utilities

sudo apt install poppler-utils

------------------------------------------------------------

📥 Clonando o Repositório

git clone <URL_DO_REPOSITORIO>
cd <NOME_DO_PROJETO>

------------------------------------------------------------

▶ Executando o Projeto

./gradlew bootRun

Na primeira execução, o Gradle irá baixar automaticamente as dependências Java.

------------------------------------------------------------

🌐 Acessando

http://localhost:8080

------------------------------------------------------------

✅ Checklist Final

java -version
tesseract --version
ocrmypdf --version
qpdf --version
ebook-convert --version
gs --version

Se tudo estiver funcionando:

./gradlew bootRun