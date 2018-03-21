1. [Background Info](#background-info)
2. [LaTeX Intro](#latex-intro)
3. [TeX and LaTeX](#tex-and-latex)
4. [Let's Begin!](#lets-begin)
5. [Formatting Basics](#formatting-basics)
6. [Let's not get aHEAD of ourselves!](#lets-not-get-ahead-of-ourselves)
7. [Section Formatting](#section-formatting)
8. [Equation Formatting](#equation-formatting)
9. [List Formatting](#list-formatting)
10. [Table Formatting](#table-formatting)
11. [Images](#images)
12. [Embedded Bibliography](#embedded-bibliography)
13. [Bibliography with Natbib](#bibliography-with-natbib)
14. [LaTeX vs. WYSIWYG](#latex-vs-wysiwyg)
15. [Who Uses LaTeX?](#who-uses-latex)

### Background Info

- Developed by Leslie Lamport
- Released in 1985
- Free document preparation system (typesetting) 
- Built off of a system known as TeX (released in 1978 by Donald Knuth)

[Back to Top](#latex)

### LaTeX Intro

- Uses plain text, as opposed to formatted text of WYSIWYG word processors
- Uses markup tagging conventions to define structure and stylize text
- Emphasizes content, rather than style
- Includes features designed for the production of technical and scientific documentation
- Easier way to use TeX

[Back to Top](#latex)

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

[Back to Top](#latex)

### Let's Begin!

```latex
\documentclass{article}
\begin{document}
Here is my text
\end{document}
```
![letsbegin](https://i.imgur.com/FXz04fM.png)

[Back to Top](#latex)

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

[Back to Top](#latex)

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

[Back to Top](#latex)

### Section Formatting

```latex
\section{Introduction}

\subsection{Abstract}
This lab was conducted to examine terminal velocity, the limiting case in the assumption of uniform acceleration where the force of air resistance (drag force) is equal to that of gravity.

\section*{Methods}
```
![sectionformatting](https://i.imgur.com/PmtzByc.png)

[Back to Top](#latex)

### Equation Formatting

```latex
\section{Introduction}

When an object reaches its terminal velocity while falling in air under the influence of gravity, we can state that:
$$F_g = F_d$$
\[mg = \frac{1}{2}\rho ACv^n\]
where $\rho$ is the density of air, $A$ is the cross-section of the object, $C$ is the undetermined drag component, and $v^n$ is the velocity raised to some power. In this lab, we will be measuring $m$ and $v$, looking up $\rho$, and determining the values of $C$ and $n$.
```
![equationformatting](https://i.imgur.com/HeF4KDA.png)

[Back to Top](#latex)

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

[Back to Top](#latex)

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

[Back to Top](#latex)

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

[Back to Top](#latex)

### Embedded Bibliography

```latex
[ADD CODE HERE]
```
![embeddedbibliography](https://i.imgur.com/xjl4py6.png)

[Back to Top](#latex)

### Bibliography with Natbib

```latex
[ADD CODE HERE]
```
![bibliographywithnatbib](https://i.imgur.com/UqYAVZo.png)

[Back to Top](#latex)

### LaTeX vs. WYSIWYG

Advantages of WYSIWYG
- Word documents allow for better collaboration among authors with commenting systems
- Built in grammar/spell check
- Easier for just quickly jotting down notes

[Back to Top](#latex)

### Who Uses LaTeX?

- LaTeX  is often used to write scientific papers in many topics such as statistics, economics, chemistry, physics, and computer science
- It is used by employees in tech companies, such as Google and AgileBits, when making PDFs to present to colleagues 
- LaTeX documents can also be converted to other formats, like HTML, making it easy to share

[Back to Top](#latex)
