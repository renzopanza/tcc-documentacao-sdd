# tcc-documentacao-sdd
Estrutura, templates, exemplificação da geração e automatização e documentação visual do Semantic Data Dictionary aplicado ao domínio da Terapia Cognitivo-Comportamental (TCC).

Contexto: Este repositório serve como um documento complementar para o seguinte Trabalho de Conclusão de Curso:

Título: Automação da geração de SDD e utilização em IA para TCC, integrando Ontologia e Grafos de Conhecimento
Curso: Engenharia de Software
Instituição: Associação Propagadora Esdeva Centro Universitário Academia – UniAcademia
Ano: 2026
Autor: Renzo Faedda Panza
Orientador: Evaldo de Oliveira da Silva

O repositório que contém o desenvolvimento apresentado no TCC está disponível em: https://github.com/evaldo/homogenise

O repositório da ontologia ONTRISCAL está disponível em: https://github.com/renzopanza/tcc-ontologia-ontriscal

-> Os cinco documentos do SDD:
1. Dictionary Mapping:
O Dictionary Mapping é o documento central do SDD, onde cada linha corresponde a uma variável do dataset utilizado e registra sua associação ao conceito ontológico presente na ONTRISCAL por meio de URI, o tipo de relação semântica e o esquema ao qual cada variável é pertencente. Por meio do Dictionary Mapping que as triplas RDF/OWL do GC são geradas.

![Especificação do Dictionary Mapping](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_dictionary_mapping.png)

2. Codebook:
Este documento complementa o Dictionary Mapping para as variáveis categóricas, definindo cada valor possível e os associando à classe correspondente na ONTRISCAL.

![Especificação do Codebook](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_codebook.png)

3. Timeline:
Documento que registra a dimensão temporal das variáveis (inicio e término de um evento) e pode ser usada para anotar classe e unidades relacionadas de um determinado evento.

![Especificação do Timeline](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_timeline.png)

4. Code Mapping:
O Code Mapping harmoniza as codificações entre diferentes sistemas, permitindo estabelecer equivalências semânticas entre variáveis distintas.

5. Infosheet:
O Infosheet é o documento de configuração estrutural do SDD, pois ele reúne os metadados gerais do dataset anotado, referência os demais documentos (Dictionary Mapping, Codebook, Code Mapping e Timeline), agindo em conformidade e garantindo os principios FAIR.

![Especificação do Infosheet](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_infosheet.png)

-> Arquivo de configuração para a automação da geração do GC:
Para que seja possível a execução do Script "sdd2rdf.py", responsável pela criação do arquivo .ttl, precisamos de ter em nosso projeto um arquivo de configuração inicial. Este arquivo é criado de maneira automática no momento em que o projeto é criado no sistema Homogenise, ele vem com o nome padronizado "config_{nome_do_projeto}.ini". O arquivo de config.ini possui informações imprescindíveis para a execução do script, tendo sua estrutura desta maneira:

![Especificação do Arquivo de configuração](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_config_ini.png)