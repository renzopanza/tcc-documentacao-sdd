# tcc-documentacao-sdd

> Estrutura, *templates*, exemplificação da geração automatizada e documentação visual do **Semantic Data Dictionary (SDD)** aplicado ao domínio da **Terapia Cognitivo-Comportamental (TCC)**.

![Status](https://img.shields.io/badge/status-desenvolvido-green)
![Ano](https://img.shields.io/badge/ano-2026-blue)
![Curso](https://img.shields.io/badge/curso-Engenharia%20de%20Software-informational)
![Licença](https://img.shields.io/badge/uso-acadêmico-lightgrey)

---

## 📑 Sumário

- [Sobre o projeto](#-sobre-o-projeto)
- [Repositórios relacionados](#-repositórios-relacionados)
- [Os cinco documentos do SDD](#-os-cinco-documentos-do-sdd)
  - [1. Dictionary Mapping](#1-dictionary-mapping)
  - [2. Codebook](#2-codebook)
  - [3. Timeline](#3-timeline)
  - [4. Code Mapping](#4-code-mapping)
  - [5. Infosheet](#5-infosheet)
- [Arquivo de configuração para automação do GC](#-arquivo-de-configuração-para-automação-do-gc)
- [Passo a passo de execução](#-passo-a-passo-de-execução)
- [Autoria](#-autoria)

---

## 📖 Sobre o projeto

Este repositório serve como **documento complementar** ao seguinte Trabalho de Conclusão de Curso:

| Campo | Descrição |
| :--- | :--- |
| **Título** | Automação da geração de SDD e utilização em IA para TCC, integrando Ontologia e Grafos de Conhecimento |
| **Curso** | Engenharia de Software |
| **Instituição** | Associação Propagadora Esdeva — Centro Universitário Academia (UniAcademia) |
| **Ano** | 2026 |
| **Autor** | Renzo Faedda Panza |
| **Orientador** | Evaldo de Oliveira da Silva |

---

## 🔗 Repositórios relacionados

- **Implementação (HOMOGENISE):** <https://github.com/evaldo/homogenise>
- **Ontologia ONTRISCAL:** <https://github.com/renzopanza/tcc-ontologia-ontriscal>

---

## 📚 Os cinco documentos do SDD

O Semantic Data Dictionary (SDD) é composto por cinco documentos interligados, cada um responsável por uma dimensão específica da anotação semântica do *dataset*.

### 1. Dictionary Mapping

O **Dictionary Mapping** é o documento central do SDD. Cada linha corresponde a uma variável do *dataset* utilizado e registra:

- Sua associação ao conceito ontológico presente na **ONTRISCAL** por meio de URI;
- O tipo de relação semântica;
- O esquema ao qual cada variável pertence.

> 💡 É a partir do *Dictionary Mapping* que as triplas **RDF/OWL** do Grafo de Conhecimento (GC) são geradas.

![Especificação do Dictionary Mapping](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_dictionary_mapping.png)

---

### 2. Codebook

O **Codebook** complementa o *Dictionary Mapping* para as **variáveis categóricas**, definindo cada valor possível e associando-os à classe correspondente na ontologia ONTRISCAL.

![Especificação do Codebook](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_codebook.png)

---

### 3. Timeline

O **Timeline** registra a **dimensão temporal** das variáveis (início e término de um evento), podendo ser utilizado para anotar a classe e as unidades relacionadas a um determinado evento.

![Especificação do Timeline](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_timeline.png)

---

### 4. Code Mapping

O **Code Mapping** harmoniza as codificações entre diferentes sistemas, permitindo estabelecer **equivalências semânticas** entre variáveis distintas.

---

### 5. Infosheet

O **Infosheet** é o documento de **configuração estrutural** do SDD. Ele:

- Reúne os metadados gerais do *dataset* anotado;
- Referencia os demais documentos (*Dictionary Mapping*, *Codebook*, *Code Mapping* e *Timeline*);
- Garante a conformidade com os princípios **FAIR** (*Findable, Accessible, Interoperable, Reusable*).

![Especificação do Infosheet](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_infosheet.png)

---

## ⚙️ Arquivo de configuração para automação do GC

Para que o *script* `sdd2rdf.py` — responsável pela criação do arquivo `.ttl` — possa ser executado, é necessário que o projeto contenha um **arquivo de configuração inicial**.

Esse arquivo é gerado automaticamente no momento em que o projeto é criado no sistema **HOMOGENISE**, recebendo o nome padronizado:

```text
config_{nome_do_projeto}.ini
```

O `config.ini` possui informações imprescindíveis para a execução do *script*, conforme estrutura abaixo:

![Especificação do Arquivo de configuração](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Especifica%C3%A7%C3%B5es/especificacao_config_ini.png)

---

## 🚀 Passo a passo de execução

O fluxograma abaixo apresenta a sequência completa para a execução da ferramenta **HOMOGENISE**:

![Passo a passo para a execução da HOMOGENISE](https://github.com/renzopanza/tcc-documentacao-sdd/blob/v1.0-tcc/Passo%20a%20passo/fluxograma_homogenise.png)

---

## ✍️ Autoria

**Renzo Faedda Panza**
Graduando em Engenharia de Software — UniAcademia
Orientador: Prof. Evaldo de Oliveira da Silva

> Este repositório é parte integrante do TCC e tem finalidade exclusivamente acadêmica.
