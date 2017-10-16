# tex_template
LaTeX preamble I start papers with

```tex
\documentclass{article}
\usepackage[letterpaper, landscape, margin=0.3in]{geometry}
\usepackage[utf8]{inputenc}
\usepackage{bm}%Bold face math
\usepackage{physics}%Bra's and ket's
\usepackage{cancel}%Cancel out math terms
\usepackage{enumerate}%For lists
\usepackage{amssymb}%Fancy letterings for number sets
\usepackage{amsmath}%Good alignment
\usepackage{comment} %Commenting out code
\usepackage{calligra} %Griffith's r kind of 
\usepackage{mathtools} %pmatrix
\usepackage{multicol}
\usepackage{lipsum}% dummy text
\usepackage{titlesec}
\usepackage{pgf}

%Nice code syntax highlighting
\usepackage{minted}
\usepackage{booktabs}
\usepackage[flushleft]{threeparttable}

% Link between sections
\usepackage[breaklinks,linktoc=all,colorlinks,urlcolor=blue,citecolor=blue,linkcolor=blue]{hyperref}

% Write large comments
\usepackage{comment}
\usepackage{pgfpages}

% Save symbols between packages
\usepackage{savesym}


% For units
\savesymbol{tablenum}
\usepackage{siunitx}
\restoresymbol{SIX}{tablenum}

% Use \todo macro
\usepackage[colorinlistoftodos]{todonotes}

\setlength{\columnseprule}{0.4pt}

% Make sections small
\titleformat*{\section}{\small\bfseries}
\titleformat*{\subsection}{\small\bfseries}
\titleformat*{\subsubsection}{\small\bfseries}
\titleformat*{\paragraph}{\large\bfseries}
\titleformat*{\subparagraph}{\large\bfseries}

\setlength{\columnseprule}{0.4pt}
\newcommand{\im}{\Rightarrow}
\renewcommand{\t}{\theta}
\DeclareMathAlphabet{\mathcalligra}{T1}{calligra}{m}{n}
\DeclareFontShape{T1}{calligra}{m}{n}{<->s*[2.2]callig15}{}
\newcommand{\scriptr}{\mathcalligra{r}\,}
% Some definitions to make math easier
\newcommand{\ot}{\theta}
\renewcommand{\d}{\text{d}}
\renewcommand{\o}{\theta}
\newcommand{\bv}[1]{\bm{\mathrm{#1}}}
\newcommand{\f}[2]{\frac{#1}{#2}}
\newcommand{\s}{\sin}
\renewcommand{\c}{\cos}
\renewcommand{\l}{\left(}
\renewcommand{\r}{\right)}
\newcommand{\sr}{\pmb{\scriptr}}
\newcommand{\uv}[1]{\bv{\hat{#1}}}
\renewcommand{\pv}[3]{#1\uv{x} #2 \uv{y} #3 \uv{z}}
\renewcommand{\k}{\f{1}{4\pi\epsilon_0}}
\DeclareMathOperator{\sgn}{sgn}
\newcommand{\inv}[1]{\f{1}{#1}}
\renewcommand{\d}{\text{d}}
\newcommand{\go}{\rightarrow}
\newcommand{\ans}[1]{\problemAnswer{#1}}
\newcommand{\Int}{\int\limits}
\renewcommand{\v}{\vec}
\newcommand{\df}[2]{\frac{\partial #1}{\partial #2}}
\newcommand{\dfc}[3]{\left(\df{#1}{#2}\right)_{#3}}
\newcommand{\dfcn}[4]{\left(\frac{\partial^{#4} #1}{\partial #2^{#4}}\right)_{#3}}
\newcommand{\dbar}{d\hspace*{-0.08em}\bar{}\hspace*{0.1em}}

% Write C++ this way
\usepackage{relsize}
\newcommand\cpp{C\nolinebreak[4]\hspace{-.05em}\raisebox{.4ex}{\relsize{-3}{\textbf{++}}} }
\newcommand\cppnospace{C\nolinebreak[4]\hspace{-.05em}\raisebox{.4ex}{\relsize{-3}{\textbf{++}}}}

%Nicer typewriter font
\usepackage{inconsolata}
\usepackage{ragged2e} %Causes text to break inside margins, e.g., for labels
\usepackage{cleveref} %Must be loaded as late as possible
\usepackage[notref,notcite]{showkeys} %Displays figure labels. Turn off (with clean) for final draft


\renewcommand*{\showkeyslabelformat}[1]{%Causes text to break inside margins, e.g., for labels
  \expandafter\def\expandafter\UrlBreaks\expandafter{\UrlBreaks%  save the current one
  \do\a\do\b\do\c\do\d\do\e\do\f\do\g\do\h\do\i\do\j%
  \do\k\do\l\do\m\do\n\do\o\do\p\do\q\do\r\do\s\do\t%
  \do\u\do\v\do\w\do\x\do\y\do\z\do\A\do\B\do\C\do\D%
  \do\E\do\F\do\G\do\H\do\I\do\J\do\K\do\L\do\M\do\N%
  \do\O\do\P\do\Q\do\R\do\S\do\T\do\U\do\V\do\W\do\X%
  \do\Y\do\Z}%
  \fbox{\vbox{\hsize=1cm\RaggedRight\noindent\normalfont\small\url{#1}\par}}}

\makeatletter
  \SK@def\Cref#1{\SK@\SK@@ref{#1}\SK@Cref{#1}}%Displays figure labels for cref
\makeatother

%For inline code.
\definecolor{codegray}{gray}{0.885}
\newmintinline[python]{python}{bgcolor=codegray,fontsize=\small}


```
