# 📍 Controle Meteorológico — Check-in de Localização

Aplicação web leve em arquivo único (`index.html`) desenvolvida para capturar coordenadas geográficas (latitude e longitude) via GPS do navegador e enviá-las automaticamente para uma planilha por meio de integração direta com o Google Forms.

---

## 📋 Funcionalidades

- **Identificação de Local:** Campo de texto obrigatório para nomear ou identificar o ponto de coleta (ex.: *Loja Centro, Ponto 04*).
- **Captura de GPS de Alta Precisão:** Utiliza a API nativa `navigator.geolocation` com `enableHighAccuracy: true`, formatando latitude e longitude com **6 casas decimais** (precisão aproximada de ~11 cm) e exibindo a margem de erro em metros.
- **Envio Assíncrono sem Back-end:** Submete os dados diretamente para o endpoint `formResponse` de um Google Forms via `fetch` (`mode: 'no-cors'`), eliminando a necessidade de servidor próprio.
- **Feedback Visual em Tempo Real:** Indicadores de carregamento (*spinner*) durante a busca de sinal GPS e envio, além de mensagens claras de sucesso ou tratamento de erros (permissão negada, sinal indisponível ou *timeout*).
- **Design Responsivo:** Interface limpa e adaptável para dispositivos móveis e desktop, sem dependências externas.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5** (estrutura semântica e formulário acessível)
- **CSS3** (variáveis CSS, Flexbox, Grid Layout e animações nativas)
- **JavaScript (ES6+)** (Geolocation API, Fetch API, `URLSearchParams` e `async/await`)
- **Google Forms** (armazenamento e integração com Google Sheets)

---

## 📂 Estrutura do Projeto

```text
controle-meteorologico/
├── index.html   # Aplicação completa (HTML, CSS e JavaScript)
└── README.md    # Documentação do projeto
