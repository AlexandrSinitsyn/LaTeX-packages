# LaTeX-packages

## Completeness

In the end of each section write this command:

```TeX
\writtenby[<part-number>]{<completeness %>}{<name>}
```

To see the result use this one:

```TeX
\showcompleteness
```

---

## Matlog package

Example:

```TeX
\begin{matlog}
    * |- a > a ?.
    * a > a > a ? 1 /
    * (a > (a > a)) > (a > (a > a) > a) > (a > a) ? 2 /
    * (a > (a > a) > a) > (a > a) ? MP 2, 3 /
    * a > (a > a) > a ? 1 /
    * a > a ? MP 4, 5 /
    \vspace{1cm}
    * !a & !(a V b) ?.
\end{matlog}
```

* Use `*` to start next expression;
  - First expression won't ever be itemized
* Each expression should stay to template of `* expr ?`. Follwed by:
  - `.` to finish the expression;
  - `<axiom's number> /` to say from which axiom was this expression gotten;
  - `MP <first>, <second> /` to set _Modus Ponens_ of two expressions.
