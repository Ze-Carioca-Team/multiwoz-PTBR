# MultiWOZ-PTBR

Esse projeto tem como objetivo realizar a tradução para português-brasileiro do [MultiWOZ](https://github.com/budzianowski/multiwoz), que foi originalmente criado em inglês.

## Como a tradução foi feita

O serviço [Google Cloud Translate](https://cloud.google.com/translate) foi utilizado para realizar a tradução das 'utterances' e dos 'slot_values' dentro de cada json.

## Arquivos Traduzidos
Os arquivos traduzidos se encontram nas pastas:
 - data/MultiWOZ_2.2/dev/
 - data/MultiWOZ_2.2/test/
 - data/MultiWOZ_2.2/train/

## Limitações

O serviço de tradução escolhido para esse projeto utiliza mecanismos que consideram diversos dados para realizar a tradução, o que pode alterar os resultados quando traduzindo palavras iguais. Esses mecanismos geralmente trazem grandes benefícios aos resultados, mas podem gerar discrepâncias se as frases sendo traduzidas precisarem ter os mesmos termos para palavras-chave.

Esse comportamento teve um impacto negativo nos resultados das traduções, onde as traduções dos 'slot_values' acabaram ficando diferentes das palavras utilizadas dentro das 'uterrance'. 

Atualmente, cerca de 9% dos meta-dados ainda apresentam alguma discrepância das frases traduzidas.

Total de acertos 23530

Total de inconsistências: 2358

## Como melhorar os resultados

Para auxiliar no processo de identificação de inconsistências e ajustes, o script `improve_multiwoz-ptbr.ipynb` é fornecido. Com esse script é possível identificar quais 'slot_values' tem maior ocorrência de problemas e adicionar um caso específico para esse problema ser solucionado no próprio script.




## Projeto

O desenvolvimento desse projeto contou com a colaboração de:

- Júlio César dos Reis - Coordenador do Projeto
- Leandro A. Villas - Pesquisador Associado
- Allan M. de Souza - Pós-Doutorado
- Rafael Roque - Pós-Doutorado
- Matheus Ferraroni Sanches - Doutorado
- Jader - Mestrado
- Paula Jeniffer dos Santos - Mestrado
- Andreis - Graduação
- Henrique - Graduação