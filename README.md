### Descrição do Projeto: Tradutor de Documentos `.docx` com OpenAI no Azure

Este projeto é um **tradutor de documentos automatizado**, foi criado durante o Bootcamp Microsoft IA 102 e utiliza a API do Azure Cognitive Services para traduzir documentos do formato `.docx` do inglês para o português. O arquivo traduzido é salvo no mesmo formato, mantendo a estrutura e o conteúdo formatado.

#### Principais Funcionalidades

1. **Tradução Automática**  
   - Traduz textos de documentos `.docx` do inglês para o português usando a API de Tradução Cognitiva do Azure.
   - Utiliza a versão 3.0 da API para garantir compatibilidade e suporte atualizado.

2. **Manipulação de Documentos**  
   - Lê o conteúdo dos parágrafos do documento original.
   - Realiza a tradução parágrafo por parágrafo.
   - Gera um novo arquivo `.docx` com o conteúdo traduzido.

3. **Exportação Automática**  
   - O arquivo traduzido é salvo com o mesmo nome do original, mas com um sufixo indicando o idioma de destino (`_pt-br`).

#### Pré-requisitos

1. **Configuração do Azure Cognitive Services**  
   - Uma chave de assinatura válida (`subscription_key`).
   - Um endpoint configurado na região correta.

2. **Bibliotecas Necessárias**  
   Instale as bibliotecas usando o comando:
   ```bash
   pip install requests python-docx
   ```

3. **Arquivo `.docx`**  
   Certifique-se de que o arquivo a ser traduzido esteja no formato `.docx`.

#### Como Usar

1. **Configure a chave de API e o endpoint** no código:
   ```python
   subscription_key = 'SUA_CHAVE_AQUI'
   endpoint = 'SEU_ENDPOINT_AQUI'
   ```

2. **Carregue o arquivo para tradução**  
   Especifique o caminho do arquivo no formato `.docx`:
   ```python
   input_file = "caminho/para/seu/arquivo.docx"
   translated_document(input_file)
   ```

3. **Resultado**  
   O arquivo traduzido será salvo no mesmo diretório do original, com o nome ajustado, por exemplo:  
   - Entrada: `arquivo.docx`
   - Saída: `arquivo_pt-br.docx`

#### Estrutura do Código

1. **Função `translator_text`**  
   - Realiza a integração com a API do Azure para traduzir um texto simples.  
   - Requer o idioma de destino (neste caso, `pt-br`).

2. **Função `translated_document`**  
   - Processa o arquivo `.docx`, traduzindo cada parágrafo.  
   - Gera um novo arquivo `.docx` com o texto traduzido.

#### Futuras Melhorias
- Adicionar suporte para tradução entre outros idiomas.
- Melhorar o tratamento de erros, especialmente para falhas de conexão com a API.
- Incorporar suporte a tabelas e imagens no `.docx`.
- Criar uma interface gráfica para facilitar o uso do script.

#### Observações
- Certifique-se de proteger sua chave de API e endpoint para evitar uso indevido.
- Use o script em conformidade com os Termos de Uso do Azure Cognitive Services.
