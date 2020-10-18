# tex_template
LaTeX preamble I start papers with

```tex
\documentclass{article}
\usepackage[utf8]{inputenc}

% Save symbols between packages
\usepackage{savesym}

% Change the font:
\usepackage{newtxtext,newtxmath}
%\usepackage[english]{babel}

%Set the margins:
\usepackage[letterpaper, margin=1in]{geometry}
\usepackage{graphicx}
\usepackage{bm}%Bold face math

%Fancy letterings for number sets
% (already imported by newtxtmath
%\usepackage{amssymb}

%Good alignment
\usepackage{amsmath}

%Add numbers to each line:
\usepackage{lineno}
\linenumbers

%Bra's and ket's; derivatives (\dv[n]{Q}{t})
\usepackage{physics}

% professional-quality tables
\usepackage{booktabs}

\usepackage{cancel}%Cancel out math terms
\usepackage{enumerate}%For lists
\usepackage{calligra} %Griffith's r kind of 
\usepackage{mathtools} %pmatrix
\usepackage{multicol}
\usepackage{lipsum}% dummy text
\usepackage{titlesec}
\usepackage{pgf}
\usepackage{color}

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

\setlength{\columnseprule}{0.4pt}

% Make sections small
\titleformat*{\section}{\small\bfseries}
\titleformat*{\subsection}{\small\bfseries}
\titleformat*{\subsubsection}{\small\bfseries}
\titleformat*{\paragraph}{\large\bfseries}
\titleformat*{\subparagraph}{\large\bfseries}

\setlength{\columnseprule}{0.4pt}
\newcommand{\im}{\Rightarrow}
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
\renewcommand\v\mathbf
\newcommand{\dbar}{d\hspace*{-0.08em}\bar{}\hspace*{0.1em}}
%To do derivatives: \dv{Q}{t} (physics package); or \pdv{Q}{t} for partial. \dv[n]{Q}{t} for multiple derivatives.
% Read full physics package; many commands: http://mirrors.ibiblio.org/CTAN/macros/latex/contrib/physics/physics.pdf

% Write C++ this way
\usepackage{relsize}
\newcommand\cpp{C\nolinebreak[4]\hspace{-.05em}\raisebox{.4ex}{\relsize{-3}{\textbf{++}}} }
\newcommand\cppnospace{C\nolinebreak[4]\hspace{-.05em}\raisebox{.4ex}{\relsize{-3}{\textbf{++}}}}

%Nicer typewriter font
\usepackage{inconsolata}
\usepackage{ragged2e} %Causes text to break inside margins, e.g., for labels
\usepackage{cleveref} %Must be loaded as late as possible

% Gives link names:
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
\renewcommand\t\text


% For Bayesian graphical models:
\usepackage{tikz}
\savesymbol{plate}
\usetikzlibrary{bayesnet}

% Define algorithm
\usepackage{algorithm}
\usepackage[noend]{algpseudocode}
\newcommand{\algorithmautorefname}{Algorithm}
\renewcommand{\subsectionautorefname}{Section}


\title{Title}
\author{Miles Cranmer}
\date{}
\newcommand{\todo}[1]{{\color{purple}TODO: #1}}

\begin{document}

\maketitle

\section{Introduction}
\label{sec:intro}
Test















% Example algorithm
\begin{comment}
\begin{algorithm}[t]
\caption{}
\begin{algorithmic}[1]
\Procedure{Learn}{}
\State $\theta_1 \gets \text{Kaiming initialization}$
\State $\theta_2 \gets  \text{Kaiming initialization}$
\State $\lambda \gets \text{learning rate}$
\State $H \gets \text{total resource allocation}$
\Repeat
    \State $\varphi \sim p(\varphi)$ \Comment{parameter of simulated environment}
    \ForAll{$i=1\ldots|\{\mathbf{v}_i\}|$} 
        \State $\mathbf{v}'_i\gets \mathbf{v}_i+\epsilon$
    \EndFor
    \State $L \gets (\hat{\varphi} - \varphi)^2$
    \If{$\sum_i \ldots $}
        \State $\tau \gets $
    \EndIf
\Until{$L$ has stabilized}\\
\Return{Trained model}
\EndProcedure
\end{algorithmic}
\end{algorithm}
\end{comment}

% Example graphical model:
\begin{comment}
\begin{tikzpicture}
    \node[obs] (x) {$\v x_{0}$} ; %
    \node[latent, xshift=-3cm] (t) {$\theta$} ; %
    \node[latent, xshift=-0.5cm, below=of x] (m) {$\mu$} ; %
    \node[latent, xshift=0.5cm, below=of x] (s) {$\sigma$} ; %
    \node[obs, below=of s, xshift=-0.5cm] (T) {$T$} ; %
    \plate {p1} {(T)(x)(s)(m)} {$\forall i\in\{1..N\}$};
    \edge {t,x} {m,s} ; %
    \edge {m,s} {T} ; %
\end{tikzpicture}
\end{comment}


\end{document}

```
