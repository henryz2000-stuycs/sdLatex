### Background Info

- Developed by Leslie Lamport
- Released in 1985
- Free document preparation system (typesetting) 
- Built off of a system known as TeX (released in 1978 by Donald Knuth)

[Back to Top](#background-info)

---

### LaTeX Intro

- Uses plain text, as opposed to formatted text of WYSIWYG word processors
- Uses markup tagging conventions to define structure and stylize text
- Emphasizes content, rather than style
- Includes features designed for the production of technical and scientific documentation
- Easier way to use TeX

[Back to Top](#background-info)

---

### TeX and LaTeX

- TeX: Macro- and token- based language and typesetting system; focus on formatting
- LaTeX: script-like user interface to the binary TeX program, considered a higher-level language; focus on content
- LaTeX commands are just complicated sets of TeX commands underneath AKA “macros”
  - Includes setting up sections, title pages, bibliographies

```tex
\TeX{} is good at typesetting words like `fjord', `efficiancy',
and `fiasco'. It is also good at typesetting math like,
$a^2 + b^2 = c^2$.
\bye
```
![tex](https://cdn.sharelatex.com/blog/images/tex-example.png)

[Back to Top](#background-info)

---

### Let's Begin!

```latex
\documentclass{article}
\begin{document}
Here is my text
\end{document}
```
![letsbegin](https://i.imgur.com/FXz04fM.png)

[Back to Top](#background-info)

---

### Formatting Basics

```latex
\textbf{argument}
\textit{argument}
\underline{argument}
\tiny{argument}
\small{argument}
\large{argument}
\huge{argument}
```
![formattingbasics](https://i.imgur.com/OjZBkUu.png)

[Back to Top](#background-info)

---

### Let's not get aHEAD of ourselves!

```latex
\documentclass{article}

\title{Lab One: Terminal Velocity and Drag Force}
\author{John Doe and Jane Doe\\Period 9/10}
\date{October 16, 2017}

\begin{document}
\maketitle
\end{document}
```
![letsnotgetaheadofourselves](https://i.imgur.com/sYaEEbI.png)

[Back to Top](#background-info)

---

### Section Formatting

```latex
\section{Introduction}

\subsection{Abstract}
This lab was conducted to examine terminal velocity, the limiting case in the assumption of uniform acceleration where the force of air resistance (drag force) is equal to that of gravity.

\section*{Methods}
```
![sectionformatting](https://i.imgur.com/PmtzByc.png)

[Back to Top](#background-info)

---

### Equation Formatting

```latex
\section{Introduction}

When an object reaches its terminal velocity while falling in air under the influence of gravity, we can state that:
$$F_g = F_d$$
\[mg = \frac{1}{2}\rho ACv^n\]
where $\rho$ is the density of air, $A$ is the cross-section of the object, $C$ is the undetermined drag component, and $v^n$ is the velocity raised to some power. In this lab, we will be measuring $m$ and $v$, looking up $\rho$, and determining the values of $C$ and $n$.
```
![equationformatting](https://i.imgur.com/HeF4KDA.png)

[Back to Top](#background-info)

---

### List Formatting

```latex
\begin{itemize}
  \item Begin each bulleted list with a begin\{itemize\} command.
  \item Add your list items using the list command.
  \item Don't forget to end your list.
\end{itemize}

\begin{enumerate}
  \item Begin each enumerated list with a begin\{enumerate\} command.
  \item Add your list items using the list command.
  \item Don't forget to end your list.
\end{enumerate}
```
![listformatting](https://i.imgur.com/FFTGFzj.png)

[Back to Top](#background-info)

---

### Table Formatting

```latex
\begin{center}
\begin{tabular}{ c c c }
 cell1 & cell2 & cell3 \\ 
 cell4 & cell5 & cell6 \\  
 cell7 & cell8 & cell9    
\end{tabular}
\end{center}

\begin{center}
\begin{tabular}{ c|c|c } 
 cell1 & cell2 & cell3 \\
 \hline
 cell4 & cell5 & cell6 \\ 
 \hline
 cell7 & cell8 & cell9 \\ 
\end{tabular}
\end{center}
```
![tableformatting1](https://i.imgur.com/F8kX60D.png)

```latex
\begin{center}
\begin{tabular}{ |c|c|c| } 
 \hline
 cell1 & cell2 & cell3 \\ 
 cell4 & cell5 & cell6 \\ 
 cell7 & cell8 & cell9 \\ 
 \hline
\end{tabular}
\end{center}

\begin{center}
\begin{tabular}{ |c|c|c| } 
 \hline
 cell1 & cell2 & cell3 \\
 \hline
 cell4 & cell5 & cell6 \\ 
 \hline
 cell7 & cell8 & cell9 \\ 
 \hline
\end{tabular}
\end{center}
```
![tableformatting2](https://i.imgur.com/gaGueR9.png)

[Back to Top](#background-info)

---

### Images

```latex
\begin{figure}[h!]
\centering
\includegraphics[scale=1.7]{universe.jpg}
\caption{The Universe}
\label{fig:univerise}
\end{figure}
```
![images](https://i.imgur.com/RzLwLjd.png)

[Back to Top](#background-info)

---

### Embedded Bibliography

```latex
\section{In-Text Citations} 
``Michel Goossens and Frank Mittelbach and Alexander Samarin``
\citep{latexcompanion} \\
``J.K. Rowling``
\citep{rowling} \\
``Albert Einstein``
\citep{einstein} \\
``Donald Knuth``
\citep{knuthwebsite} \\
 
\begin{thebibliography}{9}
 
\bibitem{einstein} 
Albert Einstein. 
Zur Elektrodynamik bewegter K{\"o}rper. (German) 
[On the electrodynamics of moving bodies]. 
\textit{Annalen der Physik}, 322(10):891–921, 1905.

\bibitem{latexcompanion} 
Michel Goossens, Frank Mittelbach, and Alexander Samarin. 
\textit{The \LaTeX\ Companion}. 
Addison-Wesley, Reading, Massachusetts, 1993.

\bibitem{knuthwebsite} 
Donald Knuth.
Knuth: Computers and Typesetting.

\bibitem{rowling}
J.K. Rowling.
\textit{Harry Potter and the Sorcerer's Stone}.
London: Bloomsburg Children, 2001.

\end{thebibliography}
```
![embeddedbibliography](https://i.imgur.com/xjl4py6.png)

[Back to Top](#background-info)

---

### Bibliography with Natbib

```latex
\usepackage{natbib}

\begin{document}

\section{In-Text Citations} 
``Michel Goossens and Frank Mittelbach and Alexander Samarin``
\citep{latexcompanion} \\
``J.K. Rowling``
\citep{rowling} \\
``Albert Einstein``
\citep{einstein} \\
``Donald Knuth``
\citep{knuthwebsite}

\bibliographystyle{plain}
\bibliography{references}
\end{document}
```
References.bib
```latex
@book{rowling,
  title =            "Harry Potter and the Sorcerer's Stone",
  author =           "Rowling, J.K.",
  year =             "2001",
  publisher =        "London: Bloomsburg Children"
}
 
@article{einstein,
    author =       "Albert Einstein",
    title =        "{Zur Elektrodynamik bewegter K{\"o}rper}. ({German})
        [{On} the electrodynamics of moving bodies]",
    journal =      "Annalen der Physik",
    volume =       "322",
    number =       "10",
    pages =        "891--921",
    year =         "1905",
    DOI =          "http://dx.doi.org/10.1002/andp.19053221004"
}
 
@book{latexcompanion,
    author    = "Michel Goossens and Frank Mittelbach and Alexander Samarin",
    title     = "The \LaTeX\ Companion",
    year      = "1993",
    publisher = "Addison-Wesley",
    address   = "Reading, Massachusetts"
}
 
@misc{knuthwebsite,
    author    = "Donald Knuth",
    title     = "Knuth: Computers and Typesetting",
    url       = "http://www-cs-faculty.stanford.edu/\~{}uno/abcde.html"
}
```
![bibliographywithnatbib](https://i.imgur.com/UqYAVZo.png)

[Back to Top](#background-info)

---

### LaTeX vs. WYSIWYG

Advantages of WYSIWYG
- Word documents allow for better collaboration among authors with commenting systems
- Built in grammar/spell check
- Easier for just quickly jotting down notes

[Back to Top](#background-info)

---

### Who Uses LaTeX?

- LaTeX  is often used to write scientific papers in many topics such as statistics, economics, chemistry, physics, and computer science
- It is used by employees in tech companies, such as Google and AgileBits, when making PDFs to present to colleagues 
- LaTeX documents can also be converted to other formats, like HTML, making it easy to share

[Back to Top](#background-info)
