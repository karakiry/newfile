\documentclass{report}
\usepackage{ucs}
\usepackage[utf8x]{inputenc}
\usepackage[english,romanian]{babel}
\usepackage{color}
\usepackage{mathptmx}
\usepackage{mathtools}
\usepackage{anyfontsize}
\usepackage{graphicx}
\usepackage{t1enc}
\usepackage[document]{ragged2e}
\title{{\sc Raport asupra practicii: 24.06-05.07.2019}}
\author{ Daniel-Mihai ERET}
\date{\,}
\begin{document}
\maketitle

\tableofcontents

\chapter{Activitati planificate}
\begin{enumerate}
\item Luni, 24.06.2019 \newline
Aducerea la cunostinta a obiectivelor practicii.
\item Marti, 25.06.2019 \newline
Instalarea pachetelor software necesare desfasurarii practicii.
\item Miercuri, 26.06.2019 \newline
Studierea modului de lucru cu Git. Interfete grafice de lucru cu Git(SmartGit).
\item Joi, 27.06.2019 \newline
Studierea si practicarea LaTeX.
\item Vineri, 28.06.2019 \newline
Initierea unei lucrari(descrierea unui algoritm, a unei teme agregate cu prof. coordonator)
Tema proiect : 12(Inchiderea Tranzitiva a unui Graf)
Prof. Coordonator: Rusu Andrei
\item Luni, 01.07.2019 \newline
Am inceput sa ma documentez despre Tema proiectului.
Sa caut informatiile necesare implementarii unui algoritm de inchidere tranzitiva a unui graf.
\item Marti, 02.09.2019\newline
Am continuat sa studiez despre Grafuri si am incercat sa gasesc o solutie optima pentru "Inchiderea Tranzitiva a unui Graf".
\item Miercuri, 03.07.2019\newline
Prezentarea temelor de practica.
\item Joi, 04.07.2019\newline
Prezentarea temelor de practica.
\item Vineri, 05.07.2019\newline
Notarea finala a activitatiii.
\end{enumerate}

\chapter{Luni, 24.06.2019}
Studierea obiectivelor și cerințelor față de practica de producție. Clarificarea situațiilor incerte.

\chapter {Marti, 25.06.2019}
Am desfăţurat următoarele activităţi:
\begin{itemize}
\item
Am identificat sursele pentru MikTeX, Git, SmartGit și BitBucket.
\begin{itemize}
\item
Am identificat sursele pentru MikTeX, Git, SmartGit și BitBucket.
\item
Am instalat, configurat pe calculatorul de lucru aplicațiile necesare:
\begin{itemize}
\item
MikTeX
\item
SmartGit
\item
Bitbucket
\end{itemize}
\item
Am instalat, configurat pe calculatorul de lucru aplicațiile necesare:
\begin{itemize}
\item
MikTeX
\item
SmartGit
\item
Bitbucket
\end{itemize}

\end{itemize}
\end{itemize}

\chapter{Miercuri, 26.06.2019}
Am studiat modul de lucru cu Git și interfața grafică de lucru cu Git (SmartGit).
\chapter{Joi, 27.06.2019}
Am studiat și am practicat Latex.
\chapter{Vineri, 28.06.2019}
Am inițiat o lucrare scrisă în Latex:
\begin{itemize}
\item
Am ales o tema de practica(Tema 12)
\item
Am inceput sa ma informez despre aceasta tema(Inchiderea Tranzitiva a unui graf).
\end{itemize}
\chapter{Luni, 01.07.2019}
Am continuat lucrul asupra temei alese.
\chapter{Marti,02.07.2019}
\section  {Am continuat lucrul asupra temei și am terminat .}


 \section { \textbf    {\emph{\underline{ \  Prezentarea temei de practică}}}}

 Tema proiectului meu este:\textbf{ \emph { "Inchiderea tranzitiva a unui graf".}}
\begin{flushleft}

\textbf {Algoritmul lui Warshall} este unul din algoritmii folositi la inchiderea tranzitiva a unui graf orientat.
\begin{itemize}
\item
Algoritmul lui \textbf {Warshall} se bazează pe observaţia simplă că, dacă într-un graf orientat
există o modalitate de a ajunge de la nodul i la nodul k şi o modalitate de a ajunge de
la nodul k la nodul j, parcurgând arce ale grafului, atunci cu siguranţă există un drum
care conectează nodul i cu nodul j. 
\begin{itemize}
\item
Problema constă de fapt în a exploata de asemenea manieră această observaţie
încât calculul să se realizeze la o singură trecere prin matrice. 
\end{itemize}
\item
Acest lucru este posibil în baza următoarei interpretări sugerate de \textbf {Warshall}:
\begin{itemize}
\item
 “Dacă există o posibilitate de a ajunge de la nodul i la nodul k utilizând
