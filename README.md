\documentclass{article}

\usepackage{fancyhdr}
\usepackage{extramarks}
\usepackage{amsmath}
\usepackage{amsthm}
\usepackage{amsfonts}
\usepackage{tikz}
\usepackage[plain]{algorithm}
\usepackage{algpseudocode}
\usepackage{latexsym}
\usepackage{amssymb}
\usepackage{circuitikz}
\usepackage{tikz}
\usetikzlibrary{circuits.logic.US}
\usetikzlibrary{positioning}

\usetikzlibrary{automata,positioning}

%
% Basic Document Settings
%

\topmargin=-0.45in
\evensidemargin=0in
\oddsidemargin=0in
\textwidth=6.5in
\textheight=9.0in
\headsep=0.25in

\linespread{1.1}

\pagestyle{fancy}
\lhead{\hmwkAuthorName}
\chead{\hmwkClass\ (\hmwkClassInstructor\ \hmwkClassTime): \hmwkTitle}
\rhead{\firstxmark}
\lfoot{\lastxmark}
\cfoot{\thepage}

\renewcommand\headrulewidth{0.4pt}
\renewcommand\footrulewidth{0.4pt}

\setlength\parindent{0pt}

%
% Create Problem Sections
%

\newcommand{\enterProblemHeader}[1]{
    \nobreak\extramarks{}{Problem \arabic{#1} continued on next page\ldots}\nobreak{}
    \nobreak\extramarks{Problem \arabic{#1} (continued)}{Problem \arabic{#1} continued on next page\ldots}\nobreak{}
}

\newcommand{\exitProblemHeader}[1]{
    \nobreak\extramarks{Problem \arabic{#1} (continued)}{Problem \arabic{#1} continued on next page\ldots}\nobreak{}
    \stepcounter{#1}
    \nobreak\extramarks{Problem \arabic{#1}}{}\nobreak{}
}

\setcounter{secnumdepth}{0}
\newcounter{partCounter}
\newcounter{homeworkProblemCounter}
\setcounter{homeworkProblemCounter}{1}
\nobreak\extramarks{Problem \arabic{homeworkProblemCounter}}{}\nobreak{}

\newenvironment{homeworkProblem}{
    \section{Problem \arabic{homeworkProblemCounter}}
    \setcounter{partCounter}{1}
    \enterProblemHeader{homeworkProblemCounter}
}{
    \exitProblemHeader{homeworkProblemCounter}
}

%
% Homework Details
%   - Title
%   - Due date
%   - Class
%   - Section/Time
%   - Instructor
%   - Author
%

\newcommand{\hmwkTitle}{Assignment\ \#2}
\newcommand{\hmwkDueDate}{September 03, 2014}
\newcommand{\hmwkClass}{ICS141}
\newcommand{\hmwkClassTime}{62092}
\newcommand{\hmwkClassInstructor}{Professor David Maxson}
\newcommand{\hmwkAuthorName}{Kawika Kekahuna}

%
% Title Page
%

\title{
    \vspace{2in}
    \textmd{\textbf{\hmwkClass:\ \hmwkTitle}}\\
    \normalsize\vspace{0.1in}\small{Due\ on\ \hmwkDueDate\ at 3:10pm}\\
    \vspace{0.1in}\large{\textit{\hmwkClassInstructor\ \hmwkClassTime}}
    \vspace{3in}
}

\author{\textbf{\hmwkAuthorName}}
\date{}

\renewcommand{\part}[1]{\textbf{\large Part \Alph{partCounter}}\stepcounter{partCounter}\\}

%
% Various Helper Commands
%

% Useful for algorithms
\newcommand{\alg}[1]{\textsc{\bfseries \footnotesize #1}}

% For derivatives
\newcommand{\deriv}[1]{\frac{\mathrm{d}}{\mathrm{d}x} (#1)}

% For partial derivatives
\newcommand{\pderiv}[2]{\frac{\partial}{\partial #1} (#2)}


% Integral dx
\newcommand{\dx}{\mathrm{d}x}

% Alias for the Solution section header
\newcommand{\solution}{\textbf{\large Solution}}

% Probability commands: Expectation, Variance, Covariance, Bias
\newcommand{\E}{\mathrm{E}}
\newcommand{\Var}{\mathrm{Var}}
\newcommand{\Cov}{\mathrm{Cov}}
\newcommand{\Bias}{\mathrm{Bias}}


\begin{document}

\maketitle

\pagebreak

\begin{homeworkProblem}
    Write the truth table for the statement p$\wedge$($\sim$q$\vee$ r):

\begin{table}[ht]
\caption{Truth Table for p$\wedge$($\sim$q$\vee$ r)} % title of Table
\centering % used for centering table
\begin{tabular}{c c c c c c} % centered columns (5 columns)
\hline\hline %inserts double horizontal lines
P & Q & R & $(\sim$q$\vee$r) & p$\wedge$$(\sim$q$\vee$r)\\ [0.5ex] % inserts table 
%heading
\hline % inserts single horizontal line
T & T & T & F & F \\ % inserting body of the table
T & T & F & T & T \\
T & F & T & T & T  \\
T & F & F & F & F \\
F & T & T & F & F \\
F & T & F & T & F \\
F & F & T & T & F \\
F & F & F & F & F \\[1ex]
\hline %inserts single line
\end{tabular}
\label{table:nonlin} % is used to refer this table in the text
\end{table}
--------------------- 



\end{homeworkProblem}



\begin {homeworkProblem}
	Use De Morgan\rq{}s law to write the negation for the statement \lq\lq{}The dollar is at an all-time high and the stock is at a record low.\rq\rq{}

	    \textbf{Part One}

	
	Let p = Dollar at all time high \\
	Let q = Stock at record low \\
	\\
	De Morgan\rq{}s law states that an \(and\)  statement is logically equivilated to the \(or\) statement in which each premise is negated. \\
	\\
	p = $\sim$p 	\\
	q = $\sim$q	\\
	\\
	Therefor, the dollar is \(not\) at an all-time high and the stock record is \(not\) at an all time low. \\
	
	
\end{homeworkProblem}

\begin{homeworkProblem}
    Write the truth table for the statement (p$\vee$q)$\vee$($\sim$p$\wedge$q)$\rightarrow$ q:

\begin{table}[ht]
\caption{Truth Table for (p$\vee$q)$\vee$($\sim$p$\wedge$q)$\rightarrow$ q}% title of Table
\centering % used for centering table
\begin{tabular}{c c c c c c} % centered columns (5 columns)
\hline\hline %inserts double horizontal lines
p & q & p$\vee$q & $\sim$p$\wedge$q & p$\wedge$ q & (p$\vee$q)$\vee$($\sim$p$\wedge$q)\\ [0.5ex] % inserts table 
%heading
\hline % inserts single horizontal line
T & T & T & F & T & T\\ % inserting body of the table
T & F & T & T & T & F \\
F & T & T & T & T & T  \\
F & F & F & F & F & T \\
\hline %inserts single line
\end{tabular}
\label{table:nonlin} % is used to refer this table in the text
\end{table}
--------------------- 

\end{homeworkProblem}
\begin{homeworkProblem}
Write each of the following three statements in symbolic
form and determine which pairs are logically equivalent.
Include truth tables and a few words of explanation.
\\

\textit {If it walks like a duck and it talks like a duck, then it is
a duck. }\\
\textbf{p$\wedge$q$\rightarrow$r}

\textit {Either it does not walk like a duck or it does not talk
like a duck, or it is a duck. }
\textbf{p$\vee$q$\rightarrow$r}
\\

\textit{If it does not walk like a duck and it does not talk like
a duck, then it is not a duck.}
\textbf{$\sim$p$\wedge$$\sim$q$\rightarrow$$\sim$r}
\\
\textbf{Let p = walks like a duck\\
Let q = talks like a duck\\
Let r = is a duck}
 \\
\begin{table}[ht]
\caption{Truth Table for Duck Statements}% title of Table
\centering % used for centering table
\begin{tabular}{c c c c c c c c c c c} % centered columns (5 columns)
\hline\hline %inserts double horizontal lines
p & q & r & p$\wedge$q & $\sim$p$\vee$$\sim$q & $\sim$p$\wedge$$\sim$q & ($\sim$p$\vee$$\sim$q)$\rightarrow$r & p$\wedge$q$\rightarrow$r & $\sim$p$\vee$$\sim$q$\rightarrow$$\sim$r\\ [0.5ex] % inserts table 
%heading
\hline % inserts single horizontal line
T & T & T & T & T & T & T & T & F\\ % inserting body of the table
T & T & F & T & F & T & T & F & T\\ % inserting body of the table
T & F & T & F & T & F & T & F & T\\ % inserting body of the table
T & F & F & F & T & F & F & T & F\\ % inserting body of the table
F & T & T & F & T & T & T & F & T\\ % inserting body of the table
F & T & F & F & T & T & T & T & F\\ % inserting body of the table
F & F & T & F & T & T & T & F & T\\ % inserting body of the table
F & F & F & F & T & F &F & T & F\\ % inserting body of the table
\hline %inserts single line
\end{tabular}
\label{table:ducktable} % is used to refer this table in the text
\end{table}
\\
Ultimately, since ($\sim$p$\wedge$$\sim$q)$\rightarrow$r and p$\wedge$q$\rightarrow$r share the same outcomes in the truth table, the forms are logically equivilent. DONOTSUBMIT NEED TO FIX
\end{homeworkProblem}

\begin{homeworkProblem}
Use the truth tables to establish the truth of the following statement:\\
\textit {The converse and inverse of a conditional statement are logically equivalent to each other.}\\
\begin{table}[ht]
\caption{Truth Table for Converse and Inverse Relationship} % title of Table
\centering % used for centering table
\begin{tabular}{c c c c c } % centered columns (5 columns)
\hline\hline %inserts double horizontal lines
p & q & p$\rightarrow$q & $\sim$p$\rightarrow$$\sim$q\\ [0.5ex] % inserts table 
%heading  
\hline % inserts single horizontal line
T & T & T & T \\ % inserting body of the table
T & F & F & F \\
F & T & F & F \\
F & F & T & T \\

\hline %inserts single line
\end{tabular}
\label{table:nonlin} % is used to refer this table in the text
\end{table}
\textbf{p$\rightarrow$q has the same truth table outcomes as $\sim$p$\rightarrow$$\sim$q, therefor they are logically equivilent. }
\\
--------------------- 

\end{homeworkProblem}
\pagebreak
\begin {homeworkProblem}
Use truth tables to determine whether the following argument form is valid. Indicate which columns represent the premises and
which represent the conclusion, and include a sentence explaining
how the truth table supports your answer. Your explanation
should show that you understand what it means for a form of
argument to be valid or invalid.

\textbf{p$\wedge$q$\rightarrow$$\sim$r \\
\\
p$\vee$$\sim$q\\
\\
$\sim$q$\rightarrow$p\\\
\\
$\therefore$\ $\sim$r}

\begin{table}[ht]
\caption{Truth Table for p$\wedge$q$\rightarrow$$\sim$r.} % title of Table
\centering % used for centering table
\begin{tabular}{c c c c c c } % centered columns (5 columns)
\hline\hline %inserts double horizontal lines
p & q & r & p$\wedge$$\sim$q & $\sim$q$\rightarrow$p & $\sim$r \\ [0.5ex] % inserts table 
%heading  
\hline % inserts single horizontal line
T & T & T & F & F & F\\ % inserting body of the table
T & T & F & F & F & T \\
T & F & T & T & T & F \\
T & F & F & T & T & T\\
F & T & T & T & T & F\\ % inserting body of the table
F & T & F & T & T & T \\
F & F & T & F & F & F\\
F & F & F & F & F * T\\

\hline %inserts single line
\end{tabular}
\label{table:nonlin} % is used to refer this table in the text
\end{table}

The statement is invalid because there are no critical rows.
\end {homeworkProblem}
\begin{homeworkProblem}
Determine if the following argument is valid, or consists of converse or inverse errors. Use symbols to write
the logical form of each argument. If the argument is valid, identify
the rule of inference that guarantees its validity. Otherwise,
state whether the converse or the inverse error is made.
\\

\textit{If this computer program is correct, then it produces the
correct output when run with the test data my teacher
gave me.
This computer program produces the correct output
when run with the test data my teacher gave me.
$\therefore$ This computer program is correct.}

\textbf{Let P = Correct Computer program\\
Let Q = Correct output\\}

p$\rightarrow$ q\\
q\\
$\therefore$ p\\
The following argument is invalid because the closest rule of inference that would guarantee it\rq{}s validity would be Modus Pones.  Due to the converse switch in the minor premise, the argument is invalid.


\end{homeworkProblem}
\begin{homeworkProblem}
See scanned .jpg file.
\end{homeworkProblem}
\end{document}
