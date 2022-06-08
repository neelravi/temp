<?xml version="1.0" encoding="utf-8"?><html lang="en" xml:lang="en" xmlns="http://www.w3.org/1999/xhtml"><head><meta content="text/html;charset=utf-8" http-equiv="Content-Type"></meta><meta content="width=device-width, initial-scale=1" name="viewport"></meta><title>Quantum Monte Carlo</title><meta content="Org mode" name="generator"></meta><meta content="Anthony Scemama, Claudia Filippi" name="author"></meta><style type="text/css">
 <!--/*--><![CDATA[/*><!--*/
  .title  { text-align: center;
             margin-bottom: .2em; }
  .subtitle { text-align: center;
              font-size: medium;
              font-weight: bold;
              margin-top:0; }
  .todo   { font-family: monospace; color: red; }
  .done   { font-family: monospace; color: green; }
  .priority { font-family: monospace; color: orange; }
  .tag    { background-color: #eee; font-family: monospace;
            padding: 2px; font-size: 80%; font-weight: normal; }
  .timestamp { color: #bebebe; }
  .timestamp-kwd { color: #5f9ea0; }
  .org-right  { margin-left: auto; margin-right: 0px;  text-align: right; }
  .org-left   { margin-left: 0px;  margin-right: auto; text-align: left; }
  .org-center { margin-left: auto; margin-right: auto; text-align: center; }
  .underline { text-decoration: underline; }
  #postamble p, #preamble p { font-size: 90%; margin: .2em; }
  p.verse { margin-left: 3%; }
  pre {
    border: 1px solid #ccc;
    box-shadow: 3px 3px 3px #eee;
    padding: 8pt;
    font-family: monospace;
    overflow: auto;
    margin: 1.2em;
  }
  pre.src {
    position: relative;
    overflow: visible;
    padding-top: 1.2em;
  }
  pre.src:before {
    display: none;
    position: absolute;
    background-color: white;
    top: -10px;
    right: 10px;
    padding: 3px;
    border: 1px solid black;
  }
  pre.src:hover:before { display: inline;}
  /* Languages per Org manual */
  pre.src-asymptote:before { content: 'Asymptote'; }
  pre.src-awk:before { content: 'Awk'; }
  pre.src-C:before { content: 'C'; }
  /* pre.src-C++ doesn't work in CSS */
  pre.src-clojure:before { content: 'Clojure'; }
  pre.src-css:before { content: 'CSS'; }
  pre.src-D:before { content: 'D'; }
  pre.src-ditaa:before { content: 'ditaa'; }
  pre.src-dot:before { content: 'Graphviz'; }
  pre.src-calc:before { content: 'Emacs Calc'; }
  pre.src-emacs-lisp:before { content: 'Emacs Lisp'; }
  pre.src-fortran:before { content: 'Fortran'; }
  pre.src-gnuplot:before { content: 'gnuplot'; }
  pre.src-haskell:before { content: 'Haskell'; }
  pre.src-hledger:before { content: 'hledger'; }
  pre.src-java:before { content: 'Java'; }
  pre.src-js:before { content: 'Javascript'; }
  pre.src-latex:before { content: 'LaTeX'; }
  pre.src-ledger:before { content: 'Ledger'; }
  pre.src-lisp:before { content: 'Lisp'; }
  pre.src-lilypond:before { content: 'Lilypond'; }
  pre.src-lua:before { content: 'Lua'; }
  pre.src-matlab:before { content: 'MATLAB'; }
  pre.src-mscgen:before { content: 'Mscgen'; }
  pre.src-ocaml:before { content: 'Objective Caml'; }
  pre.src-octave:before { content: 'Octave'; }
  pre.src-org:before { content: 'Org mode'; }
  pre.src-oz:before { content: 'OZ'; }
  pre.src-plantuml:before { content: 'Plantuml'; }
  pre.src-processing:before { content: 'Processing.js'; }
  pre.src-python:before { content: 'Python'; }
  pre.src-R:before { content: 'R'; }
  pre.src-ruby:before { content: 'Ruby'; }
  pre.src-sass:before { content: 'Sass'; }
  pre.src-scheme:before { content: 'Scheme'; }
  pre.src-screen:before { content: 'Gnu Screen'; }
  pre.src-sed:before { content: 'Sed'; }
  pre.src-sh:before { content: 'shell'; }
  pre.src-sql:before { content: 'SQL'; }
  pre.src-sqlite:before { content: 'SQLite'; }
  /* additional languages in org.el's org-babel-load-languages alist */
  pre.src-forth:before { content: 'Forth'; }
  pre.src-io:before { content: 'IO'; }
  pre.src-J:before { content: 'J'; }
  pre.src-makefile:before { content: 'Makefile'; }
  pre.src-maxima:before { content: 'Maxima'; }
  pre.src-perl:before { content: 'Perl'; }
  pre.src-picolisp:before { content: 'Pico Lisp'; }
  pre.src-scala:before { content: 'Scala'; }
  pre.src-shell:before { content: 'Shell Script'; }
  pre.src-ebnf2ps:before { content: 'ebfn2ps'; }
  /* additional language identifiers per "defun org-babel-execute"
       in ob-*.el */
  pre.src-cpp:before  { content: 'C++'; }
  pre.src-abc:before  { content: 'ABC'; }
  pre.src-coq:before  { content: 'Coq'; }
  pre.src-groovy:before  { content: 'Groovy'; }
  /* additional language identifiers from org-babel-shell-names in
     ob-shell.el: ob-shell is the only babel language using a lambda to put
     the execution function name together. */
  pre.src-bash:before  { content: 'bash'; }
  pre.src-csh:before  { content: 'csh'; }
  pre.src-ash:before  { content: 'ash'; }
  pre.src-dash:before  { content: 'dash'; }
  pre.src-ksh:before  { content: 'ksh'; }
  pre.src-mksh:before  { content: 'mksh'; }
  pre.src-posh:before  { content: 'posh'; }
  /* Additional Emacs modes also supported by the LaTeX listings package */
  pre.src-ada:before { content: 'Ada'; }
  pre.src-asm:before { content: 'Assembler'; }
  pre.src-caml:before { content: 'Caml'; }
  pre.src-delphi:before { content: 'Delphi'; }
  pre.src-html:before { content: 'HTML'; }
  pre.src-idl:before { content: 'IDL'; }
  pre.src-mercury:before { content: 'Mercury'; }
  pre.src-metapost:before { content: 'MetaPost'; }
  pre.src-modula-2:before { content: 'Modula-2'; }
  pre.src-pascal:before { content: 'Pascal'; }
  pre.src-ps:before { content: 'PostScript'; }
  pre.src-prolog:before { content: 'Prolog'; }
  pre.src-simula:before { content: 'Simula'; }
  pre.src-tcl:before { content: 'tcl'; }
  pre.src-tex:before { content: 'TeX'; }
  pre.src-plain-tex:before { content: 'Plain TeX'; }
  pre.src-verilog:before { content: 'Verilog'; }
  pre.src-vhdl:before { content: 'VHDL'; }
  pre.src-xml:before { content: 'XML'; }
  pre.src-nxml:before { content: 'XML'; }
  /* add a generic configuration mode; LaTeX export needs an additional
     (add-to-list 'org-latex-listings-langs '(conf " ")) in .emacs */
  pre.src-conf:before { content: 'Configuration File'; }

  table { border-collapse:collapse; }
  caption.t-above { caption-side: top; }
  caption.t-bottom { caption-side: bottom; }
  td, th { vertical-align:top;  }
  th.org-right  { text-align: center;  }
  th.org-left   { text-align: center;   }
  th.org-center { text-align: center; }
  td.org-right  { text-align: right;  }
  td.org-left   { text-align: left;   }
  td.org-center { text-align: center; }
  dt { font-weight: bold; }
  .footpara { display: inline; }
  .footdef  { margin-bottom: 1em; }
  .figure { padding: 1em; }
  .figure p { text-align: center; }
  .inlinetask {
    padding: 10px;
    border: 2px solid gray;
    margin: 10px;
    background: #ffffcc;
  }
  #org-div-home-and-up
   { text-align: right; font-size: 70%; white-space: nowrap; }
  textarea { overflow-x: auto; }
  .linenr { font-size: smaller }
  .code-highlighted { background-color: #ffff00; }
  .org-info-js_info-navigation { border-style: none; }
  #org-info-js_console-label
    { font-size: 10px; font-weight: bold; white-space: nowrap; }
  .org-info-js_search-highlight
    { background-color: #ffff00; color: #000000; font-weight: bold; }
  .org-svg { width: 90%; }
  /*]]>*/-->
</style><link href="worg.css" rel="stylesheet" title="Standard" type="text/css"></link><script src="org-info.js" type="text/javascript">
/**
 *
 * @source: org-info.js
 *
 * @licstart  The following is the entire license notice for the
 *  JavaScript code in org-info.js.
 *
 * Copyright (C) 2012-2019 Free Software Foundation, Inc.
 *
 *
 * The JavaScript code in this tag is free software: you can
 * redistribute it and/or modify it under the terms of the GNU
 * General Public License (GNU GPL) as published by the Free Software
 * Foundation, either version 3 of the License, or (at your option)
 * any later version.  The code is distributed WITHOUT ANY WARRANTY;
 * without even the implied warranty of MERCHANTABILITY or FITNESS
 * FOR A PARTICULAR PURPOSE.  See the GNU GPL for more details.
 *
 * As additional permission under GNU GPL version 3 section 7, you
 * may distribute non-source (e.g., minimized or compacted) forms of
 * that code without the copy of the GNU GPL normally required by
 * section 4, provided you include this license notice and a URL
 * through which recipients can access the Corresponding Source.
 *
 * @licend  The above is the entire license notice
 * for the JavaScript code in org-info.js.
 *
 */
</script><script type="text/javascript">

/*
@licstart  The following is the entire license notice for the
JavaScript code in this tag.

Copyright (C) 2012-2019 Free Software Foundation, Inc.

The JavaScript code in this tag is free software: you can
redistribute it and/or modify it under the terms of the GNU
General Public License (GNU GPL) as published by the Free Software
Foundation, either version 3 of the License, or (at your option)
any later version.  The code is distributed WITHOUT ANY WARRANTY;
without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE.  See the GNU GPL for more details.

As additional permission under GNU GPL version 3 section 7, you
may distribute non-source (e.g., minimized or compacted) forms of
that code without the copy of the GNU GPL normally required by
section 4, provided you include this license notice and a URL
through which recipients can access the Corresponding Source.


@licend  The above is the entire license notice
for the JavaScript code in this tag.
*/

<!--/*--><![CDATA[/*><!--*/
org_html_manager.set("TOC_DEPTH", "4");
org_html_manager.set("LINK_HOME", "");
org_html_manager.set("LINK_UP", "");
org_html_manager.set("LOCAL_TOC", "1");
org_html_manager.set("VIEW_BUTTONS", "0");
org_html_manager.set("MOUSE_HINT", "underline");
org_html_manager.set("FIXED_TOC", "0");
org_html_manager.set("TOC", "1");
org_html_manager.set("VIEW", "info");
org_html_manager.setup();  // activate after the parameters are set
/*]]>*///-->
</script><script type="text/javascript">
/*
@licstart  The following is the entire license notice for the
JavaScript code in this tag.

Copyright (C) 2012-2019 Free Software Foundation, Inc.

The JavaScript code in this tag is free software: you can
redistribute it and/or modify it under the terms of the GNU
General Public License (GNU GPL) as published by the Free Software
Foundation, either version 3 of the License, or (at your option)
any later version.  The code is distributed WITHOUT ANY WARRANTY;
without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE.  See the GNU GPL for more details.

As additional permission under GNU GPL version 3 section 7, you
may distribute non-source (e.g., minimized or compacted) forms of
that code without the copy of the GNU GPL normally required by
section 4, provided you include this license notice and a URL
through which recipients can access the Corresponding Source.


@licend  The above is the entire license notice
for the JavaScript code in this tag.
*/
<!--/*--><![CDATA[/*><!--*/
 function CodeHighlightOn(elem, id)
 {
   var target = document.getElementById(id);
   if(null != target) {
     elem.cacheClassElem = elem.className;
     elem.cacheClassTarget = target.className;
     target.className = "code-highlighted";
     elem.className   = "code-highlighted";
   }
 }
 function CodeHighlightOff(elem, id)
 {
   var target = document.getElementById(id);
   if(elem.cacheClassElem)
     elem.className = elem.cacheClassElem;
   if(elem.cacheClassTarget)
     target.className = elem.cacheClassTarget;
 }
/*]]>*///-->
</script><script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        displayAlign: "center",
        displayIndent: "0em",

        "HTML-CSS": { scale: 100,
                        linebreaks: { automatic: "false" },
                        webFont: "TeX"
                       },
        SVG: {scale: 100,
              linebreaks: { automatic: "false" },
              font: "TeX"},
        NativeMML: {scale: 100},
        TeX: { equationNumbers: {autoNumber: "AMS"},
               MultLineWidth: "85%",
               TagSide: "right",
               TagIndent: ".8em"
             }
});
</script><script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS_HTML" type="text/javascript"></script></head><body><div id="content">Quantum Monte Carlo
===================

<div id="table-of-contents">Table of Contents
-----------------

<div id="text-table-of-contents">- [1. Introduction](#org70485eb)
  - [1.1. Energy and local energy](#org6fc743c)
- [2. Numerical evaluation of the energy of the hydrogen atom](#orge543e0e)
  - [2.1. Local energy](#orgba60729)
      - [2.1.1. Exercise 1](#org954c40b)
      - [2.1.2. Exercise 2](#org28b707a)
      - [2.1.3. Exercise 3](#orgea37920)
      - [2.1.4. Exercise 4](#org913dd8b)
      - [2.1.5. Exercise 5](#orgfa02dda)
  - [2.2. Plot of the local energy along the \\(x\\) axis](#org46b45c5)
      - [2.2.1. Exercise](#org09ec0db)
  - [2.3. Numerical estimation of the energy](#orgfb47a4e)
      - [2.3.1. Exercise](#org74b4c2f)
  - [2.4. Variance of the local energy](#org1d2fd58)
      - [2.4.1. Exercise (optional)](#org39d6a49)
      - [2.4.2. Exercise](#org67a65e8)
- [3. Variational Monte Carlo](#org670b628)
  - [3.1. Computation of the statistical error](#org062bbf8)
      - [3.1.1. Exercise](#orge22e1d8)
  - [3.2. Uniform sampling in the box](#org77b3c6a)
      - [3.2.1. Exercise](#org313f15c)
  - [3.3. Metropolis sampling with \\(\\Psi^2\\)](#orgdffe812)
      - [3.3.1. Optimal step size](#org33983d0)
      - [3.3.2. Exercise](#org0b89863)
  - [3.4. Generalized Metropolis algorithm](#org1795441)
      - [3.4.1. Gaussian random number generator](#org4a0843e)
      - [3.4.2. Exercise 1](#org4a6aa65)
      - [3.4.3. Exercise 2](#org35062aa)
- [4. Diffusion Monte Carlo](#org84089bb)
  - [4.1. Schrödinger equation in imaginary time](#org16ba172)
  - [4.2. Relation to diffusion](#org61c215f)
  - [4.3. Importance sampling](#org5ee9aee)
      - [4.3.1. Appendix : Details of the Derivation](#org5805991)
  - [4.4. Pure Diffusion Monte Carlo](#org8801356)
  - [4.5. Hydrogen atom](#org339c87b)
      - [4.5.1. Exercise](#orgbbacf6d)
- [5. Project](#org9d710e3)
- [6. Acknowledgments](#org38ba401)

</div></div><div class="outline-2" id="outline-container-org70485eb"><span class="section-number-2">1</span> Introduction
----------------------------------------------------

<div class="outline-text-2" id="text-1">This website contains the QMC tutorial of the 2021 LTTC winter school [Tutorials in Theoretical Chemistry](https://www.irsamc.ups-tlse.fr/lttc/Luchon).

We propose different exercises to understand quantum Monte Carlo (QMC) methods. In the first section, we start with the computation of the energy of a hydrogen atom using numerical integration. The goal of this section is to familarize yourself with the concept of *local energy*. Then, we introduce the variational Monte Carlo (VMC) method which computes a statistical estimate of the expectation value of the energy associated with a given wave function, and apply this approach to the hydrogen atom. Finally, we present the diffusion Monte Carlo (DMC) method which we use here to estimate the exact energy of the hydrogen atom and of the H<sub>2</sub> molecule, starting from an approximate wave function.

Code examples will be given in Python3 and Fortran. You can use whatever language you prefer to write the programs.

We consider the stationary solution of the Schrödinger equation, so the wave functions considered here are real: for an \\(N\\) electron system where the electrons move in the 3-dimensional space, \\(\\Psi : \\mathbb{R}^{3N} \\rightarrow \\mathbb{R}\\). In addition, \\(\\Psi\\) is defined everywhere, continuous, and infinitely differentiable.

All the quantities are expressed in *atomic units* (energies, coordinates, etc).

</div><div class="outline-3" id="outline-container-org6fc743c">### <span class="section-number-3">1.1</span> Energy and local energy

<div class="outline-text-3" id="text-1-1">For a given system with Hamiltonian \\(\\hat{H}\\) and wave function \\(\\Psi\\), we define the local energy as

\\\[ E\_L(\\mathbf{r}) = \\frac{\\hat{H} \\Psi(\\mathbf{r})}{\\Psi(\\mathbf{r})}, \\\]

where \\(\\mathbf{r}\\) denotes the 3N-dimensional electronic coordinates.

The electronic energy of a system, \\(E\\), can be rewritten in terms of the local energy \\(E\_L(\\mathbf{r})\\) as

\begin{eqnarray*} E &amp; = &amp; \frac{\langle \Psi| \hat{H} | \Psi\rangle}{\langle \Psi |\Psi \rangle} = \frac{\int \Psi(\mathbf{r})\, \hat{H} \Psi(\mathbf{r})\, d\mathbf{r}}{\int |\Psi(\mathbf{r}) |^2 d\mathbf{r}} \\ &amp; = &amp; \frac{\int |\Psi(\mathbf{r})|^2\, \frac{\hat{H} \Psi(\mathbf{r})}{\Psi(\mathbf{r})}\,d\mathbf{r}}{\int |\Psi(\mathbf{r}) |^2 d\mathbf{r}} = \frac{\int |\Psi(\mathbf{r})|^2\, E_L(\mathbf{r})\,d\mathbf{r}}{\int |\Psi(\mathbf{r}) |^2 d\mathbf{r}} \end{eqnarray*} For few dimensions, one can easily compute \\(E\\) by evaluating the integrals on a grid but, for a high number of dimensions, one can resort to Monte Carlo techniques to compute \\(E\\).

To this aim, recall that the probabilistic *expected value* of an arbitrary function \\(f(x)\\) with respect to a probability density function \\(P(x)\\) is given by

\\\[ \\langle f \\rangle\_P = \\int\_{-\\infty}^\\infty P(x)\\, f(x)\\,dx, \\\]

where a probability density function \\(P(x)\\) is non-negative and integrates to one:

\\\[ \\int\_{-\\infty}^\\infty P(x)\\,dx = 1. \\\]

Similarly, we can view the the energy of a system, \\(E\\), as the expected value of the local energy with respect to a probability density \\(P(\\mathbf{r})\\) defined in 3\\(N\\) dimensions:

\\\[ E = \\int E\_L(\\mathbf{r}) P(\\mathbf{r})\\,d\\mathbf{r} \\equiv \\langle E\_L \\rangle\_{P}\\,, \\\]

where the probability density is given by the square of the wave function:

\\\[ P(\\mathbf{r}) = \\frac{|\\Psi(\\mathbf{r})|^2}{\\int |\\Psi(\\mathbf{r})|^2 d\\mathbf{r}}\\,. \\\]

If we can sample \\(N\_{\\rm MC}\\) configurations \\(\\{\\mathbf{r}\\}\\) distributed as \\(P\\), we can estimate \\(E\\) as the average of the local energy computed over these configurations:

\\\[ E \\approx \\frac{1}{N\_{\\rm MC}} \\sum\_{i=1}^{N\_{\\rm MC}} E\_L(\\mathbf{r}\_i) \\,. \\\]

</div></div></div><div class="outline-2" id="outline-container-orge543e0e"><span class="section-number-2">2</span> Numerical evaluation of the energy of the hydrogen atom
-----------------------------------------------------------------------------------------------

<div class="outline-text-2" id="text-2">In this section, we consider the hydrogen atom with the following wave function:

\\\[ \\Psi(\\mathbf{r}) = \\exp(-a |\\mathbf{r}|) \\\]

We will first verify that, for a particular value of \\(a\\), \\(\\Psi\\) is an eigenfunction of the Hamiltonian

\\\[ \\hat{H} = \\hat{T} + \\hat{V} = - \\frac{1}{2} \\Delta - \\frac{1}{|\\mathbf{r}|} \\\]

To do that, we will compute the local energy and check whether it is constant.

</div><div class="outline-3" id="outline-container-orgba60729">### <span class="section-number-3">2.1</span> Local energy

<div class="outline-text-3" id="text-2-1">You will now program all quantities needed to compute the local energy of the H atom for the given wave function.

Write all the functions of this section in a single file : `hydrogen.py` if you use Python, or `hydrogen.f90` is you use Fortran.

<div class="note">- When computing a square root in \\(\\mathbb{R}\\), **always** make sure that the argument of the square root is non-negative.
- When you divide, **always** make sure that you will not divide by zero

If a *floating-point exception* can occur, you should make a test to catch the error.

</div></div><div class="outline-4" id="outline-container-org954c40b">#### <span class="section-number-4">2.1.1</span> Exercise 1

<div class="outline-text-4" id="text-2-1-1"><div class="exercise">Write a function which computes the potential at \\(\\mathbf{r}\\). The function accepts a 3-dimensional vector `r` as input argument and returns the potential.

</div>\\(\\mathbf{r}=\\left( \\begin{array}{c} x \\\\ y\\\\ z\\end{array} \\right)\\), so \\\[ V(\\mathbf{r}) = -\\frac{1}{\\sqrt{x^2 + y^2 + z^2}} \\\]

**Python**

<div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>
<span style="color: #a020f0;">import</span> numpy <span style="color: #a020f0;">as</span> np

<span style="color: #a020f0;">def</span> <span style="color: #0000ff;">potential</span>(r):
    # <span style="color: #b22222;">TODO</span>
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #228b22;">double precision </span><span style="color: #a020f0;">function</span><span style="color: #a0522d;"> </span><span style="color: #0000ff;">potential</span><span style="color: #000000; background-color: #ffffff;">(r)</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in) ::<span style="color: #a0522d;"> r(3)</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end function</span> <span style="color: #0000ff;">potential</span>
```

</div></div></div><div class="outline-4" id="outline-container-org28b707a">#### <span class="section-number-4">2.1.2</span> Exercise 2

<div class="outline-text-4" id="text-2-1-2"><div class="exercise">Write a function which computes the wave function at \\(\\mathbf{r}\\). The function accepts a scalar `a` and a 3-dimensional vector `r` as input arguments, and returns a scalar.

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python"><span style="color: #a020f0;">def</span> <span style="color: #0000ff;">psi</span>(a, r):
    # <span style="color: #b22222;">TODO</span>
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #228b22;">double precision </span><span style="color: #a020f0;">function</span><span style="color: #a0522d;"> </span><span style="color: #0000ff;">psi</span><span style="color: #000000; background-color: #ffffff;">(a, r)</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in) ::<span style="color: #a0522d;"> a, r(3)</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end function</span> <span style="color: #0000ff;">psi</span>
```

</div></div></div><div class="outline-4" id="outline-container-orgea37920">#### <span class="section-number-4">2.1.3</span> Exercise 3

<div class="outline-text-4" id="text-2-1-3"><div class="exercise">Write a function which computes the local kinetic energy at \\(\\mathbf{r}\\). The function accepts `a` and `r` as input arguments and returns the local kinetic energy.

</div>The local kinetic energy is defined as \\\[T\_L(\\mathbf{r}) = -\\frac{1}{2}\\frac{\\Delta \\Psi(\\mathbf{r})}{\\Psi(\\mathbf{r})}.\\\]

We differentiate \\(\\Psi\\) with respect to \\(x\\):

\\\[ \\Psi(\\mathbf{r}) = \\exp(-a\\,|\\mathbf{r}|) \\\] \\\[\\frac{\\partial \\Psi}{\\partial x} = \\frac{\\partial \\Psi}{\\partial |\\mathbf{r}|} \\frac{\\partial |\\mathbf{r}|}{\\partial x} = - \\frac{a\\,x}{|\\mathbf{r}|} \\Psi(\\mathbf{r}) \\\]

and we differentiate a second time:

\\\[ \\frac{\\partial^2 \\Psi}{\\partial x^2} = \\left( \\frac{a^2\\,x^2}{|\\mathbf{r}|^2} - \\frac{a(y^2+z^2)}{|\\mathbf{r}|^{3}} \\right) \\Psi(\\mathbf{r}). \\\]

The Laplacian operator \\(\\Delta = \\frac{\\partial^2}{\\partial x^2} + \\frac{\\partial^2}{\\partial y^2} + \\frac{\\partial^2}{\\partial z^2}\\) applied to the wave function gives:

\\\[ \\Delta \\Psi (\\mathbf{r}) = \\left(a^2 - \\frac{2a}{\\mathbf{|r|}} \\right) \\Psi(\\mathbf{r})\\,. \\\]

Therefore, the local kinetic energy is \\\[ T\_L (\\mathbf{r}) = -\\frac{1}{2}\\left(a^2 - \\frac{2a}{\\mathbf{|r|}} \\right) \\\]

**Python**

<div class="org-src-container">```
<pre class="src src-python"><span style="color: #a020f0;">def</span> <span style="color: #0000ff;">kinetic</span>(a,r):
    # <span style="color: #b22222;">TODO</span>
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #228b22;">double precision </span><span style="color: #a020f0;">function</span><span style="color: #a0522d;"> </span><span style="color: #0000ff;">kinetic</span><span style="color: #000000; background-color: #ffffff;">(a,r)</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in) ::<span style="color: #a0522d;"> a, r(3)</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end function</span> <span style="color: #0000ff;">kinetic</span>
```

</div></div></div><div class="outline-4" id="outline-container-org913dd8b">#### <span class="section-number-4">2.1.4</span> Exercise 4

<div class="outline-text-4" id="text-2-1-4"><div class="exercise">Write a function which computes the local energy at \\(\\mathbf{r}\\), using the previously defined functions. The function accepts `a` and `r` as input arguments and returns the local kinetic energy.

</div>\\\[ E\_L(\\mathbf{r}) = -\\frac{1}{2} \\frac{\\Delta \\Psi}{\\Psi} (\\mathbf{r}) + V(\\mathbf{r}) \\\]

**Python**

<div class="org-src-container">```
<pre class="src src-python"><span style="color: #a020f0;">def</span> <span style="color: #0000ff;">e_loc</span>(a,r):
    #<span style="color: #b22222;">TODO</span>
```

</div>**Fortran**

<div class="note">When you call a function in Fortran, you need to declare its return type. You might by accident choose a function name which is the same as an internal function of Fortran. So it is recommended to **always** use the keyword `external` to make sure the function you are calling is yours.

</div><div class="org-src-container">```
<pre class="src src-f90"><span style="color: #228b22;">double precision </span><span style="color: #a020f0;">function</span><span style="color: #a0522d;"> </span><span style="color: #0000ff;">e_loc</span><span style="color: #000000; background-color: #ffffff;">(a,r)</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in) ::<span style="color: #a0522d;"> a, r(3)</span>

  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> kinetic</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> potential</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end function</span> <span style="color: #0000ff;">e_loc</span>
```

</div></div></div><div class="outline-4" id="outline-container-orgfa02dda">#### <span class="section-number-4">2.1.5</span> Exercise 5

<div class="outline-text-4" id="text-2-1-5"><div class="exercise">Find the theoretical value of \\(a\\) for which \\(\\Psi\\) is an eigenfunction of \\(\\hat{H}\\).

</div></div></div></div><div class="outline-3" id="outline-container-org46b45c5">### <span class="section-number-3">2.2</span> Plot of the local energy along the \\(x\\) axis

<div class="outline-text-3" id="text-2-2">The program you will write in this section will be written in another file (`plot_hydrogen.py` or `plot_hydrogen.f90` for example). It will use the functions previously defined.

In Python, you should put at the beginning of the file

<div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>

<span style="color: #a020f0;">from</span> hydrogen <span style="color: #a020f0;">import</span> e_loc
```

</div>to be able to use the `e_loc` function of the `hydrogen.py` file.

In Fortran, you will need to compile all the source files together:

<div class="org-src-container">```
<pre class="src src-sh">gfortran hydrogen.f90 plot_hydrogen.f90 -o plot_hydrogen
```

</div></div><div class="outline-4" id="outline-container-org09ec0db">#### <span class="section-number-4">2.2.1</span> Exercise

<div class="outline-text-4" id="text-2-2-1"><div class="exercise">For multiple values of \\(a\\) (0.1, 0.2, 0.5, 1., 1.5, 2.), plot the local energy along the \\(x\\) axis. In Python, you can use matplotlib for example. In Fortran, it is convenient to write in a text file the values of \\(x\\) and \\(E\_L(\\mathbf{r})\\) for each point, and use Gnuplot to plot the files. With Gnuplot, you will need 2 blank lines to separate the data corresponding to different values of \\(a\\).

</div><div class="note">The potential and the kinetic energy both diverge at \\(r=0\\), so we choose a grid which does not contain the origin to avoid numerical issues.

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>

<span style="color: #a020f0;">import</span> numpy <span style="color: #a020f0;">as</span> np
<span style="color: #a020f0;">import</span> matplotlib.pyplot <span style="color: #a020f0;">as</span> plt

<span style="color: #a020f0;">from</span> hydrogen <span style="color: #a020f0;">import</span> e_loc

<span style="color: #a0522d;">x</span>=np.linspace(-5,5)
plt.figure(figsize=(10,5))

# <span style="color: #b22222;">TODO</span>

plt.tight_layout()
plt.legend()
plt.savefig(<span style="color: #8b2252;">"plot_py.png"</span>)
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">program</span> <span style="color: #0000ff;">plot</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> e_loc</span>

  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> x(50), dx</span>
  <span style="color: #228b22;">integer</span> ::<span style="color: #a0522d;"> i, j</span>

  dx = 10.d0/(<span style="color: #a020f0;">size</span>(x)-1)
  <span style="color: #a020f0;">do</span> i=1,<span style="color: #a020f0;">size</span>(x)
     x(i) = -5.d0 + (i-1)*dx
  <span style="color: #a020f0;">end do</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end program</span> <span style="color: #0000ff;">plot</span>
```

</div>To compile and run:

<div class="org-src-container">```
<pre class="src src-sh">gfortran hydrogen.f90 plot_hydrogen.f90 -o plot_hydrogen
./plot_hydrogen > data
```

</div>To plot the data using Gnuplot:

<div class="org-src-container">```
<pre class="src src-gnuplot">set grid
set xrange [-5:5]
set yrange [-2:1]
plot './data' index 0 using 1:2 with lines title 'a=0.1', \
     './data' index 1 using 1:2 with lines title 'a=0.2', \
     './data' index 2 using 1:2 with lines title 'a=0.5', \
     './data' index 3 using 1:2 with lines title 'a=1.0', \
     './data' index 4 using 1:2 with lines title 'a=1.5', \
     './data' index 5 using 1:2 with lines title 'a=2.0'
```

</div></div></div></div><div class="outline-3" id="outline-container-orgfb47a4e">### <span class="section-number-3">2.3</span> Numerical estimation of the energy

<div class="outline-text-3" id="text-2-3">If the space is discretized in small volume elements \\(\\mathbf{r}\_i\\) of size \\(\\delta \\mathbf{r}\\), the expression of \\(\\langle E\_L \\rangle\_{\\Psi^2}\\) becomes a weighted average of the local energy, where the weights are the values of the wave function square at \\(\\mathbf{r}\_i\\) multiplied by the volume element:

\\\[ \\langle E \\rangle\_{\\Psi^2} \\approx \\frac{\\sum\_i w\_i E\_L(\\mathbf{r}\_i)}{\\sum\_i w\_i}, \\;\\; w\_i = \\left|\\Psi(\\mathbf{r}\_i)\\right|^2 \\delta \\mathbf{r} \\\]

<div class="note">The energy is biased because:

- The volume elements are not infinitely small (discretization error)
- The energy is evaluated only inside the box (incompleteness of the space)

</div></div><div class="outline-4" id="outline-container-org74b4c2f">#### <span class="section-number-4">2.3.1</span> Exercise

<div class="outline-text-4" id="text-2-3-1"><div class="exercise">Compute a numerical estimate of the energy using a grid of \\(50\\times50\\times50\\) points in the range \\((-5,-5,-5) \\le \\mathbf{r} \\le (5,5,5)\\).

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>

<span style="color: #a020f0;">import</span> numpy <span style="color: #a020f0;">as</span> np
<span style="color: #a020f0;">from</span> hydrogen <span style="color: #a020f0;">import</span> e_loc, psi

<span style="color: #a0522d;">interval</span> = np.linspace(-5,5,num=50)
<span style="color: #a0522d;">delta</span> = (interval[1]-interval[0])**3

<span style="color: #a0522d;">r</span> = np.array([0.,0.,0.])

<span style="color: #a020f0;">for</span> a <span style="color: #a020f0;">in</span> [0.1, 0.2, 0.5, 0.9, 1., 1.5, 2.]:
    # <span style="color: #b22222;">TODO</span>
    <span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"a = {a} \t E = {E}"</span>)

```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">program</span> <span style="color: #0000ff;">energy_hydrogen</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> e_loc, psi</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> x(50), w, delta, energy, dx, r(3), a(6), norm</span>
  <span style="color: #228b22;">integer</span> ::<span style="color: #a0522d;"> i, k, l, j</span>

  a = (/ 0.1d0, 0.2d0, 0.5d0, 1.d0, 1.5d0, 2.d0 /)

  dx = 10.d0/(<span style="color: #a020f0;">size</span>(x)-1)
  <span style="color: #a020f0;">do</span> i=1,<span style="color: #a020f0;">size</span>(x)
     x(i) = -5.d0 + (i-1)*dx
  <span style="color: #a020f0;">end do</span>

  <span style="color: #a020f0;">do</span> j=1,<span style="color: #a020f0;">size</span>(a)

     ! <span style="color: #b22222;">TODO</span>

     <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'a = '</span>, a(j), <span style="color: #8b2252;">'    E = '</span>, energy
  <span style="color: #a020f0;">end do</span>

<span style="color: #a020f0;">end program</span> <span style="color: #0000ff;">energy_hydrogen</span>
```

</div>To compile the Fortran and run it:

<div class="org-src-container">```
<pre class="src src-sh">gfortran hydrogen.f90 energy_hydrogen.f90 -o energy_hydrogen
./energy_hydrogen
```

</div></div></div></div><div class="outline-3" id="outline-container-org1d2fd58">### <span class="section-number-3">2.4</span> Variance of the local energy

<div class="outline-text-3" id="text-2-4">The variance of the local energy is a functional of \\(\\Psi\\) which measures the magnitude of the fluctuations of the local energy associated with \\(\\Psi\\) around its average:

\\\[ \\sigma^2(E\_L) = \\frac{\\int |\\Psi(\\mathbf{r})|^2\\, \\left\[ E\_L(\\mathbf{r}) - E \\right\]^2 \\, d\\mathbf{r}}{\\int |\\Psi(\\mathbf{r}) |^2 d\\mathbf{r}} \\\] which can be simplified as

\\\[ \\sigma^2(E\_L) = \\langle E\_L^2 \\rangle\_{\\Psi^2} - \\langle E\_L \\rangle\_{\\Psi^2}^2.\\\]

If the local energy is constant (i.e. \\(\\Psi\\) is an eigenfunction of \\(\\hat{H}\\)) the variance is zero, so the variance of the local energy can be used as a measure of the quality of a wave function.

</div><div class="outline-4" id="outline-container-org39d6a49">#### <span class="section-number-4">2.4.1</span> Exercise (optional)

<div class="outline-text-4" id="text-2-4-1"><div class="exercise">Prove that : \\\[\\langle \\left( E - \\langle E \\rangle\_{\\Psi^2} \\right)^2\\rangle\_{\\Psi^2} = \\langle E^2 \\rangle\_{\\Psi^2} - \\langle E \\rangle\_{\\Psi^2}^2 \\\]

</div></div></div><div class="outline-4" id="outline-container-org67a65e8">#### <span class="section-number-4">2.4.2</span> Exercise

<div class="outline-text-4" id="text-2-4-2"><div class="exercise">Add the calculation of the variance to the previous code, and compute a numerical estimate of the variance of the local energy using a grid of \\(50\\times50\\times50\\) points in the range \\((-5,-5,-5) \\le \\mathbf{r} \\le (5,5,5)\\) for different values of \\(a\\).

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>

<span style="color: #a020f0;">import</span> numpy <span style="color: #a020f0;">as</span> np <span style="color: #a020f0;">from</span> hydrogen <span style="color: #a020f0;">import</span> e_loc, psi

<span style="color: #a0522d;">interval</span> = np.linspace(-5,5,num=50)

<span style="color: #a0522d;">delta</span> = (interval[1]-interval[0])**3

<span style="color: #a0522d;">r</span> = np.array([0.,0.,0.])

<span style="color: #a020f0;">for</span> a <span style="color: #a020f0;">in</span> [0.1, 0.2, 0.5, 0.9, 1., 1.5, 2.]:

    # <span style="color: #b22222;">TODO</span>

    <span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"a = {a} \t E = {E:10.8f} \t \sigma^2 = {s2:10.8f}"</span>)
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">program</span> <span style="color: #0000ff;">variance_hydrogen</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>

  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> x(50), w, delta, energy, energy2</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> dx, r(3), a(6), norm, e_tmp, s2</span>
  <span style="color: #228b22;">integer</span>          ::<span style="color: #a0522d;"> i, k, l, j</span>

  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> e_loc, psi</span>

  a = (/ 0.1d0, 0.2d0, 0.5d0, 1.d0, 1.5d0, 2.d0 /)

  dx = 10.d0/(<span style="color: #a020f0;">size</span>(x)-1)
  <span style="color: #a020f0;">do</span> i=1,<span style="color: #a020f0;">size</span>(x)
     x(i) = -5.d0 + (i-1)*dx
  <span style="color: #a020f0;">end do</span>

  <span style="color: #a020f0;">do</span> j=1,<span style="color: #a020f0;">size</span>(a)

     ! <span style="color: #b22222;">TODO</span>

     <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'a = '</span>, a(j), <span style="color: #8b2252;">'    E = '</span>, energy
  <span style="color: #a020f0;">end do</span>

<span style="color: #a020f0;">end program</span> <span style="color: #0000ff;">variance_hydrogen</span>
```

</div>To compile and run:

<div class="org-src-container">```
<pre class="src src-sh">gfortran hydrogen.f90 variance_hydrogen.f90 -o variance_hydrogen
./variance_hydrogen
```

</div></div></div></div></div><div class="outline-2" id="outline-container-org670b628"><span class="section-number-2">3</span> Variational Monte Carlo
---------------------------------------------------------------

<div class="outline-text-2" id="text-3">Numerical integration with deterministic methods is very efficient in low dimensions. When the number of dimensions becomes large, instead of computing the average energy as a numerical integration on a grid, it is usually more efficient to use Monte Carlo sampling.

Moreover, Monte Carlo sampling will allow us to remove the bias due to the discretization of space, and compute a statistical confidence interval.

</div><div class="outline-3" id="outline-container-org062bbf8">### <span class="section-number-3">3.1</span> Computation of the statistical error

<div class="outline-text-3" id="text-3-1">To compute the statistical error, you need to perform \\(M\\) independent Monte Carlo calculations. You will obtain \\(M\\) different estimates of the energy, which are expected to have a Gaussian distribution for large \\(M\\), according to the [Central Limit Theorem](https://en.wikipedia.org/wiki/Central_limit_theorem).

The estimate of the energy is

\\\[ E = \\frac{1}{M} \\sum\_{i=1}^M E\_i \\\]

The variance of the average energies can be computed as

\\\[ \\sigma^2 = \\frac{1}{M-1} \\sum\_{i=1}^{M} (E\_i - E)^2 \\\]

And the confidence interval is given by

\\\[ E \\pm \\delta E, \\text{ where } \\delta E = \\frac{\\sigma}{\\sqrt{M}} \\\]

</div><div class="outline-4" id="outline-container-orge22e1d8">#### <span class="section-number-4">3.1.1</span> Exercise

<div class="outline-text-4" id="text-3-1-1"><div class="exercise">Write a function returning the average and statistical error of an input array.

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>

<span style="color: #a020f0;">from</span> math <span style="color: #a020f0;">import</span> sqrt
<span style="color: #a020f0;">def</span> <span style="color: #0000ff;">ave_error</span>(arr):
    #<span style="color: #b22222;">TODO</span>
    <span style="color: #a020f0;">return</span> (average, error)
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">subroutine</span> <span style="color: #0000ff;">ave_error</span>(x,n,ave,err)
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">integer</span>, <span style="color: #a020f0;">intent</span>(in)           ::<span style="color: #a0522d;"> n</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> x(n)</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(out) ::<span style="color: #a0522d;"> ave, err</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end subroutine</span> <span style="color: #0000ff;">ave_error</span>
```

</div></div></div></div><div class="outline-3" id="outline-container-org77b3c6a">### <span class="section-number-3">3.2</span> Uniform sampling in the box

<div class="outline-text-3" id="text-3-2">We will now perform our first Monte Carlo calculation to compute the energy of the hydrogen atom.

Consider again the expression of the energy

\begin{eqnarray*} E &amp; = &amp; \frac{\int E_L(\mathbf{r})|\Psi(\mathbf{r})|^2\,d\mathbf{r}}{\int |\Psi(\mathbf{r}) |^2 d\mathbf{r}}\,. \end{eqnarray*} Clearly, the square of the wave function is a good choice of probability density to sample but we will start with something simpler and rewrite the energy as

\begin{eqnarray*} E &amp; = &amp; \frac{\int E_L(\mathbf{r})\frac{|\Psi(\mathbf{r})|^2}{P(\mathbf{r})}P(\mathbf{r})\, \,d\mathbf{r}}{\int \frac{|\Psi(\mathbf{r})|^2 }{P(\mathbf{r})}P(\mathbf{r})d\mathbf{r}}\,. \end{eqnarray*} Here, we will sample a uniform probability \\(P(\\mathbf{r})\\) in a cube of volume \\(L^3\\) centered at the origin:

\\\[ P(\\mathbf{r}) = \\frac{1}{L^3}\\,, \\\]

and zero outside the cube.

One Monte Carlo run will consist of \\(N\_{\\rm MC}\\) Monte Carlo iterations. At every Monte Carlo iteration:

- Draw a random point \\(\\mathbf{r}\_i\\) in the box \\((-5,-5,-5) \\le (x,y,z) \\le (5,5,5)\\)
- Compute \\(|\\Psi(\\mathbf{r}\_i)|^2\\) and accumulate the result in a variable `normalization`
- Compute \\(|\\Psi(\\mathbf{r}\_i)|^2 \\times E\_L(\\mathbf{r}\_i)\\), and accumulate the result in a variable `energy`

Once all the iterations have been computed, the run returns the average energy \\(\\bar{E}\_k\\) over the \\(N\_{\\rm MC}\\) iterations of the run.

To compute the statistical error, perform \\(M\\) independent runs. The final estimate of the energy will be the average over the \\(\\bar{E}\_k\\), and the variance of the \\(\\bar{E}\_k\\) will be used to compute the statistical error.

</div><div class="outline-4" id="outline-container-org313f15c">#### <span class="section-number-4">3.2.1</span> Exercise

<div class="outline-text-4" id="text-3-2-1"><div class="exercise">Parameterize the wave function with \\(a=1.2\\). Perform 30 independent Monte Carlo runs, each with 100 000 Monte Carlo steps. Store the final energies of each run and use this array to compute the average energy and the associated error bar.

</div>**Python**

<div class="note">To draw a uniform random number in Python, you can use the [`random.uniform`](https://numpy.org/doc/stable/reference/random/generated/numpy.random.uniform.html) function of Numpy.

</div><div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>

<span style="color: #a020f0;">from</span> hydrogen  <span style="color: #a020f0;">import</span> *
<span style="color: #a020f0;">from</span> qmc_stats <span style="color: #a020f0;">import</span> *

<span style="color: #a020f0;">def</span> <span style="color: #0000ff;">MonteCarlo</span>(a, nmax):
     # <span style="color: #b22222;">TODO</span>

<span style="color: #a0522d;">a</span>    = 1.2
<span style="color: #a0522d;">nmax</span> = 100000

#<span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"E = {E} +/- {deltaE}"</span>)
```

</div>**Fortran**

<div class="note">To draw a uniform random number in Fortran, you can use the [`RANDOM_NUMBER`](https://gcc.gnu.org/onlinedocs/gfortran/RANDOM_005fNUMBER.html) subroutine.

</div><div class="note">When running Monte Carlo calculations, the number of steps is usually very large. We expect `nmax` to be possibly larger than 2 billion, so we use 8-byte integers (`integer*8`) to represent it, as well as the index of the current step.

</div><div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">subroutine</span> <span style="color: #0000ff;">uniform_montecarlo</span>(a,nmax,energy)
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> a</span>
  <span style="color: #228b22;">integer</span>*8       , <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> nmax</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(out) ::<span style="color: #a0522d;"> energy</span>

  <span style="color: #228b22;">integer</span>*8        ::<span style="color: #a0522d;"> istep</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> norm, r(3), w</span>

  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> e_loc, psi</span>

  ! <span style="color: #b22222;">TODO</span>
<span style="color: #a020f0;">end subroutine</span> <span style="color: #0000ff;">uniform_montecarlo</span>

<span style="color: #a020f0;">program</span> <span style="color: #0000ff;">qmc</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> a = 1.2d0</span>
  <span style="color: #228b22;">integer</span>*8       , <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> nmax = 100000</span>
  <span style="color: #228b22;">integer</span>         , <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> nruns = 30</span>

  <span style="color: #228b22;">integer</span>          ::<span style="color: #a0522d;"> irun</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> X(nruns)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> ave, err</span>

  !<span style="color: #b22222;">TODO</span>

  <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'E = '</span>, ave, <span style="color: #8b2252;">'+/-'</span>, err

<span style="color: #a020f0;">end program</span> <span style="color: #0000ff;">qmc</span>
```

</div><div class="org-src-container">```
<pre class="src src-sh">gfortran hydrogen.f90 qmc_stats.f90 qmc_uniform.f90 -o qmc_uniform
./qmc_uniform
```

</div></div></div></div><div class="outline-3" id="outline-container-orgdffe812">### <span class="section-number-3">3.3</span> Metropolis sampling with \\(\\Psi^2\\)

<div class="outline-text-3" id="text-3-3">We will now use the square of the wave function to sample random points distributed with the probability density \\\[ P(\\mathbf{r}) = \\frac{|\\Psi(\\mathbf{r})|^2}{\\int |\\Psi(\\mathbf{r})|^2 d\\mathbf{r}}\\,. \\\]

The expression of the average energy is now simplified as the average of the local energies, since the weights are taken care of by the sampling:

\\\[ E \\approx \\frac{1}{N\_{\\rm MC}}\\sum\_{i=1}^{N\_{\\rm MC}} E\_L(\\mathbf{r}\_i)\\,. \\\]

To sample a chosen probability density, an efficient method is the [Metropolis-Hastings sampling algorithm](https://en.wikipedia.org/wiki/Metropolis%E2%80%93Hastings_algorithm). Starting from a random initial position \\(\\mathbf{r}\_0\\), we will realize a random walk:

\\\[ \\mathbf{r}\_0 \\rightarrow \\mathbf{r}\_1 \\rightarrow \\mathbf{r}\_2 \\ldots \\rightarrow \\mathbf{r}\_{N\_{\\rm MC}}\\,, \\\]

according to the following algorithm.

At every step, we propose a new move according to a transition probability \\(T(\\mathbf{r}\_{n}\\rightarrow\\mathbf{r}\_{n+1})\\) of our choice.

For simplicity, we will move the electron in a 3-dimensional box of side \\(2\\delta L\\) centered at the current position of the electron:

\\\[ \\mathbf{r}\_{n+1} = \\mathbf{r}\_{n} + \\delta L \\, \\mathbf{u} \\\]

where \\(\\delta L\\) is a fixed constant, and \\(\\mathbf{u}\\) is a uniform random number in a 3-dimensional box \\((-1,-1,-1) \\le \\mathbf{u} \\le (1,1,1)\\).

After having moved the electron, we add the accept/reject step that guarantees that the distribution of the \\(\\mathbf{r}\_n\\) is \\(\\Psi^2\\). This amounts to accepting the move with probability

\\\[ A(\\mathbf{r}\_{n}\\rightarrow\\mathbf{r}\_{n+1}) = \\min\\left(1,\\frac{T(\\mathbf{r}\_{n+1}\\rightarrow\\mathbf{r}\_{n}) P(\\mathbf{r}\_{n+1})}{T(\\mathbf{r}\_{n}\\rightarrow\\mathbf{r}\_{n+1})P(\\mathbf{r}\_{n})}\\right)\\,, \\\]

which, for our choice of transition probability, becomes

\\\[ A(\\mathbf{r}\_{n}\\rightarrow\\mathbf{r}\_{n+1}) = \\min\\left(1,\\frac{P(\\mathbf{r}\_{n+1})}{P(\\mathbf{r}\_{n})}\\right)= \\min\\left(1,\\frac{|\\Psi(\\mathbf{r}\_{n+1})|^2}{|\\Psi(\\mathbf{r}\_{n})|^2}\\right)\\,. \\\]

<div class="exercise">Explain why the transition probability cancels out in the expression of \\(A\\).

</div>Also note that we do not need to compute the norm of the wave function!

The algorithm is summarized as follows:

1. Evaluate the local energy at \\(\\mathbf{r}\_n\\) and accumulate it
2. Compute a new position \\(\\mathbf{r'} = \\mathbf{r}\_n + \\delta L\\, \\mathbf{u}\\)
3. Evaluate \\(\\Psi(\\mathbf{r}')\\) at the new position
4. Compute the ratio \\(A = \\frac{\\left|\\Psi(\\mathbf{r'})\\right|^2}{\\left|\\Psi(\\mathbf{r}\_{n})\\right|^2}\\)
5. Draw a uniform random number \\(v \\in \[0,1\]\\)
6. if \\(v \\le A\\), accept the move : set \\(\\mathbf{r}\_{n+1} = \\mathbf{r'}\\)
7. else, reject the move : set \\(\\mathbf{r}\_{n+1} = \\mathbf{r}\_n\\)

<div class="note">A common error is to remove the rejected samples from the calculation of the average. **Don't do it!**

All samples should be kept, from both accepted *and* rejected moves.

</div></div><div class="outline-4" id="outline-container-org33983d0">#### <span class="section-number-4">3.3.1</span> Optimal step size

<div class="outline-text-4" id="text-3-3-1">If the box is infinitely small, the ratio will be very close to one and all the steps will be accepted. However, the moves will be very correlated and you will visit the configurational space very slowly.

On the other hand, if you propose too large moves, the number of accepted steps will decrease because the ratios might become small. If the number of accepted steps is close to zero, then the space is not well sampled either.

The size of the move should be adjusted so that it is as large as possible, keeping the number of accepted steps not too small. To achieve that, we define the acceptance rate as the number of accepted steps over the total number of steps. Adjusting the time step such that the acceptance rate is close to 0.5 is a good compromise for the current problem.

<div class="note">Below, we use the symbol \\(\\delta t\\) to denote \\(\\delta L\\) since we will use the same variable later on to store a time step.

</div></div></div><div class="outline-4" id="outline-container-org0b89863">#### <span class="section-number-4">3.3.2</span> Exercise

<div class="outline-text-4" id="text-3-3-2"><div class="exercise">Modify the program of the previous section to compute the energy, sampled with \\(\\Psi^2\\).

Compute also the acceptance rate, so that you can adapt the time step in order to have an acceptance rate close to 0.5.

Can you observe a reduction in the statistical error?

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>

<span style="color: #a020f0;">from</span> hydrogen  <span style="color: #a020f0;">import</span> *
<span style="color: #a020f0;">from</span> qmc_stats <span style="color: #a020f0;">import</span> *

<span style="color: #a020f0;">def</span> <span style="color: #0000ff;">MonteCarlo</span>(a,nmax,dt):

    # <span style="color: #b22222;">TODO</span>

    <span style="color: #a020f0;">return</span> energy/nmax, N_accep/nmax


# <span style="color: #b22222;">Run simulation</span>
<span style="color: #a0522d;">a</span>    = 1.2
<span style="color: #a0522d;">nmax</span> = 100000
<span style="color: #a0522d;">dt</span>   = #<span style="color: #b22222;">TODO</span>

<span style="color: #a0522d;">X0</span> = [ MonteCarlo(a,nmax,dt) <span style="color: #a020f0;">for</span> i <span style="color: #a020f0;">in</span> <span style="color: #483d8b;">range</span>(30)]

# <span style="color: #b22222;">Energy</span>
<span style="color: #a0522d;">X</span> = [ x <span style="color: #a020f0;">for</span> (x, _) <span style="color: #a020f0;">in</span> X0 ]
<span style="color: #a0522d;">E</span>, <span style="color: #a0522d;">deltaE</span> = ave_error(X)
<span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"E = {E} +/- {deltaE}"</span>)

# <span style="color: #b22222;">Acceptance rate</span>
<span style="color: #a0522d;">X</span> = [ x <span style="color: #a020f0;">for</span> (_, x) <span style="color: #a020f0;">in</span> X0 ]
<span style="color: #a0522d;">A</span>, <span style="color: #a0522d;">deltaA</span> = ave_error(X)
<span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"A = {A} +/- {deltaA}"</span>)
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">subroutine</span> <span style="color: #0000ff;">metropolis_montecarlo</span>(a,nmax,dt,energy,accep)
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> a</span>
  <span style="color: #228b22;">integer</span>*8       , <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> nmax</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> dt</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(out) ::<span style="color: #a0522d;"> energy</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(out) ::<span style="color: #a0522d;"> accep</span>

  <span style="color: #228b22;">integer</span>*8        ::<span style="color: #a0522d;"> istep</span>
  <span style="color: #228b22;">integer</span>*8        ::<span style="color: #a0522d;"> n_accep</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> r_old(3), r_new(3), psi_old, psi_new</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> v, ratio</span>

  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> e_loc, psi, gaussian</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end subroutine</span> <span style="color: #0000ff;">metropolis_montecarlo</span>

<span style="color: #a020f0;">program</span> <span style="color: #0000ff;">qmc</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> a     = 1.2d0</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> dt    = </span>! <span style="color: #b22222;">TODO</span>
  <span style="color: #228b22;">integer</span>*8       , <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> nmax  = 100000</span>
  <span style="color: #228b22;">integer</span>         , <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> nruns = 30</span>

  <span style="color: #228b22;">integer</span>          ::<span style="color: #a0522d;"> irun</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> X(nruns), Y(nruns)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> ave, err</span>

  <span style="color: #a020f0;">do</span> irun=1,nruns
     <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">metropolis_montecarlo</span>(a,nmax,dt,X(irun),Y(irun))
  <span style="color: #a020f0;">enddo</span>

  <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">ave_error</span>(X,nruns,ave,err)
  <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'E = '</span>, ave, <span style="color: #8b2252;">'+/-'</span>, err

  <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">ave_error</span>(Y,nruns,ave,err)
  <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'A = '</span>, ave, <span style="color: #8b2252;">'+/-'</span>, err

<span style="color: #a020f0;">end program</span> <span style="color: #0000ff;">qmc</span>
```

</div><div class="org-src-container">```
<pre class="src src-sh">gfortran hydrogen.f90 qmc_stats.f90 qmc_metropolis.f90 -o qmc_metropolis
./qmc_metropolis
```

</div></div></div></div><div class="outline-3" id="outline-container-org1795441">### <span class="section-number-3">3.4</span> Generalized Metropolis algorithm

<div class="outline-text-3" id="text-3-4">One can use more efficient numerical schemes to move the electrons by choosing a smarter expression for the transition probability.

The Metropolis acceptance step has to be adapted accordingly to ensure that the detailed balance condition is satisfied. This means that the acceptance probability \\(A\\) is chosen so that it is consistent with the probability of leaving \\(\\mathbf{r}\_n\\) and the probability of entering \\(\\mathbf{r}\_{n+1}\\):

\\\[ A(\\mathbf{r}\_{n} \\rightarrow \\mathbf{r}\_{n+1}) = \\min \\left( 1, \\frac{T(\\mathbf{r}\_{n+1} \\rightarrow \\mathbf{r}\_{n}) P(\\mathbf{r}\_{n+1})} {T(\\mathbf{r}\_{n} \\rightarrow \\mathbf{r}\_{n+1}) P(\\mathbf{r}\_{n})} \\right) \\\] where \\(T(\\mathbf{r}\_n \\rightarrow \\mathbf{r}\_{n+1})\\) is the probability of transition from \\(\\mathbf{r}\_n\\) to \\(\\mathbf{r}\_{n+1}\\).

In the previous example, we were using uniform sampling in a box centered at the current position. Hence, the transition probability was symmetric

\\\[ T(\\mathbf{r}\_{n} \\rightarrow \\mathbf{r}\_{n+1}) = T(\\mathbf{r}\_{n+1} \\rightarrow \\mathbf{r}\_{n}) = \\text{constant}\\,, \\\]

so the expression of \\(A\\) was simplified to the ratios of the squared wave functions.

Now, if instead of drawing uniform random numbers, we choose to draw Gaussian random numbers with zero mean and variance \\(\\delta t\\), the transition probability becomes:

\\\[ T(\\mathbf{r}\_{n} \\rightarrow \\mathbf{r}\_{n+1}) = \\frac{1}{(2\\pi\\,\\delta t)^{3/2}} \\exp \\left\[ - \\frac{\\left( \\mathbf{r}\_{n+1} - \\mathbf{r}\_{n} \\right)^2}{2\\delta t} \\right\]\\,. \\\]

Furthermore, to sample the density even better, we can "push" the electrons into in the regions of high probability, and "pull" them away from the low-probability regions. This will increase the acceptance ratios and improve the sampling.

To do this, we can use the gradient of the probability density

\\\[ \\frac{\\nabla \[ \\Psi^2 \]}{\\Psi^2} = 2 \\frac{\\nabla \\Psi}{\\Psi}\\,, \\\]

and add the so-called drift vector, \\(\\frac{\\nabla \\Psi}{\\Psi}\\), so that the numerical scheme becomes a drifted diffusion with transition probability:

\\\[ T(\\mathbf{r}\_{n} \\rightarrow \\mathbf{r}\_{n+1}) = \\frac{1}{(2\\pi\\,\\delta t)^{3/2}} \\exp \\left\[ - \\frac{\\left( \\mathbf{r}\_{n+1} - \\mathbf{r}\_{n} - \\delta t\\frac{\\nabla \\Psi(\\mathbf{r}\_n)}{\\Psi(\\mathbf{r}\_n)} \\right)^2}{2\\,\\delta t} \\right\]\\,. \\\]

The corresponding move is proposed as

\\\[ \\mathbf{r}\_{n+1} = \\mathbf{r}\_{n} + \\delta t\\, \\frac{\\nabla \\Psi(\\mathbf{r})}{\\Psi(\\mathbf{r})} + \\chi \\,, \\\]

where \\(\\chi\\) is a Gaussian random variable with zero mean and variance \\(\\delta t\\).

The algorithm of the previous exercise is only slighlty modified as:

1. Evaluate the local energy at \\(\\mathbf{r}\_{n}\\) and accumulate it
2. Compute a new position \\(\\mathbf{r'} = \\mathbf{r}\_n + \\delta t\\, \\frac{\\nabla \\Psi(\\mathbf{r})}{\\Psi(\\mathbf{r})} + \\chi\\)
3. Evaluate \\(\\Psi(\\mathbf{r}')\\) and \\(\\frac{\\nabla \\Psi(\\mathbf{r'})}{\\Psi(\\mathbf{r'})}\\) at the new position
4. Compute the ratio \\(A = \\frac{T(\\mathbf{r}' \\rightarrow \\mathbf{r}\_{n}) P(\\mathbf{r}')}{T(\\mathbf{r}\_{n} \\rightarrow \\mathbf{r}') P(\\mathbf{r}\_{n})}\\)
5. Draw a uniform random number \\(v \\in \[0,1\]\\)
6. if \\(v \\le A\\), accept the move : set \\(\\mathbf{r}\_{n+1} = \\mathbf{r'}\\)
7. else, reject the move : set \\(\\mathbf{r}\_{n+1} = \\mathbf{r}\_n\\)

</div><div class="outline-4" id="outline-container-org4a0843e">#### <span class="section-number-4">3.4.1</span> Gaussian random number generator

<div class="outline-text-4" id="text-3-4-1">To obtain Gaussian-distributed random numbers, you can apply the [Box Muller transform](https://en.wikipedia.org/wiki/Box%E2%80%93Muller_transform) to uniform random numbers:

\begin{eqnarray*} z_1 &amp;=&amp; \sqrt{-2 \ln u_1} \cos(2 \pi u_2) \\ z_2 &amp;=&amp; \sqrt{-2 \ln u_1} \sin(2 \pi u_2) \end{eqnarray*} Below is a Fortran implementation returning a Gaussian-distributed n-dimensional vector \\(\\mathbf{z}\\). This will be useful for the following sections.

**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">subroutine</span> <span style="color: #0000ff;">random_gauss</span>(z,n)
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">integer</span>, <span style="color: #a020f0;">intent</span>(in) ::<span style="color: #a0522d;"> n</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(out) ::<span style="color: #a0522d;"> z(n)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> u(n+1)</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> two_pi = 2.d0*dacos(-1.d0)</span>
  <span style="color: #228b22;">integer</span> ::<span style="color: #a0522d;"> i</span>

  <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">random_number</span>(u)

  <span style="color: #a020f0;">if</span> (<span style="color: #a020f0;">iand</span>(n,1) == 0) <span style="color: #a020f0;">then</span>
     ! <span style="color: #b22222;">n is even</span>
     <span style="color: #a020f0;">do</span> i=1,n,2
        z(i)   = dsqrt(-2.d0*dlog(u(i)))
        z(i+1) = z(i) * dsin( two_pi*u(i+1) )
        z(i)   = z(i) * dcos( two_pi*u(i+1) )
     <span style="color: #a020f0;">end do</span>

  <span style="color: #a020f0;">else</span>
     ! <span style="color: #b22222;">n is odd</span>
     <span style="color: #a020f0;">do</span> i=1,n-1,2
        z(i)   = dsqrt(-2.d0*dlog(u(i)))
        z(i+1) = z(i) * dsin( two_pi*u(i+1) )
        z(i)   = z(i) * dcos( two_pi*u(i+1) )
     <span style="color: #a020f0;">end do</span>

     z(n)   = dsqrt(-2.d0*dlog(u(n)))
     z(n)   = z(n) * dcos( two_pi*u(n+1) )

  <span style="color: #a020f0;">end if</span>

<span style="color: #a020f0;">end subroutine</span> <span style="color: #0000ff;">random_gauss</span>
```

</div>In Python, you can use the [`random.normal`](https://numpy.org/doc/stable/reference/random/generated/numpy.random.normal.html) function of Numpy.

</div></div><div class="outline-4" id="outline-container-org4a6aa65">#### <span class="section-number-4">3.4.2</span> Exercise 1

<div class="outline-text-4" id="text-3-4-2"><div class="exercise">If you use Fortran, copy/paste the `random_gauss` function in a Fortran file.

</div><div class="exercise">Write a function to compute the drift vector \\(\\frac{\\nabla \\Psi(\\mathbf{r})}{\\Psi(\\mathbf{r})}\\).

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python"><span style="color: #a020f0;">def</span> <span style="color: #0000ff;">drift</span>(a,r):
   # <span style="color: #b22222;">TODO</span>
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">subroutine</span> <span style="color: #0000ff;">drift</span>(a,r,b)
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> a, r(3)</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(out) ::<span style="color: #a0522d;"> b(3)</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end subroutine</span> <span style="color: #0000ff;">drift</span>
```

</div></div></div><div class="outline-4" id="outline-container-org35062aa">#### <span class="section-number-4">3.4.3</span> Exercise 2

<div class="outline-text-4" id="text-3-4-3"><div class="exercise">Modify the previous program to introduce the drift-diffusion scheme. (This is a necessary step for the next section on diffusion Monte Carlo).

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python">#<span style="color: #b22222;">!/usr/bin/env python3</span>

<span style="color: #a020f0;">from</span> hydrogen  <span style="color: #a020f0;">import</span> *
<span style="color: #a020f0;">from</span> qmc_stats <span style="color: #a020f0;">import</span> *

<span style="color: #a020f0;">def</span> <span style="color: #0000ff;">MonteCarlo</span>(a,nmax,dt):
   # <span style="color: #b22222;">TODO</span>

# <span style="color: #b22222;">Run simulation</span>
<span style="color: #a0522d;">a</span>    = 1.2
<span style="color: #a0522d;">nmax</span> = 100000
<span style="color: #a0522d;">dt</span>   = # <span style="color: #b22222;">TODO</span>

<span style="color: #a0522d;">X0</span> = [ MonteCarlo(a,nmax,dt) <span style="color: #a020f0;">for</span> i <span style="color: #a020f0;">in</span> <span style="color: #483d8b;">range</span>(30)]

# <span style="color: #b22222;">Energy</span>
<span style="color: #a0522d;">X</span> = [ x <span style="color: #a020f0;">for</span> (x, _) <span style="color: #a020f0;">in</span> X0 ]
<span style="color: #a0522d;">E</span>, <span style="color: #a0522d;">deltaE</span> = ave_error(X)
<span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"E = {E} +/- {deltaE}"</span>)

# <span style="color: #b22222;">Acceptance rate</span>
<span style="color: #a0522d;">X</span> = [ x <span style="color: #a020f0;">for</span> (_, x) <span style="color: #a020f0;">in</span> X0 ]
<span style="color: #a0522d;">A</span>, <span style="color: #a0522d;">deltaA</span> = ave_error(X)
<span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"A = {A} +/- {deltaA}"</span>)
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">subroutine</span> <span style="color: #0000ff;">variational_montecarlo</span>(a,dt,nmax,energy,accep)
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> a, dt</span>
  <span style="color: #228b22;">integer</span>*8       , <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> nmax</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(out) ::<span style="color: #a0522d;"> energy, accep</span>

  <span style="color: #228b22;">integer</span>*8        ::<span style="color: #a0522d;"> istep</span>
  <span style="color: #228b22;">integer</span>*8        ::<span style="color: #a0522d;"> n_accep</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> sq_dt, chi(3)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> psi_old, psi_new</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> r_old(3), r_new(3)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> d_old(3), d_new(3)</span>

  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> e_loc, psi</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end subroutine</span> <span style="color: #0000ff;">variational_montecarlo</span>

<span style="color: #a020f0;">program</span> <span style="color: #0000ff;">qmc</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> a     = 1.2d0</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> dt    = </span>! <span style="color: #b22222;">TODO</span>
  <span style="color: #228b22;">integer</span>*8       , <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> nmax  = 100000</span>
  <span style="color: #228b22;">integer</span>         , <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> nruns = 30</span>

  <span style="color: #228b22;">integer</span>          ::<span style="color: #a0522d;"> irun</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> X(nruns), accep(nruns)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> ave, err</span>

  <span style="color: #a020f0;">do</span> irun=1,nruns
     <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">variational_montecarlo</span>(a,dt,nmax,X(irun),accep(irun))
  <span style="color: #a020f0;">enddo</span>

  <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">ave_error</span>(X,nruns,ave,err)
  <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'E = '</span>, ave, <span style="color: #8b2252;">'+/-'</span>, err

  <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">ave_error</span>(accep,nruns,ave,err)
  <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'A = '</span>, ave, <span style="color: #8b2252;">'+/-'</span>, err

<span style="color: #a020f0;">end program</span> <span style="color: #0000ff;">qmc</span>
```

</div><div class="org-src-container">```
<pre class="src src-sh">gfortran hydrogen.f90 qmc_stats.f90 vmc_metropolis.f90 -o vmc_metropolis
./vmc_metropolis
```

</div></div></div></div></div><div class="outline-2" id="outline-container-org84089bb"><span class="section-number-2">4</span> Diffusion Monte Carlo
-------------------------------------------------------------

<div class="outline-text-2" id="text-4">As we have seen, Variational Monte Carlo is a powerful method to compute integrals in large dimensions. It is often used in cases where the expression of the wave function is such that the integrals can't be evaluated (multi-centered Slater-type orbitals, correlation factors, etc).

Diffusion Monte Carlo is different. It goes beyond the computation of the integrals associated with an input wave function, and aims at finding a near-exact numerical solution to the Schrödinger equation.

</div><div class="outline-3" id="outline-container-org16ba172">### <span class="section-number-3">4.1</span> Schrödinger equation in imaginary time

<div class="outline-text-3" id="text-4-1">Consider the time-dependent Schrödinger equation:

\\\[ i\\frac{\\partial \\Psi(\\mathbf{r},t)}{\\partial t} = (\\hat{H} -E\_{\\rm ref}) \\Psi(\\mathbf{r},t)\\,. \\\]

where we introduced a shift in the energy, \\(E\_{\\rm ref}\\), for reasons which will become apparent below.

We can expand a given starting wave function, \\(\\Psi(\\mathbf{r},0)\\), in the basis of the eigenstates of the time-independent Hamiltonian, \\(\\Phi\_k\\), with energies \\(E\_k\\):

\\\[ \\Psi(\\mathbf{r},0) = \\sum\_k a\_k\\, \\Phi\_k(\\mathbf{r}). \\\]

The solution of the Schrödinger equation at time \\(t\\) is

\\\[ \\Psi(\\mathbf{r},t) = \\sum\_k a\_k \\exp \\left( -i\\, (E\_k-E\_{\\rm ref})\\, t \\right) \\Phi\_k(\\mathbf{r}). \\\]

Now, if we replace the time variable \\(t\\) by an imaginary time variable \\(\\tau=i\\,t\\), we obtain

\\\[ -\\frac{\\partial \\psi(\\mathbf{r}, \\tau)}{\\partial \\tau} = (\\hat{H} -E\_{\\rm ref}) \\psi(\\mathbf{r}, \\tau) \\\]

where \\(\\psi(\\mathbf{r},\\tau) = \\Psi(\\mathbf{r},-i\\,\\tau)\\) and

\begin{eqnarray*} \psi(\mathbf{r},\tau) &amp;=&amp; \sum_k a_k \exp( -(E_k-E_{\rm ref})\, \tau) \Phi_k(\mathbf{r})\\ &amp;=&amp; \exp(-(E_0-E_{\rm ref})\, \tau)\sum_k a_k \exp( -(E_k-E_0)\, \tau) \Phi_k(\mathbf{r})\,. \end{eqnarray*} For large positive values of \\(\\tau\\), \\(\\psi\\) is dominated by the \\(k=0\\) term, namely, the lowest eigenstate. If we adjust \\(E\_{\\rm ref}\\) to the running estimate of \\(E\_0\\), we can expect that simulating the differetial equation in imaginary time will converge to the exact ground state of the system.

</div></div><div class="outline-3" id="outline-container-org61c215f">### <span class="section-number-3">4.2</span> Relation to diffusion

<div class="outline-text-3" id="text-4-2">The [diffusion equation](https://en.wikipedia.org/wiki/Diffusion_equation) of particles is given by

\\\[ \\frac{\\partial \\psi(\\mathbf{r},t)}{\\partial t} = D\\, \\Delta \\psi(\\mathbf{r},t) \\\]

where \\(D\\) is the diffusion coefficient. When the imaginary-time Schrödinger equation is written in terms of the kinetic energy and potential,

\\\[ \\frac{\\partial \\psi(\\mathbf{r}, \\tau)}{\\partial \\tau} = \\left(\\frac{1}{2}\\Delta - \[V(\\mathbf{r}) -E\_{\\rm ref}\]\\right) \\psi(\\mathbf{r}, \\tau)\\,, \\\]

it can be identified as the combination of:

- a diffusion equation (Laplacian)
- an equation whose solution is an exponential (potential)

The diffusion equation can be simulated by a Brownian motion:

\\\[ \\mathbf{r}\_{n+1} = \\mathbf{r}\_{n} + \\sqrt{\\delta t}\\, \\chi \\\]

where \\(\\chi\\) is a Gaussian random variable, and the potential term can be simulated by creating or destroying particles over time (a so-called branching process) or by simply considering it as a cumulative multiplicative weight along the diffusion trajectory (pure Diffusion Monte Carlo):

\\\[ \\prod\_i \\exp \\left( - (V(\\mathbf{r}\_i) - E\_{\\text{ref}}) \\delta t \\right). \\\]

We note that the ground-state wave function of a Fermionic system is antisymmetric and changes sign. Therefore, its interpretation as a probability distribution is somewhat problematic. In fact, mathematically, since the Bosonic ground state is lower in energy than the Fermionic one, for large \\(\\tau\\), the system will evolve towards the Bosonic solution.

For the systems you will study, this is not an issue:

- Hydrogen atom: You only have one electron!
- Two-electron system (\\(H\_2\\) or He): The ground-wave function is antisymmetric in the spin variables but symmetric in the space ones.

Therefore, in both cases, you are dealing with a "Bosonic" ground state.

</div></div><div class="outline-3" id="outline-container-org5ee9aee">### <span class="section-number-3">4.3</span> Importance sampling

<div class="outline-text-3" id="text-4-3">In a molecular system, the potential is far from being constant and, in fact, diverges at the inter-particle coalescence points. Hence, it results in very large fluctuations of the erm weight associated with the potental, making the calculations impossible in practice. Fortunately, if we multiply the Schrödinger equation by a chosen *trial wave function* \\(\\Psi\_T(\\mathbf{r})\\) (Hartree-Fock, Kohn-Sham determinant, CI wave function, *etc*), one obtains

\\\[ -\\frac{\\partial \\psi(\\mathbf{r},\\tau)}{\\partial \\tau} \\Psi\_T(\\mathbf{r}) = \\left\[ -\\frac{1}{2} \\Delta \\psi(\\mathbf{r},\\tau) + V(\\mathbf{r}) \\psi(\\mathbf{r},\\tau) \\right\] \\Psi\_T(\\mathbf{r}) \\\]

Defining \\(\\Pi(\\mathbf{r},\\tau) = \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r})\\), (see appendix for details)

\\\[ -\\frac{\\partial \\Pi(\\mathbf{r},\\tau)}{\\partial \\tau} = -\\frac{1}{2} \\Delta \\Pi(\\mathbf{r},\\tau) + \\nabla \\left\[ \\Pi(\\mathbf{r},\\tau) \\frac{\\nabla \\Psi\_T(\\mathbf{r})}{\\Psi\_T(\\mathbf{r})} \\right\] + (E\_L(\\mathbf{r})-E\_{\\rm ref})\\Pi(\\mathbf{r},\\tau) \\\]

The new "kinetic energy" can be simulated by the drift-diffusion scheme presented in the previous section (VMC). The new "potential" is the local energy, which has smaller fluctuations when \\(\\Psi\_T\\) gets closer to the exact wave function. This term can be simulated by \\\[ \\prod\_i \\exp \\left( - (E\_L(\\mathbf{r}\_i) - E\_{\\text{ref}}) \\delta t \\right). \\\] where \\(E\_{\\rm ref}\\) is the constant we had introduced above, which is adjusted to an estimate of the average energy to keep the weights close to one.

This equation generates the *N*-electron density \\(\\Pi\\), which is the product of the ground state solution with the trial wave function. You may then ask: how can we compute the total energy of the system?

To this aim, we use the *mixed estimator* of the energy:

\begin{eqnarray*} E(\tau) &amp;=&amp; \frac{\langle \psi(\tau) | \hat{H} | \Psi_T \rangle}{\langle \psi(\tau) | \Psi_T \rangle}\\ &amp;=&amp; \frac{\int \psi(\mathbf{r},\tau) \hat{H} \Psi_T(\mathbf{r}) d\mathbf{r}} {\int \psi(\mathbf{r},\tau) \Psi_T(\mathbf{r}) d\mathbf{r}} \\ &amp;=&amp; \frac{\int \psi(\mathbf{r},\tau) \Psi_T(\mathbf{r}) E_L(\mathbf{r}) d\mathbf{r}} {\int \psi(\mathbf{r},\tau) \Psi_T(\mathbf{r}) d\mathbf{r}} \,. \end{eqnarray*} For large \\(\\tau\\), we have that

\\\[ \\Pi(\\mathbf{r},\\tau) =\\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\rightarrow \\Phi\_0(\\mathbf{r}) \\Psi\_T(\\mathbf{r})\\,, \\\]

and, using that \\(\\hat{H}\\) is Hermitian and that \\(\\Phi\_0\\) is an eigenstate of the Hamiltonian, we obtain for large \\(\\tau\\)

\\\[ E(\\tau) = \\frac{\\langle \\psi\_\\tau | \\hat{H} | \\Psi\_T \\rangle} {\\langle \\psi\_\\tau | \\Psi\_T \\rangle} = \\frac{\\langle \\Psi\_T | \\hat{H} | \\psi\_\\tau \\rangle} {\\langle \\Psi\_T | \\psi\_\\tau \\rangle} \\rightarrow E\_0 \\frac{\\langle \\Psi\_T | \\Phi\_0 \\rangle} {\\langle \\Psi\_T | \\Phi\_0 \\rangle} = E\_0 \\\]

Therefore, we can compute the energy within DMC by generating the density \\(\\Pi\\) with random walks, and simply averaging the local energies computed with the trial wave function.

</div><div class="outline-4" id="outline-container-org5805991">#### <span class="section-number-4">4.3.1</span> Appendix : Details of the Derivation

<div class="outline-text-4" id="text-4-3-1">\\\[ -\\frac{\\partial \\psi(\\mathbf{r},\\tau)}{\\partial \\tau} \\Psi\_T(\\mathbf{r}) = \\left\[ -\\frac{1}{2} \\Delta \\psi(\\mathbf{r},\\tau) + V(\\mathbf{r}) \\psi(\\mathbf{r},\\tau) \\right\] \\Psi\_T(\\mathbf{r}) \\\]

\\\[ -\\frac{\\partial \\big\[ \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\big\]}{\\partial \\tau} = -\\frac{1}{2} \\Big( \\Delta \\big\[ \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\big\] - \\psi(\\mathbf{r},\\tau) \\Delta \\Psi\_T(\\mathbf{r}) - 2 \\nabla \\psi(\\mathbf{r},\\tau) \\nabla \\Psi\_T(\\mathbf{r}) \\Big) + V(\\mathbf{r}) \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\\]

\\\[ -\\frac{\\partial \\big\[ \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\big\]}{\\partial \\tau} = -\\frac{1}{2} \\Delta \\big\[\\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\big\] + \\frac{1}{2} \\psi(\\mathbf{r},\\tau) \\Delta \\Psi\_T(\\mathbf{r}) + \\Psi\_T(\\mathbf{r})\\nabla \\psi(\\mathbf{r},\\tau) \\frac{\\nabla \\Psi\_T(\\mathbf{r})}{\\Psi\_T(\\mathbf{r})} + V(\\mathbf{r}) \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\\]

\\\[ -\\frac{\\partial \\big\[ \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\big\]}{\\partial \\tau} = -\\frac{1}{2} \\Delta \\big\[\\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\big\] + \\psi(\\mathbf{r},\\tau) \\Delta \\Psi\_T(\\mathbf{r}) + \\Psi\_T(\\mathbf{r})\\nabla \\psi(\\mathbf{r},\\tau) \\frac{\\nabla \\Psi\_T(\\mathbf{r})}{\\Psi\_T(\\mathbf{r})} + E\_L(\\mathbf{r}) \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\\] \\\[ -\\frac{\\partial \\big\[ \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\big\]}{\\partial \\tau} = -\\frac{1}{2} \\Delta \\big\[\\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\big\] + \\nabla \\left\[ \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\frac{\\nabla \\Psi\_T(\\mathbf{r})}{\\Psi\_T(\\mathbf{r})} \\right\] + E\_L(\\mathbf{r}) \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r}) \\\]

Defining \\(\\Pi(\\mathbf{r},t) = \\psi(\\mathbf{r},\\tau) \\Psi\_T(\\mathbf{r})\\),

\\\[ -\\frac{\\partial \\Pi(\\mathbf{r},\\tau)}{\\partial \\tau} = -\\frac{1}{2} \\Delta \\Pi(\\mathbf{r},\\tau) + \\nabla \\left\[ \\Pi(\\mathbf{r},\\tau) \\frac{\\nabla \\Psi\_T(\\mathbf{r})}{\\Psi\_T(\\mathbf{r})} \\right\] + E\_L(\\mathbf{r}) \\Pi(\\mathbf{r},\\tau) \\\]

</div></div></div><div class="outline-3" id="outline-container-org8801356">### <span class="section-number-3">4.4</span> Pure Diffusion Monte Carlo

<div class="outline-text-3" id="text-4-4">Instead of having a variable number of particles to simulate the branching process as in the *Diffusion Monte Carlo* (DMC) algorithm, we use variant called *pure Diffusion Monte Carlo* (PDMC) where the potential term is considered as a cumulative product of weights:

\begin{eqnarray*} W(\mathbf{r}_n, \tau) = \prod_{i=1}^{n} \exp \left( -\delta t\, (E_L(\mathbf{r}_i) - E_{\text{ref}}) \right) = \prod_{i=1}^{n} w(\mathbf{r}_i) \end{eqnarray*} where \\(\\mathbf{r}\_i\\) are the coordinates along the trajectory and we introduced a *time-step variable* \\(\\delta t\\) to discretize the integral.

The PDMC algorithm is less stable than the DMC algorithm: it requires to have a value of \\(E\_\\text{ref}\\) which is close to the fixed-node energy, and a good trial wave function. Moreover, we can't let \\(\\tau\\) become too large because the weight whether explode or vanish: we need to have a fixed value of \\(\\tau\\) (projection time). The big advantage of PDMC is that it is rather simple to implement starting from a VMC code:

1. Start with \\(W(\\mathbf{r}\_0)=1, \\tau\_0 = 0\\)
2. Evaluate the local energy at \\(\\mathbf{r}\_{n}\\)
3. Compute the contribution to the weight \\(w(\\mathbf{r}\_n) = \\exp(-\\delta t(E\_L(\\mathbf{r}\_n)-E\_\\text{ref}))\\)
4. Update \\(W(\\mathbf{r}\_{n}) = W(\\mathbf{r}\_{n-1}) \\times w(\\mathbf{r}\_n)\\)
5. Accumulate the weighted energy \\(W(\\mathbf{r}\_n) \\times E\_L(\\mathbf{r}\_n)\\), and the weight \\(W(\\mathbf{r}\_n)\\) for the normalization
6. Update \\(\\tau\_n = \\tau\_{n-1} + \\delta t\\)
7. If \\(\\tau\_{n} &gt; \\tau\_\\text{max}\\) (\\(\\tau\_\\text{max}\\) is an input parameter), the long projection time has been reached and we can start an new trajectory from the current position: reset \\(W(r\_n) = 1\\) and \\(\\tau\_n = 0\\)
8. Compute a new position \\(\\mathbf{r'} = \\mathbf{r}\_n + \\delta t\\, \\frac{\\nabla \\Psi(\\mathbf{r})}{\\Psi(\\mathbf{r})} + \\chi\\)
9. Evaluate \\(\\Psi(\\mathbf{r}')\\) and \\(\\frac{\\nabla \\Psi(\\mathbf{r'})}{\\Psi(\\mathbf{r'})}\\) at the new position
10. Compute the ratio \\(A = \\frac{T(\\mathbf{r}' \\rightarrow \\mathbf{r}\_{n}) P(\\mathbf{r}')}{T(\\mathbf{r}\_{n} \\rightarrow \\mathbf{r}') P(\\mathbf{r}\_{n})}\\)

1. Draw a uniform random number \\(v \\in \[0,1\]\\)
2. if \\(v \\le A\\), accept the move : set \\(\\mathbf{r}\_{n+1} = \\mathbf{r'}\\)
3. else, reject the move : set \\(\\mathbf{r}\_{n+1} = \\mathbf{r}\_n\\)

Some comments are needed:

- You estimate the energy as
  
  \\begin{eqnarray\*} E = \\frac{\\sum\_{k=1}^{N\_{\\rm MC}} E\_L(\\mathbf{r}\_k) W(\\mathbf{r}\_k, k\\delta t)}{\\sum\_{k=1}^{N\_{\\rm MC}} W(\\mathbf{r}\_k, k\\delta t)} \\end{eqnarray\*}
- The result will be affected by a time-step error (the finite size of \\(\\delta t\\)) due to the discretization of the integral, and one has in principle to extrapolate to the limit \\(\\delta t \\rightarrow 0\\). This amounts to fitting the energy computed for multiple values of \\(\\delta t\\).
  
  Here, you will be using a small enough time-step and you should not worry about the extrapolation.
- The accept/reject step (steps 9-12 in the algorithm) is in principle not needed for the correctness of the DMC algorithm. However, its use reduces significantly the time-step error.

</div></div><div class="outline-3" id="outline-container-org339c87b">### <span class="section-number-3">4.5</span> Hydrogen atom

<div class="outline-text-3" id="text-4-5"></div><div class="outline-4" id="outline-container-orgbbacf6d">#### <span class="section-number-4">4.5.1</span> Exercise

<div class="outline-text-4" id="text-4-5-1"><div class="exercise">Modify the Metropolis VMC program into a PDMC program. In the limit \\(\\delta t \\rightarrow 0\\), you should recover the exact energy of H for any value of \\(a\\), as long as the simulation is stable. We choose here a time step of 0.05 a.u. and a fixed projection time \\(\\tau\_{\\text{max}}\\) =100 a.u.

</div>**Python**

<div class="org-src-container">```
<pre class="src src-python"><span style="color: #a020f0;">from</span> hydrogen  <span style="color: #a020f0;">import</span> *
<span style="color: #a020f0;">from</span> qmc_stats <span style="color: #a020f0;">import</span> *

<span style="color: #a020f0;">def</span> <span style="color: #0000ff;">MonteCarlo</span>(a, nmax, dt, Eref):
    # <span style="color: #b22222;">TODO</span>

# <span style="color: #b22222;">Run simulation</span>
<span style="color: #a0522d;">a</span>     = 1.2
<span style="color: #a0522d;">nmax</span>  = 100000
<span style="color: #a0522d;">dt</span>    = 0.05
<span style="color: #a0522d;">tau</span>   = 100.
<span style="color: #a0522d;">E_ref</span> = -0.5

<span style="color: #a0522d;">X0</span> = [ MonteCarlo(a, nmax, dt, E_ref) <span style="color: #a020f0;">for</span> i <span style="color: #a020f0;">in</span> <span style="color: #483d8b;">range</span>(30)]

# <span style="color: #b22222;">Energy</span>
<span style="color: #a0522d;">X</span> = [ x <span style="color: #a020f0;">for</span> (x, _) <span style="color: #a020f0;">in</span> X0 ]
<span style="color: #a0522d;">E</span>, <span style="color: #a0522d;">deltaE</span> = ave_error(X)
<span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"E = {E} +/- {deltaE}"</span>)

# <span style="color: #b22222;">Acceptance rate</span>
<span style="color: #a0522d;">X</span> = [ x <span style="color: #a020f0;">for</span> (_, x) <span style="color: #a020f0;">in</span> X0 ]
<span style="color: #a0522d;">A</span>, <span style="color: #a0522d;">deltaA</span> = ave_error(X)
<span style="color: #a020f0;">print</span>(f<span style="color: #8b2252;">"A = {A} +/- {deltaA}"</span>)
```

</div>**Fortran**

<div class="org-src-container">```
<pre class="src src-f90"><span style="color: #a020f0;">subroutine</span> <span style="color: #0000ff;">pdmc</span>(a, dt, nmax, energy, accep, tau, E_ref)
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> a, dt, tau</span>
  <span style="color: #228b22;">integer</span>*8       , <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> nmax</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(out) ::<span style="color: #a0522d;"> energy, accep</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">intent</span>(in)  ::<span style="color: #a0522d;"> E_ref</span>

  <span style="color: #228b22;">integer</span>*8        ::<span style="color: #a0522d;"> istep</span>
  <span style="color: #228b22;">integer</span>*8        ::<span style="color: #a0522d;"> n_accep</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> sq_dt, chi(3)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> psi_old, psi_new</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> r_old(3), r_new(3)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> d_old(3), d_new(3)</span>

  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">external</span> ::<span style="color: #a0522d;"> e_loc, psi</span>

  ! <span style="color: #b22222;">TODO</span>

<span style="color: #a020f0;">end subroutine</span> <span style="color: #0000ff;">pdmc</span>

<span style="color: #a020f0;">program</span> <span style="color: #0000ff;">qmc</span>
  <span style="color: #a020f0;">implicit</span> <span style="color: #228b22;">none</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> a     = 1.2d0</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> dt    = 0.05d0</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> E_ref = -0.5d0</span>
  <span style="color: #228b22;">double precision</span>, <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> tau   = 100.d0</span>
  <span style="color: #228b22;">integer</span>*8       , <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> nmax  = 100000</span>
  <span style="color: #228b22;">integer</span>         , <span style="color: #a020f0;">parameter</span> ::<span style="color: #a0522d;"> nruns = 30</span>

  <span style="color: #228b22;">integer</span>          ::<span style="color: #a0522d;"> irun</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> X(nruns), accep(nruns)</span>
  <span style="color: #228b22;">double precision</span> ::<span style="color: #a0522d;"> ave, err</span>

  <span style="color: #a020f0;">do</span> irun=1,nruns
     <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">pdmc</span>(a, dt, nmax, X(irun), accep(irun), tau, E_ref)
  <span style="color: #a020f0;">enddo</span>

  <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">ave_error</span>(X,nruns,ave,err)
  <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'E = '</span>, ave, <span style="color: #8b2252;">'+/-'</span>, err

  <span style="color: #a020f0;">call</span> <span style="color: #0000ff;">ave_error</span>(accep,nruns,ave,err)
  <span style="color: #a020f0;">print</span> *, <span style="color: #8b2252;">'A = '</span>, ave, <span style="color: #8b2252;">'+/-'</span>, err

<span style="color: #a020f0;">end program</span> <span style="color: #0000ff;">qmc</span>
```

</div><div class="org-src-container">```
<pre class="src src-sh">gfortran hydrogen.f90 qmc_stats.f90 pdmc.f90 -o pdmc
./pdmc
```

</div></div></div></div></div><div class="outline-2" id="outline-container-org9d710e3"><span class="section-number-2">5</span> Project
-----------------------------------------------

<div class="outline-text-2" id="text-5">Change your PDMC code for one of the following:

- the Helium atom, or
- the H<sub>2</sub> molecule at \\(R\\) =1.401 bohr.

And compute the ground state energy.

</div></div><div class="outline-2" id="outline-container-org38ba401"><span class="section-number-2">6</span> Acknowledgments
-------------------------------------------------------

<div class="outline-text-2" id="text-6"><div class="figure">![euflag.jpg](https://trex-coe.eu/sites/default/files/inline-images/euflag.jpg)

</div>[TREX](https://trex-coe.eu) : Targeting Real Chemical Accuracy at the Exascale project has received funding from the European Union’s Horizon 2020 - Research and Innovation program - under grant agreement no. 952165. The content of this document does not represent the opinion of the European Union, and the European Union is not responsible for any use that might be made of such content.

</div></div></div><div class="status" id="postamble">Author: Anthony Scemama, Claudia Filippi

Created: 2022-06-08 wo 13:03

[Validate](http://validator.w3.org/check?uri=referer)

</div>