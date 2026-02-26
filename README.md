# 🚀 Stirling – Guia Completo de Instalação e Execução Local

Este documento descreve como baixar o projeto do repositório e executá-lo localmente utilizando:

```bash
./gradlew bootRun
```

---

# 📋 Pré-requisitos do Sistema

Instale **todas** as dependências abaixo antes de executar o projeto.

---

## 1️⃣ Java (Obrigatório)

Requerido: **Java 17 ou superior** (recomendado 17 LTS)

### ✔ Verificar versão

```bash
java -version
```

### ⬇ Instalar (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install openjdk-17-jdk
```

---

## 2️⃣ Git

```bash
sudo apt install git
```

---

## 3️⃣ Tesseract (OCR PDF)

```bash
sudo apt install tesseract-ocr
sudo apt install tesseract-ocr-por   # opcional idioma português
```

Verificar:

```bash
tesseract --version
```

---

## 4️⃣ OCRmyPDF (OCR PDF)

```bash
sudo apt install ocrmypdf
```

Verificar:

```bash
ocrmypdf --version
```

---

## 5️⃣ qpdf (Repair / Compress PDF)

Requerido: **versão 11 ou superior** (recomendado 12)

```bash
sudo apt install qpdf
```

Verificar:

```bash
qpdf --version
```

---

## 6️⃣ rar (PDF → CBR)

```bash
sudo apt install rar
```

---

## 7️⃣ WeasyPrint (HTML / URL / Markdown / EML → PDF)

### Dependências do sistema

```bash
sudo apt install python3-pip python3-dev \
    libcairo2 libpango-1.0-0 libpangocairo-1.0-0 \
    libgdk-pixbuf-2.0-0 libffi-dev shared-mime-info
```

### Instalar

```bash
pip install weasyprint
```

### Verificar

```bash
weasyprint --version
```

---

## 8️⃣ unoconvert (File → PDF)

### Instalar LibreOffice

```bash
sudo apt install libreoffice
```

### Instalar unoconv

```bash
pip install unoconv
```

### Verificar

```bash
unoconv --version
```

---

## 9️⃣ ebook-convert (PDF ↔ EPUB / Ebook)

Faz parte do **Calibre**.

```bash
sudo apt install calibre
```

Verificar:

```bash
ebook-convert --version
```

---

## 🔟 OpenCV (Python) – Extract Image Scans

```bash
pip install opencv-python
```

Verificar:

```bash
python3 -c "import cv2; print(cv2.__version__)"
```

---

## 1️⃣1️⃣ Ghostscript

```bash
sudo apt install ghostscript
```

Verificar:

```bash
gs --version
```

---

## 1️⃣2️⃣ Poppler Utilities

```bash
sudo apt install poppler-utils
```

---

# 📥 Clonando o Repositório

```bash
git clone <https://github.com/VitorRez/Stirling-PDF.git>
```

---

# ▶ Executando o Projeto

O projeto utiliza **Gradle Wrapper**, portanto não é necessário instalar o Gradle manualmente.

```bash
./gradlew bootRun
```

Na primeira execução, o Gradle irá baixar automaticamente todas as dependências Java.

---

# 🌐 Acessando a Aplicação

Após iniciar corretamente:

```
http://localhost:8080
```

---

# ✅ Checklist Final

Verifique se tudo está instalado corretamente:

```bash
java -version
tesseract --version
ocrmypdf --version
qpdf --version
ebook-convert --version
gs --version
```

Se tudo estiver funcionando:

```bash
./gradlew bootRun
```

---

# ⚙️ Customização

Abra o arquivo:

```
app/core/configs/settings.yml
```

Edite os seguintes valores:

```yaml
ui:
  appName: PDF UFSJ            # Nome visível da aplicação
  homeDescription: ''          # Descrição exibida na página inicial
  appNameNavbar: PDF UFSJ      # Nome exibido na barra de navegação
  languages: []                # Se vazio, todos os idiomas são habilitados.
                               # Para exibir apenas Alemão e Polonês:
                               # ["de_DE", "pl_PL"]
                               # Inglês britânico é sempre habilitado.
```

---
```