numai noduri cu indici mai mici decât k, şi o posibilitate de a ajunge de la
nodul k la nodul j în aceleaşi condiţii, atunci există un drum de la nodul i la
nodul j care străbate numai noduri care cu indicele mai mic ca şi k+1”. 
\end{itemize}
\item
În baza acestei interpretări, dându-se graful ordonat G şi matricea sa de adiacenţe A,
algoritmul lui Warshall determină matricea T care reprezintă închiderea tranzitivă a
grafului G.
\begin{itemize}
\item
În această matrice \texttt{T[i,j]=true}, dacă există posibilitatea de a ajunge de la
nodul i la nodul j, altfel \texttt{T[i,j]=false}. 
\end{itemize}
\item
Spre exemplu în figura \textbf {figura 8.1(b) } apare închiderea tranzitivă în forma matricii T a
grafului orientat din \textbf{figura  8.1(a)}. 
\begin{figure}[htb]
\begin{center}
\includegraphics{Figura1}
\end{center}
\caption {Inchiderea tranzitiva a unui graf orientat}
\end{figure}
\item
Închiderea tranzitivă poate fi determinată aplicând o procedură similară procedurii
Floyd, utilizând însă următoarea formulă în cea de-a k-a trecere prin matricea T :
\newline

\[T_k  [i,j]  = T_{k-1} [i,j] \quad \textrm{OR} \quad (T_{k-1} [i,k]  \quad \textrm{AND} \quad  T_{k-1} [k,j] \]

\item Aceasta formula precizeaza ca exista un drum de la nodul i la nodul j care nu trece printr-un nod cu numar mai mare ca si k daca :
\begin{enumerate}
\item
Există deja un drum de la i la j care nu trece prin nici un nod cu număr
mai mare decât k-1, sau 
\item
Există un drum de la i la k care nu trece prin nici un nod cu număr mai
mare decât k-1 şi există un drum de la k la j, care nu trece prin niciun nod cu
număr mai mare decât k-1. 
\end{enumerate}
\item
Ca şi în cazul algoritmului lui Floyd, sunt valabile formulele :
\[T_k  [i,j]  = T_{k-1} [i,j] \quad \textrm {si} \quad T_k  [k,j]  = T_{k-1} [k,j] \]  
motiv pentru care în calcul se poate utiliza o singură instanţă a matricii T. 
\LARGE {--------------------------------------------------------}
\normalsize
\textbf {PROCEDURE} Warshall(A: \textbf {ARRAY}[1..n,1..n] \textbf{OF} boolean;
\newline
\textbf {VAR} T: \textbf {ARRAY} [1..n,1..n] \textbf{OF} boolean); 
\newline
\textcolor{red}{Procedura construieşte în T închiderea tranzitivă a lui A}
\newline
 \textbf {VAR} i,j,k: integer 
\newline
\textbf{BEGIN}
\begin{enumerate}
\item
 \textbf  {FOR} i:= 1  \textbf {TO} n  \textbf {DO}
\item
 \textbf {FOR} j:= 1  \textbf {TO} n  \textbf {DO}
\item
T[i,j]:= A[i,j]; 
\item
 \textbf {FOR} k:= 1  \textbf {TO} n  \textbf {DO}
\item
 \textbf {FOR} i:= 1  \textbf {TO} n  \textbf {DO}
\item
 \textbf {FOR} j:= 1  \textbf {TO} n  \textbf {DO} 
\item
 \textbf {IF} T[i,j] =  \textbf {false THEN}
\item
T[i,j]:= T[i,k]  \textbf {AND} T[k,j] 
\end{enumerate}
 \textbf {END};   \textbf { (Acesta este Algoritmul lui Warshall in \textcolor{red} {PSEUDOCOD})} 
\LARGE {--------------------------------------------------------}
\normalsize
\textcolor{blue}{Acest algoritm are o performanta de} \[O_(n^3)\]
\end{itemize}
\end{flushleft}


\chapter{Miercuri, 03.07.2019}
Prezentarea proiectului.
\chapter{Joi, 04.07.2019}
Prezentarea proiectului.
\chapter{Vineri, 05.07.2017}
Notarea finală a activității.

\chapter{Concluzii}
Am invățat să lucrez cu Latex ,Git și BitBucket. 
\newline
\textbf {LaTeX } este un limbaj de markup si programare folosit in redactarea documentelor, cu ajutorul acestuia mi-am redactat \textcolor{blue}{Raportul de practica}

\textbf{Git}


% aici urmeaza declaratiile care fac posibila includerea bibliografiei in format bibtex. 


\bibliography{referinte} 
\bibliographystyle{ieeetr}

\end{document}
