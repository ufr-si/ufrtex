![TEMPLATE PARA TRABALHOS ACADÊMICOS DA UFR](https://user-images.githubusercontent.com/385329/186760202-a59f1fa0-d38d-4b05-a1f9-24239a0d1f84.png)
# UFRTeX: Template para Trabalhos Acadêmicos da Universidade Federal de Rondonópolis

Este é um template em TeX para a elaboração de trabalhos acadêmicos da Universidade Federal de Rondonópolis. Atualmente, suporta a elaboração de trabalhos de graduação.

Para utilizar, você pode simplesmente copiar este repositório e alterar as informações necessárias para elaborar seu documento, ou baixar o zip do release mais recente.

## Markdown

O pacote `markdown` é carregado em modo híbrido, permitindo misturar Markdown e comandos LaTeX no documento. Use um bloco diretamente no arquivo `.tex`:

```latex
\begin{markdown}
# Título

Texto em **Markdown**, com uma citação LaTeX \cite{chave}.
\end{markdown}
```

Ou inclua um arquivo Markdown:

```latex
\inputMarkdown{2-capitulos/introducao.md}
```

O comando `\markdownInput{...}` do pacote também está disponível.

As citações LaTeX continuam usando a bibliografia do template (`bibliografia.bib`). A compilação precisa permitir shell escape; por exemplo, use `pdflatex --shell-escape ufr-tcc.tex` e habilite essa opção nas configurações do seu editor online.
