# LostMa LaTeX Presentation Template

This repository contains a Beamer template for presentations given as part of the LostMa project.

## Download
To use the template, download the files in the `src/` folder. Unless you want to contribute to the template, it's best if you do not `git clone` the repository, especially if your presentation is in a folder already with a git history. Instead, download only the `src/` folder by clicking on this [link](https://download-directory.github.io/?url=https%3A%2F%2Fgithub.com%2FLostMa-ERC%2Flatex-beamer-template%2Ftree%2Fmain%2Fsrc) from [download-directory.github.io](https://download-directory.github.io). This will download a compressed file containing to your computer's regular downloads folder. Except for Windows, computers will have the downloads folder at `~/Downloads` if its language is English (or `~/Téléchargements` if French).

Finally, move (`mv`) the downloaded file, then decompress (`unzip`) it.

```shell
$ mv ~/Downloads/LostMa-ERC\ latex-beamer-template\ main\ src.zip ./download.zip
$ unzip ./download.zip -d ./template
```


## How-To
To get started modify the [`main.tex`](src/main.text) file in your downloaded `template/` folder. Like all LaTeX documents, the `main.tex` file is the root of everything.

1. Change the `main.tex` file's preamble to include your presentation's title, subtitle, date, and your name.

[`template/main.tex`](src/main.tex)

```latex
%%% Modify the presentation's bibliographic details
\title{Title}
\subtitle{Subtite}
\date{Date}
\author[Firstname Lastname]{Name}
\institute[ENC]
{
  LostMa\\
  École nationale des chartes
}
```

---

2. Add sections to your presentation using LaTeX's `\section{}` and `\input{}` commands. The former gives a name to the section and the latter points to the LaTeX file within the template's sub-directory `sections`, which will contain the actual content of the section's slides.

[`template/main.tex`](src/main.tex)
```latex
\section{Section 1}
\input{sections/first}
```

---

3. In the section files, add slides to your presentation with the `\begin{frame}{}` command. (Note: You don't need to add any preamble, `\begin{document}`, etc. All of that is in the `main.tex` file. The imported file simply has the beamer slides you want in that section.)

[`template/sections/first.tex`](src/sections/first.tex)
```latex
\begin{frame}{Description}
    \lipsum[1]
\end{frame}
```

---

4. If you want to add subsections, add them to the section file.

[`template/sections/first.tex`](src/sections/first.tex)
```latex
\subsection{Description}

\begin{frame}{Description of Problem}
    \lipsum[1]
\end{frame}
```
---