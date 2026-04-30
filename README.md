# Beamer 101

Template Beamer em LaTeX para apresentações acadêmicas, com estrutura pronta para seções, imagens, bibliografia e capa customizável por logos.

## O que este modelo oferece

- Capa customizável com três logos via `\SetupCustomTitle{logo_instituto}{logo_laboratorio}{logo_universidade}`.
- Estrutura base de apresentação: capa, súmario, seções e frames.
- Macros de apoio para figuras e pausas de apresentação.
- Integração com bibliografia em `BibLaTeX` (arquivo [references.bib](references.bib)).
- Pastas de figuras por seção em [figuras/](figuras/).

## Estrutura principal

- Modelo principal: [modelo.tex](modelo.tex)
- Exemplo adicional: [exemplo.tex](exemplo.tex)
- Configuração geral de slides: [loadslides.tex](loadslides.tex)
- Macros e utilitários: [styles/elegantmacros.sty](styles/elegantmacros.sty)
- Tema Beamer (estilos): [styles/](styles/)
- Referências bibliográficas: [references.bib](references.bib)

## Como customizar rapidamente

### 1) Metadados
Edite em [modelo.tex](modelo.tex):

- `\title{...}`
- `\subtitle{...}` (opcional)
- `\author{...}`
- `\institute{...}`
- `\date{...}`
- `\newcommand{\orientador}{...}`

### 2) Logos da capa
No [modelo.tex](modelo.tex), ajuste:

```tex
\SetupCustomTitle{logo_feec.png}{logo_dspcom.pdf}{unicamp-logotipo.pdf}
```

A ordem dos argumentos e:

1. Logo do instituto
2. Logo do laboratório/grupo
3. Logo da universidade

Se um arquivo não existir, ele é ignorado automaticamente.

### 3) Imagens
Coloque imagens em [figuras/](figuras/) e subpastas.

Use a macro:

```tex
\FigureWithFallbackCaption{arquivo.png}{Legenda da figura.}
```

Se a imagem não existir, o slide mostra um placeholder no lugar.

### 4) Pausas e destaque de conteudo
Macros úteis em [styles/elegantmacros.sty](styles/elegantmacros.sty):

- `\BlockPause{Titulo}{conteudo}`
- `\EquationPause{...}`
- `\FigureWithFallbackCaption{path}{Legenda}`

## Fluxo sugerido

1. Duplica [modelo.tex](modelo.tex) para um arquivo com o nome da sua apresentação;
2. Ajusta metadados e logos da capa;
3. Organiza seções e frames;
4. Adiciona figuras e referências no [references.bib](references.bib).
