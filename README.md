# SERPTI - Sistema de Separação Patrimonial 📦

![Status](https://img.shields.io/badge/Status-MVP_Concluído-success)
![Licença](https://img.shields.io/badge/Licença-Uso_Interno-blue)

## 📌 Sobre o Projeto
O **SERPTI** é uma solução tecnológica *offline-first* voltada à modernização e automatização da logística de movimentação e despacho de equipamentos de TI. Desenvolvido para atuar na infraestrutura de almoxarifados da Secretaria de Estado de Saúde (SES-MT), o sistema resolve o gargalo operacional causado pela ausência de rede de internet (áreas de subsolo) e pela lentidão da conferência manual.

O projeto opera sob o modelo de **Processamento em Lote (*Batch Processing*)**, dividindo a responsabilidade em duas frentes integradas: um coletor móvel nativo e um painel web validador.

---

## 🚀 Principais Funcionalidades

*   **Leitura Óptica Offline:** Utilização da câmera do smartphone para ler códigos de barras de forma contínua e sem dependência de internet.
*   **Bloqueio de Duplicidades na Origem:** O aplicativo identifica e impede instantaneamente a leitura repetida de um mesmo patrimônio.
*   **Geração de Remessa:** Exportação rápida do lote de equipamentos conferidos para processamento.
*   **Consolidação Visual (Web):** Painel administrativo responsivo que recebe o lote, processa os dados localmente e atualiza o status de separação visualmente em tempo real.

---

## 🛠️ Tecnologias Utilizadas

A arquitetura do sistema é híbrida e foi desenvolvida para rodar com o máximo de performance nos dispositivos do próprio setor:

**Módulo Coletor (Mobile)**
*   **Java (Android Studio):** Desenvolvimento nativo para garantir acesso rápido ao hardware da câmera.
*   **ZXing Android Embedded:** Biblioteca de visão computacional para decodificação de códigos de barras.
*   **SQLite:** Banco de dados relacional embarcado para registro temporário da coleta.

**Módulo Validador (Web)**
*   **HTML5 & CSS3:** Estruturação e estilização do painel administrativo.
*   **JavaScript (Vanilla):** Lógica de negócios no lado do cliente (*client-side*), processamento de arquivos `.txt/.csv` e validação de regras de interface.
*   **IndexedDB:** Persistência de dados diretamente no navegador.

---

## 📂 Estrutura do Repositório

O código-fonte está dividido para facilitar a manutenção e o entendimento da arquitetura:

*   `/SERPTI-Web`: Contém todos os arquivos do painel administrativo (HTML, CSS e JS).
*   `/SERPTI-Mobile`: Contém o código-fonte completo do aplicativo desenvolvido no Android Studio.
*   `app-debug.apk`: Arquivo executável pronto para instalação em smartphones Android.

---

## 💻 Como Instalar e Executar

### 1. Painel Web (Módulo Validador)
Não é necessária a instalação de um servidor local.
1. Baixe os arquivos da pasta `SERPTI-Web`.
2. Abra o arquivo `index.html` em qualquer navegador moderno (Chrome, Edge, Firefox).

### 2. Aplicativo Mobile (Módulo Coletor)
1. Faça o download do arquivo `app-debug.apk` disponível na raiz deste repositório diretamente pelo seu celular Android.
2. Nas configurações do seu aparelho, permita a instalação de "Fontes Desconhecidas".
3. Execute o instalador e abra o app SERPTI.

---

## 📸 Capturas de Tela

*(Arraste as imagens do seu computador para cá. O GitHub vai gerar automaticamente um link para elas)*

*   **Tela Inicial do Painel Web:**
    `[Insira o print da tela do site aqui]`
*   **Coleta via Câmera (App Mobile):**
    `[Insira o print do app lendo o código de barras aqui]`

---

## 👨‍💻 Desenvolvedor e Responsável Técnico

**Otoniel Silva**
*   Engenharia da Computação - IFMT (Campus Cuiabá - Cel. Octayde Jorge da Silva)
*   Suporte de TI e Operações - SES-MT
