# Tradutor de Textos com Gemini

Este projeto em Python utiliza a API do Gemini do Google AI Studio para traduzir palavras ou textos inseridos pelo usuário para diferentes idiomas. A tradução é feita de forma sucinta, conforme configurado.

## Funcionalidades

* **Tradução para Múltiplos Idiomas:** O script permite traduzir textos para inglês, russo, alemão, espanhol, turco e português do Brasil.
* **Interface de Linha de Comando:** A interação com o usuário é feita através da linha de comando, solicitando a palavra/texto a ser traduzido e o idioma de destino.
* **Utilização da API Gemini:** Integra-se com a API do Gemini para realizar as traduções.
* **Configurações de Chat Específicas:** Para cada idioma, uma configuração de chat é criada, instruindo o modelo a atuar como um poliglota fluente no idioma alvo e a traduzir de forma sucinta.
* **Loop Interativo:** Permite que o usuário traduza múltiplas palavras ou textos sem precisar reiniciar o script. O programa encerra quando o usuário digita "fim".
* **Tratamento de Erros:** Inclui tratamento para erros de entrada do usuário (ao escolher o idioma).

## Pré-requisitos

Antes de executar o código, você precisará:

1.  **Criar uma conta no Google AI Studio:** Acesse [https://makersuite.google.com/app/apikey](https://makersuite.google.com/app/apikey) e siga as instruções para criar uma conta e gerar uma **API Key**.
2.  **Instalar as dependências:** Certifique-se de ter as seguintes bibliotecas Python instaladas. Você pode instalá-las usando o `pip`:

    ```bash
    pip install google-generativeai google-colab
    ```

## Configuração

1.  **Armazenar a API Key:** O script utiliza o `google.colab.userdata` para acessar a API Key de forma segura no ambiente Google Colab. Se você estiver executando o código localmente ou em outro ambiente, precisará configurar a variável de ambiente `GOOGLE_API_KEY`.

    **No Google Colab:**
    * No painel esquerdo, clique no ícone de chave (Secrets).
    * Crie um novo segredo com o nome `GOOGLE_API_KEY` e cole sua API Key do Google AI Studio no campo de valor.

    **Localmente (não recomendado para segurança em longo prazo):**
    Você pode definir a variável de ambiente diretamente no seu terminal antes de executar o script:

    ```bash
    export GOOGLE_API_KEY="SUA_API_KEY"
    ```

    **Melhor prática localmente (usando `.env`):**
    Crie um arquivo chamado `.env` no mesmo diretório do seu script e adicione a seguinte linha:

    ```
    GOOGLE_API_KEY=SUA_API_KEY
    ```

    Em seguida, você precisaria adicionar algumas linhas ao seu código Python para carregar as variáveis de ambiente do arquivo `.env` (usando uma biblioteca como `python-dotenv`).

2.  **Executar no Google Colab (opcional):** Se você estiver usando o Google Colab, o ambiente já possui algumas dependências pré-instaladas. Basta conectar-se a um runtime e executar as células de código.

## Como Usar

1.  **Execute o script Python.**
2.  Quando solicitado na linha de comando, **informe a palavra ou o texto** que você deseja traduzir e pressione Enter.
3.  Em seguida, você será solicitado a **informar o número correspondente ao idioma** para o qual deseja traduzir:
    * `1 - Ingles`
    * `2 - Russo`
    * `3 - Alemão`
    * `4 - Espanhol`
    * `5 - Turco`
    * `6 - Português`
4.  O script enviará o texto para a API do Gemini e exibirá a tradução na tela.
5.  Você será solicitado a inserir outra palavra ou texto. Para encerrar o programa, digite `fim` e pressione Enter.

## Exemplo de Uso

Informe a palavra ou texto a ser traduzido: Olá
Informe o idioma da tradução:
1 - Ingles
2 - Russo
3 - Alemão
4 - Espanhol
5 - Turco
6 - Português
6
Tradução:  Olá

Informe a palavra ou texto a ser traduzido: Hello
Informe o idioma da tradução:
1 - Ingles
2 - Russo
3 - Alemão
4 - Espanhol
5 - Turco
6 - Português
2
Tradução:  Привет

Informe a palavra ou texto a ser traduzido: fim
Programa encerrado.


## Observações

* A qualidade da tradução dependerá da complexidade do texto de entrada e das capacidades do modelo Gemini.
* Certifique-se de que sua API Key esteja configurada corretamente para que o script possa se conectar à API do Google AI Studio.
* O tempo de resposta pode variar dependendo da carga da API do Gemini e da sua conexão com a internet.

## Autor

[lcllima3012]

Sinta-se à vontade para contribuir com melhorias ou reportar problemas!
