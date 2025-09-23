# 🤖 Imersão em Agentes de IA com Python — Alessandra Cardozo

Este repositório reúne os projetos desenvolvidos por mim, Alessandra, durante minha jornada de aprendizado em **Inteligência Artificial** e **Python**, utilizando o ambiente do **Google Colab**. Cada notebook representa uma etapa prática da imersão, com foco em dados, visão computacional e agentes inteligentes.

---

## 📚 Projetos Disponíveis

### 1. `Visão_Computacional.ipynb`
> **Detecção Facial Estilizada com OpenCV**

- Utiliza classificadores Haar para detectar rostos, olhos e sorrisos em imagens.
- Aplica estilo visual com retângulos coloridos e título personalizado.
- Imagem utilizada: Carlo Acutis.
- Resultado: imagem processada com destaque facial.

📷 *Imagem gerada com detecção facial estilizada incluída no notebook.*

---

### 2. `Imersao_Alessandra_Agentes_de_IA_Alura+Gente.ipynb`
> **Exploração de Agentes Inteligentes com Python**

- Projeto desenvolvido durante a imersão da Alura + Gente.
- Simulações de agentes autônomos e interações inteligentes.
- Utilização de bibliotecas como `random`, `matplotlib`, e lógica de decisão.

---

### 3. `Aula-04++-Python-para-Dados+Ciência (1).ipynb`
> **Manipulação de Dados com Python**

- Introdução à análise de dados com Python.
- Uso de estruturas como listas, dicionários e DataFrames.
- Aplicações práticas com dados simulados.

---

## 🚀 Como Executar os Projetos

1. Acesse cada notebook diretamente no Google Colab.
2. Execute as células em ordem para visualizar os resultados.
3. Para projetos com imagens, certifique-se de que os arquivos `.png` estejam no mesmo diretório.

---

## 🧠 Tecnologias Utilizadas

- Python 3
- Google Colab
- OpenCV
- Matplotlib
- Pandas
- Lógica de agentes e simulações



## 💬 Sobre Mim

Sou apaixonada por tecnologia, aprendizado contínuo e aplicações criativas de inteligência artificial. Este repositório é parte da minha jornada de estudos e experimentações com Python e IA.

Feito com 💚 por **Alessandra Cardozo**

---


## 📌 Licença

Este projeto está sob a licença MIT. Sinta-se à vontade para explorar, aprender e contribuir!
______________________________________________________________________________________________________________________

# 👩‍⚕️👨‍⚕️ Especialista vs Generalista — Reconhecimento Facial com OpenCV

Este projeto demonstra como realizar **reconhecimento facial** em imagens usando a biblioteca **OpenCV** no ambiente **Google Colab**. A imagem utilizada compara dois profissionais da saúde — um especialista e um generalista — e serve como base para aplicar técnicas de detecção facial.

## 📌 Objetivos
- Carregar e exibir imagens no Google Colab
- Detectar rostos usando o classificador Haar Cascade
- Destacar rostos com retângulos visuais
- Salvar imagens com rostos detectados

## 🛠️ Tecnologias utilizadas
- Python 3
- OpenCV
- Matplotlib
- Google Colab

## 🚀 Como executar

1. Faça upload da imagem no Colab:
   ```python
   from google.colab import files
   uploaded = files.upload()

2. Carregue e exiba a imagem:

import cv2
import matplotlib.pyplot as plt

imagem_nome = list(uploaded.keys())[0]
img = cv2.imread(imagem_nome)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb)
plt.axis('off')
plt.show()

3. Baixe o classificador Haar Cascade e detecte rostos:

cascade_url = "https://github.com/opencv/opencv/raw/master/data/haarcascades/haarcascade_frontalface_default.xml"
cascade_path = "haarcascade_frontalface_default.xml"

import urllib.request
urllib.request.urlretrieve(cascade_url, cascade_path)

gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
face_cascade = cv2.CascadeClassifier(cascade_path)
faces = face_cascade.detectMultiScale(gray, scaleFactor=1.1, minNeighbors=5)

for (x, y, w, h) in faces:
    cv2.rectangle(img, (x, y), (x+w, y+h), (0, 255, 0), 2)

img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb)
plt.axis('off')
plt.title(f"{len(faces)} rosto(s) detectado(s)")
plt.show()

4. (Opcional) Salve a imagem com os rostos detectados:

cv2.imwrite("rostos_detectados.jpg", img)

📷 Imagem utilizada
A imagem compara dois médicos — um especialista e um generalista — e foi gerada para fins educacionais. Ela pode ser substituída por fotos reais para testes mais avançados.

📚 Créditos
Projeto desenvolvido por Alessandra com apoio do Microsoft Copilot 🤖.






