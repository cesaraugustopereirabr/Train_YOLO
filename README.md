# Train_YOLO
Treinamento para detecção e classificação de imagens com rede YOLO.

# YOLOv8 - Detecção de Objetos Personalizada (Pessoas, Cães e Carros)

Este projeto realiza **detecção de objetos em imagens estáticas** usando o modelo **YOLOv8x**, com foco em pessoas, cães e carros. As detecções são destacadas com **cores específicas por classe** e aplicam limiares de confiança distintos para melhor precisão.

---

## 📸 Exemplo de aplicação

![Exemplo de detecção](imagem_colorida.png)

---

## 🧠 Tecnologias utilizadas

- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- Python 3
- OpenCV
- Google Colab (execução sugerida)
- Matplotlib / PIL

---

## 🎯 Classes tratadas com cores personalizadas

| Classe   | Cor da Borda |
|----------|--------------|
| `person` | Verde        |
| `dog`    | Azul         |
| `car`    | Vermelho     |
| Outras   | Amarelo      |

---

## 📦 Funcionalidades

- [x] Detecção de objetos com YOLOv8 pré-treinado (`yolov8x.pt`)
- [x] Filtro de confiança geral (`≥ 0.60`) e específico para carros (`≥ 0.40`)
- [x] Cores específicas por classe detectada
- [x] Exibição dos rótulos e níveis de confiança
- [x] Geração automática de imagem final (`imagem_colorida.png`)
- [x] Download do resultado com bounding boxes

---

## ▶️ Como usar no Google Colab

1. Abra um novo notebook no [Google Colab](https://colab.research.google.com/).
2. Copie o código do arquivo `detecção_yolov8_colab.py`.
3. Execute célula por célula:
   - Faça o upload da imagem desejada;
   - Aguarde o processamento;
   - Baixe a imagem anotada com as detecções.

---

## 🛠 Parâmetros configuráveis

Você pode ajustar diretamente no código:

```python
GENERAL_THRESHOLD = 0.60  # confiança mínima geral
CAR_THRESHOLD = 0.40      # confiança mínima apenas para 'car'
