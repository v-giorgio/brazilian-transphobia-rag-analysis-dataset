# Brazilian Transphobia YouTube Comments Dataset (BTYCD)

Este repositório contém o **Brazilian Transphobia YouTube Comments Dataset (BTYCD)**, um conjunto de dados anonimizado com comentários públicos do YouTube em português brasileiro, rótulos finais de anotação e predições finais de modelos usados no Trabalho de Conclusão de Curso. O objetivo é disponibilizar apenas os artefatos necessários para inspeção, reuso acadêmico autorizado e reprodução dos resultados finais.

Os dados são derivados de comentários públicos do YouTube, mas este repositório não contém nomes de usuários, IDs originais de usuários, IDs originais de comentários, IDs originais de vídeos, URLs de comentários ou metadados persistentes de publicação.

## Repositório com Código-Fonte

O código-fonte usado para preparação dos dados, experimentos, avaliação dos modelos e análises está disponível em:

[v-giorgio/brazilian-transphobia-rag-analysis](https://github.com/v-giorgio/brazilian-transphobia-rag-analysis)

## Estrutura

```text
final_dataset/
  dataset_final.csv
  dataset_final_full.csv

models_predictions/
  bertimbau/
  few_shot/
  rag/
  svm/
  zero_shot/
```

## Datasets

O nome recomendado para referência ao conjunto de dados é **Brazilian Transphobia YouTube Comments Dataset (BTYCD)**.

`final_dataset/dataset_final.csv` contém o subconjunto final usado nos experimentos principais. Ele inclui apenas comentários com pelo menos duas anotações, critério adotado para aumentar a confiabilidade dos rótulos usados na avaliação dos modelos.

`final_dataset/dataset_final_full.csv` contém a versão final ampliada do conjunto anotado. Ele inclui comentários com pelo menos uma anotação. Este conjunto não foi usado na avaliação dos modelos, mas é disponibilizado publicamente para contribuição científica, análises complementares e possíveis estudos futuros.

As colunas usam um identificador interno artificial (`dataset_comment_id`), título do vídeo, texto do comentário anonimizado, rótulos finais de anotação, contagens agregadas de anotação e metadados metodológicos de consenso/confiança. Os identificadores originais de YouTube e de usuários foram removidos.

## Predições

`models_predictions/` contém as predições finais dos modelos avaliados, organizadas por família de experimento:

- `bertimbau/`: predições de modelos BERTimbau ajustados.
- `svm/`: predições de modelos SVM.
- `zero_shot/`: predições zero-shot de LLMs.
- `few_shot/`: predições few-shot de LLMs.
- `rag/`: predições de LLMs com recuperação de contexto.

Os arquivos podem conter identificador interno, título do vídeo, comentário anonimizado, rótulo real, rótulo predito, escores, justificativa, contra-resposta e contexto recuperado sanitizado. IDs persistentes de fontes originais e URLs foram removidos dos artefatos de predição.

## Aviso Ético

Este repositório trata de classificação de discurso sobre pessoas trans e pode conter comentários ofensivos, transfóbicos, discriminatórios ou outros conteúdos sensíveis. O material é disponibilizado para fins de pesquisa, auditoria científica e desenvolvimento de métodos de moderação, não para assédio, exposição, vigilância, identificação de indivíduos ou amplificação de conteúdo abusivo.

## Restrições de Uso

Use estes dados apenas para fins acadêmicos, educacionais, jornalísticos ou de pesquisa responsável. Não tente reidentificar autores, localizar comentários originais, reconstruir IDs do YouTube, contatar pessoas envolvidas ou combinar estes dados com outras bases para identificação de indivíduos.

Este conjunto de dados não deve ser replicado, redistribuído, republicado ou incorporado em outros repositórios sem autorização prévia e menção/citação adequada ao trabalho original, conforme os termos indicados no arquivo `LICENSE`.

## Como Citar

Ao usar este repositório, cite obrigatoriamente o **Brazilian Transphobia YouTube Comments Dataset (BTYCD)** e inclua a referência ao repositório público do dataset. A citação do repositório é a referência principal do conjunto de dados.

```bibtex
@misc{btycd_2026,
  author = {Autor do TCC},
  title = {Brazilian Transphobia YouTube Comments Dataset (BTYCD)},
  year = {2026},
  howpublished = {Repositório público},
  url = {https://github.com/v-giorgio/brazilian-transphobia-rag-analysis-dataset},
  note = {Dataset anonimizado derivado de comentários públicos do YouTube}
}
```

Também cite o repositório de código-fonte usado para preparação dos dados, experimentos e análises:

```bibtex
@misc{brazilian_transphobia_rag_analysis,
  author = {Giorgio, V.},
  title = {Brazilian Transphobia RAG Analysis},
  year = {2026},
  howpublished = {\url{https://github.com/v-giorgio/brazilian-transphobia-rag-analysis}}
}
```

## Licença

Este repositório inclui um arquivo `LICENSE` com os termos de uso aplicáveis. A replicação, redistribuição ou republicação dos dados exige autorização prévia e menção/citação adequada ao trabalho original.

A redistribuição autorizada deve preservar este aviso ético, a nota de anonimização, as restrições de uso e a citação do trabalho original.
