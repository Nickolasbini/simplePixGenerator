# Gerador de PIX Estático (Copia e Cola + QR Code)

![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)

Este projeto é uma ferramenta prática para gerar payloads de pagamento **PIX Estático** seguindo as normas do Banco Central do Brasil. Ideal para landing pages, pequenos e-commerces ou doações.

---

## Tutorial Completo
Este código foi desenvolvido e explicado detalhadamente no canal **CódigoPráticoOficial**.
👉 [Assista ao tutorial no YouTube](https://www.youtube.com/@CodigoPraticoOficial)

---

## Como Funciona o Padrão BRCode
Diferente de uma simples string, o PIX utiliza o padrão **EMV QRCPS**. Cada informação possui um ID e um tamanho específico.

| ID | Descrição | Valor Exemplo |
| :--- | :--- | :--- |
| **00** | Payload Format Indicator | `01` |
| **26** | Merchant Account Info | `BR.GOV.BCB.PIX...` |
| **52** | Merchant Category Code | `0000` |
| **54** | Transaction Amount | `10.50` |
| **58** | Country Code | `BR` |
| **63** | CRC16 (Checksum) | `E139` |



---

## Tecnologias Utilizadas
* **JavaScript Puro (Vanilla JS):** Lógica de montagem e cálculo de bits.
* **QRCode.js:** Biblioteca leve para renderização do QR Code no navegador.
* **CSS Flexbox:** Interface responsiva e limpa.

---

## Como Rodar o Projeto
1. Faça o download do arquivo `index.html`.
2. Abra em qualquer navegador moderno.
3. Preencha sua **Chave PIX**, **Nome** e **Valor**.
4. O código "Copia e Cola" e o QR Code serão gerados instantaneamente.

### Regras Importantes do Banco Central:
* **Sem Acentos:** O nome do beneficiário e a cidade não podem conter acentos ou caracteres especiais (ex: `São Paulo` vira `SAO PAULO`).
* **Casas Decimais:** O valor deve sempre ter duas casas decimais separadas por ponto (ex: `10.00`).
* **CRC16:** O código final é validado por um Checksum de 16 bits. Se um único caractere estiver errado, o banco recusará o pagamento.

---

## Licença
Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

---
Feito com ☕ por [CódigoPráticoOficial](https://www.youtube.com/@CodigoPraticoOficial)