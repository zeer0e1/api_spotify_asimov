# Spotify Artist Info

---

Um web app simples construído com **Streamlit** que permite buscar informações sobre artistas do Spotify, incluindo suas músicas mais populares e seu índice de popularidade.

## Funcionalidades

* **Busca de Artistas:** Encontre artistas pelo nome.
* **Detalhes do Artista:** Visualize o nome oficial do artista e sua popularidade.
* **Top Músicas:** Obtenha uma lista das músicas mais populares do artista, juntamente com seus links diretos no Spotify e índices de popularidade.

---

## Como Usar

Siga os passos abaixo para configurar e executar o aplicativo localmente:

### 1. Pré-requisitos

Certifique-se de ter o **Python** instalado (versão 3.8 ou superior é recomendada).

### 2. Configuração do Ambiente

1.  **Clone o Repositório (ou crie os arquivos):**
    Se você estiver clonando um repositório Git:
    ```bash
    git clone <URL_DO_SEU_REPOSITORIO>
    cd <SEU_REPOSITORIO>
    ```
    Caso contrário, crie um diretório para o projeto e adicione os arquivos `app.py` (com o código fornecido) e `requirements.txt` (com as dependências) nele.

2.  **Crie um Ambiente Virtual (Recomendado):**
    ```bash
    python -m venv venv
    ```
    Ative o ambiente virtual:
    * **Windows:** `.\venv\Scripts\activate`
    * **macOS/Linux:** `source venv/bin/activate`

3.  **Instale as Dependências:**
    Crie um arquivo chamado `requirements.txt` no mesmo diretório do seu código e adicione as seguintes linhas:
    ```
    streamlit
    python-dotenv
    requests
    ```
    Em seguida, instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```

### 3. Configuração das Credenciais do Spotify API

1.  **Crie uma Aplicação no Spotify Developers:**
    * Vá para o [Spotify for Developers Dashboard](https://developer.spotify.com/dashboard/).
    * Faça login com sua conta Spotify.
    * Clique em "**Create an App**".
    * Preencha os detalhes solicitados (nome do aplicativo, descrição).
    * Após criar o aplicativo, você verá o seu **Client ID** e **Client Secret**.

2.  **Crie o Arquivo `.env`:**
    No diretório raiz do seu projeto (o mesmo onde está o arquivo `app.py`), crie um arquivo chamado `.env` e adicione suas credenciais do Spotify da seguinte forma:
    ```
    SPOTIFY_CLIENT_ID=SEU_CLIENT_ID_AQUI
    SPOTIFY_CLIENT_SECRET=SEU_CLIENT_SECRET_AQUI
    ```
    **Importante:** Nunca compartilhe seu arquivo `.env` ou suas chaves secretas publicamente (por exemplo, em repositórios Git).

### 4. Executando o Aplicativo

Com o ambiente virtual ativado e as credenciais configuradas, execute o aplicativo Streamlit:
```bash
streamlit run app.py