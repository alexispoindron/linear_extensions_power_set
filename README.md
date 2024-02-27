
\section{Unreshuffling linear extensions}

\begin{definition}
The \textit{unreshuffling $(n,\sigma)$-linear extension} $ U_{(n,\sigma)}$, shortly denoted by $ U_{\sigma}$ when $n$ is implicit, is the linear extension obtained by the following algorithm:
\begin{itemize}
    \item Start from $ L=[[]]$. 
    \item For $ k=\sigma(1), \ldots, \sigma(n)$, duplicate the states of $ L$ by adding $ k$ at each duplication.
\end{itemize}

 \end{definition}

 \begin{example} With the order of addition of nodes $ \sigma=(1,2,3,4)$, we produce the following unreshuffling $ (n,\sigma)$-linear extension.
\begin{enumerate}
   \item $L=[[]]$
        \item $L=[[],[1]]$
        \item $L=[[],[1],[2],[1,2]]$
        \item $L=[[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3]]$
        \item $L=[[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3],[4],[1,4],[2,4],[1,2,4],[3,4],[1,3,4],[2,3,4],[1,2,3,4]]$.
  
\end{enumerate}
             
 \end{example}



 The \textit{unreshuffling} linear extension can be seen as the natural order induced by successive duplications of the hypercube. This linear order valued for the following advantage, that it owe its name to: in order to add a new agent, we do not need to reshuffle the list, meaning that the ranks are previous states remain unchanged. A direct consequence of the construction of $ U_{\sigma}$ is Property \ref{p1}, that gives an explicit expression of the rank of a given state in an unreshuffling as a function of the order of entry of new agents.  In binary notation, $ R^{U_{(1, \ldots, n)}}(S)$ is a 0-1 vector whose $ k^{th}$ entry is 1 if and only if $ k\in S $, and indeed this expression does not depend on $n$. Stated otherwise, the binary notations of numbers from 0 to $ 2^n-1$ indicate, by the place of the 1, the corresponding set in the linear extension, up to the relabelling of agents. 


 \begin{property} \label{p1}
     $ \displaystyle{R^{U_{\sigma}}(S)=\sum_{k\in S}2^{\sigma(k)-1}}=v(S)$,
 \end{property}

 where $ v(S)$ is the 0-1 vector whose $ 1$ entries correspond to the elements in $ S$. This additional notation being a bit superfluous, identifying a state $S$ to a 0-1 vector, by the abuse of notation allowed by a natural identification, we can simply write $R^{U_{\sigma}}(S)=S $. When true for all $ S$, this identity is actually a characterization of the unreshuffling linear extension. 

  
 \begin{example}
     In the middle linear extension of Figure \ref{Fex}, $\sigma(3)=3$, $ \sigma(4)=4$, and we have $ R(34)=2^{3-1}+2^{4-1}=12.$
 \end{example}

 
 We denote by $ U$ the set of unreshuffling linear extensions. The set of all permutations of $ N$ is denoted by $ S_n$. Denote by $ U^{S} $ the set of unreshuffling linear extensions obtained from the set of permutations $S $. By definition of $U$, $ U= U^{S_n} $.


\section{Convex hull of a set of linear extensions}



\begin{definition}
The \textit{convex hull} of a set $ L=\{ \mathcal{L}_0, \ldots,  \mathcal{L}_L\}$ of linear extensions, denoted by $ \overline{\{\mathcal{L}_1, \ldots, \mathcal{L}_L \}}$ or $ Conv(\mathcal{L}_1, \ldots, \mathcal{L}_L )$, is the set of linear extensions that are obtained from Algorithm \ref{algoL}. A linear extension in the convex hull of some linear extension is said to be a \textit{combination} of them.
 
\begin{algorithm} 
  \caption{Linear extension of the power set}
\begin{algorithmic}
\State{- Consider $ L $ linear extensions $\mathcal{L}_1, \ldots, \mathcal{L}_L $ (``the basis'').}
 \State{- Start from an empty list $ \mathcal{L}_{O}$ (which will finally be the output)}
 \State{- Start from one of the linear extensions of the basis.}
 \State{- Specify a walk of length $ 2^n$ between the linear extensions of the basis (randomly, if needed)}
 \State{- Navigate between the linear extensions according to this walk. For each linear extension $\mathcal{L} $ met by the walk, attribute to $ \mathcal{L}_{O}$ the smallest element of $ \mathcal{L}$ that is not already in $ \mathcal{L}_O$.}
\end{algorithmic}
  % \begin{algorithmic}[1]
  % %  \EndFor
  % \end{algorithmic}
  \label{algoL}
\end{algorithm}
\end{definition}
\begin{example}
    We display in Figure \ref{Fex} the process of generation of a linear extension according to Algorithm \ref{algoL} and a basis of two linear extensions ($|L|=2$). 
\end{example}

