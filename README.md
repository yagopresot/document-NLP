# Extração e Análise de Entidades com NLP em Documentos

Este repositório contém um projeto de **Processamento de Linguagem Natural (NLP)** aplicado a **coleções de documentos em texto**. O foco principal é a utilização de **Reconhecimento de Entidades Nomeadas (NER)** com spaCy, além da organização das palavras em tabelas para futuras análises.

> Arquivo principal: `npl_documentos.py`

---

## 🧠 O que foi feito no código

1. **Acesso aos arquivos**

   * Montagem do Google Drive.
   * Leitura de um arquivo compactado (`texts.zip`) contendo múltiplos documentos de texto.

2. **Exploração inicial**

   * Impressão da lista de arquivos dentro do `.zip`.
   * Leitura e exibição do conteúdo de arquivos específicos.

3. **Reconhecimento de Entidades Nomeadas (NER)**

   * Uso do modelo `pt_core_news_sm` (português) do spaCy.
   * Extração de entidades como pessoas, locais, organizações etc.
   * Criação de um DataFrame com entidades e seus rótulos.

4. **Explicação dos rótulos**

   * Uso da função `spacy.explain` para descrever o significado de labels como `LOC`, `PER`, `ORG` e `MISC`.

5. **Visualização das entidades**

   * Uso de `spacy.displacy` para destacar graficamente as entidades dentro do texto.

6. **Processamento em inglês**

   * Download e uso do modelo `en_core_web_sm` do spaCy para análise de textos em inglês.

7. **Construção de tabela de palavras**

   * Geração de uma tabela (DataFrame) listando todas as palavras de cada arquivo (`Arquivo`, `Palavra`).
   * Exportação da tabela para CSV.

8. **Leitura de dados anotados (IOB)**

   * Importação de um arquivo `.tsv` (`palavras_IOB.tsv`) com rótulos IOB.
   * Inspeção das classes únicas presentes.

9. **Agrupamento de dados por documento**

   * Organização das palavras rotuladas por arquivo.
   * Extração de subconjuntos para análise de contextos específicos.

---

## 🧹 Benefícios de cada etapa

* **Leitura de arquivos compactados**: permite lidar com coleções de documentos sem necessidade de extração manual.
* **NER com spaCy**: identifica automaticamente nomes de pessoas, organizações, locais e outros elementos, enriquecendo a análise de textos.
* **Explicação dos labels**: facilita a compreensão dos tipos de entidades reconhecidos.
* **Visualização (`displacy`)**: melhora a interpretação das entidades, destacando-as dentro do texto.
* **Tabela de palavras (CSV/TSV)**: organiza os dados em formato tabular para análises estatísticas e treinamento de modelos.
* **Agrupamento por arquivo**: possibilita estudar cada documento separadamente, mantendo o contexto original.

---

## 🔮 Resultado esperado

O código fornece:

* Lista clara de documentos analisados.
* Extração automática de entidades nomeadas em português e inglês.
* Visualizações gráficas e tabelas com palavras e rótulos.
* Base estruturada pronta para futuras etapas de NLP (ex.: treinamento de NER customizado).

---

## 📜 Licença

Sinta-se à vontade para usar e adaptar.
