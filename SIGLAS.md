# Sistema de Siglas Automático

O UFRTeX agora inclui um sistema automático para definição e uso de siglas/abreviaturas.

## Como Usar

### 1. Definindo Siglas

Abra o arquivo `_configuracoes/siglas.tex` e adicione suas siglas usando o comando `\definesigla`:

```latex
\definesigla{SIGLA}{Definição completa da sigla}
```

**Exemplos:**
```latex
\definesigla{UFRON}{Universidade Federal de Rondonópolis}
\definesigla{TCC}{Trabalho de Conclusão de Curso}
\definesigla{ABNT}{Associação Brasileira de Normas Técnicas}
\definesigla{NBR}{Norma Brasileira}
```

### 2. Usando Siglas no Texto

No texto do seu documento, use o comando `\sigla{}` para referenciar uma sigla:

```latex
Este é meu \sigla{TCC} da \sigla{UFRON}, seguindo as normas da \sigla{ABNT}.
```

### 3. Lista Automática

As siglas definidas são automaticamente incluídas na lista de abreviaturas e siglas do documento, com links clicáveis.

## Vantagens

- ✅ **Automático**: Não precisa adicionar manualmente na lista
- ✅ **Links**: Clique na sigla para ir à lista de definições
- ✅ **Centralizado**: Todas as siglas ficam em um arquivo só
- ✅ **Compatível**: Funciona com o sistema manual também

## Avisos

- Se usar uma sigla não definida, você receberá um aviso durante a compilação
- Evite usar siglas que conflitem com comandos LaTeX existentes (ex: `\UFR` já existe)
- Para compilação completa com links, execute o pdflatex duas vezes

## Sistema Legado

O sistema manual ainda funciona. Se preferir, pode adicionar siglas manualmente no arquivo `1-pre-textual/listas.tex` usando:

```latex
\begin{siglas}
  \item[SIGLA] Definição da sigla
\end{siglas}
```