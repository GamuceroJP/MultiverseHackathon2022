---
title: "test"
output: 
  html_document:
    self_contained: false
    includes:
      in_header: head.html
---
# MultiverseHackathon2022
Repositorio para proyectos del Multiverse Hackathon 2022, equipo "Los Plancktons"

<!-- creating header file to insert in-header. mathjax config seems to be required -->
```{cat, engine.opts = list(file = "head.html")}
<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [['$','$'], ['\\(','\\)']],
            displayMath: [['$$','$$'], ['\\[','\\]']],
            processEscapes: true,
            processEnvironments: true,
        }
    });
</script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/pseudocode@latest/build/pseudocode.min.css">
<script src="https://cdn.jsdelivr.net/npm/pseudocode@latest/build/pseudocode.min.js"></script>
```

# Mathjax is still working
A block 
$$
1+1
$$

or inline math like $\alpha = x/y$

## Inserting an algorithm too

You can use an algorithm code block using syntax from [pseudocode.js](https://github.com/SaswatPadhi/pseudocode.js) by setting the fenced div attribute `algorithm` as below

```{.algorithm}
% This quicksort algorithm is extracted from Chapter 7, Introduction to Algorithms (3rd edition)
\begin{algorithm}
\caption{Quicksort}
\begin{algorithmic}
\PROCEDURE{Quicksort}{$A, p, r$}
    \IF{$p < r$} 
        \STATE $q = $ \CALL{Partition}{$A, p, r$}
        \STATE \CALL{Quicksort}{$A, p, q - 1$}
        \STATE \CALL{Quicksort}{$A, q + 1, r$}
    \ENDIF
\ENDPROCEDURE
\PROCEDURE{Partition}{$A, p, r$}
    \STATE $x = A[r]$
    \STATE $i = p - 1$
    \FOR{$j = p$ \TO $r - 1$}
        \IF{$A[j] < x$}
            \STATE $i = i + 1$
            \STATE exchange
            $A[i]$ with $A[j]$
        \ENDIF
        \STATE exchange $A[i]$ with $A[r]$
    \ENDFOR
\ENDPROCEDURE
\end{algorithmic}
\end{algorithm}
```

### Another one 

```{.algorithm}
\begin{algorithm}
\caption{The original \textsf{Relief} algorithm for ranking predictor variables in classification models with two classes.}
\begin{algorithmic}
\STATE Initialize the predictor scores $S_j$ to zero;
\FOR{$i = 1\ldots m$ randomly selected training set samples ($R_i$)}
\STATE Find the nearest miss and hit in the training set;
\FOR{$j = 1\ldots p$ predictor variables}
   \STATE Adjust the score for each predictor  based on the proximity of $R_j$ to the nearest miss and hit:\\
   $S_j = S_j - diff_j(R_j, Hit)^2/m + diff_j(R_j, Miss)^2/m$;
\ENDFOR
\ENDFOR
\end{algorithmic}
\end{algorithm}
```

<!-- rendering the algo block -->
```{js, echo = FALSE}
window.addEventListener('load', (event) => {
  elem = document.querySelectorAll(".algorithm")
  elem.forEach(e => {
    pseudocode.renderElement(e, {lineNumber: true, lineNumberPunc: ' '});
  })
});
```
