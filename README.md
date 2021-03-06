
BrGram - a lexical-functional grammar fragment of Brazilian Portuguese

Author: Leonel F. de Alencar leonel.de.alencar@ufc.br
Copyright (C) 2013-2018 Leonel F. de Alencar

License: Apache License Version 2.0, January 2004. For more
information, visit https://www.apache.org/licenses/LICENSE-2.0


BrGramm is a computational grammar fragment of Brazilian Portuguese in
the LFG formalism. It is implemented in the Xerox Linguistic
Environment - XLE. To compile a parser from the grammar and parse
sentences in Portuguese, you first need XLE:

http://www2.parc.com/isl/groups/nltt/xle/

You also need XFST to compile the source files of the basic tokenizer
and the morphological analizer into finite-state transducers:

http://web.stanford.edu/~laurik/fsmbook/home.html

You can download the source files of both transducers from here:

https://github.com/LFG-PTBR/BrGram/fst

The finite-state transducers must be compiled with XFST in the
operating system where you are running XLE. Edit the respective path
in the morphology.lfg file to point to the location of each transducer
file in your system.

Once you have XLE installed and the transducers compiled, you can
compile a parser from the grammar by executing the following command
on the XLE shell (I assume your working directory is the grammar
folder):

create-parser config.lfg

To apply the parser on individual sentences from the testfile.lfg in the test folder, run:

parse-testfile testfile.lfg 1

where 1 refers to first sentence in the testfile.

For more details on the XLE textual and graphical user interfaces, see
the documentation:

http://www2.parc.com/isl/groups/nltt/xle/doc/xle.html#SEC2

BrGramm is a significantly improved version of the grammar fragment
described in the following papers:

- Alencar, Leonel F. de. BrGram: uma gramática computacional de um
  fragmento do português brasileiro no formalismo da LFG. In:
  BRAZILIAN SYMPOSIUM IN INFORMATION AND HUMAN LANGUAGE TECHNOLOGY –
  STIL, 2013, Fortaleza. BRAZILIAN SYMPOSIUM IN INFORMATION AND HUMAN
  LANGUAGE TECHNOLOGY – STIL. Fortaleza: Sociedade Brasileira de
  Computação, 2013. p.183 -
  188. http://www.aclweb.org/anthology/W13-4823

- Alencar, Leonel F. de. A passiva em português como construção
  predicativa adjetival: evidência morfológica e implementação
  computacional em LFG/XLE. Estudos da Língua(gem) (Online), v. 13,
  p. 35-57, 2015. http://www.repositorio.ufc.br/handle/riufc/19740

- BrGram basically has the same basically as FrGramm, an LFG/XLE
  grammr fragment of French implemented by the author, available at
  https://github.com/lfg-french-grammar. FrGramm is described in
  detail in the following paper:

- Alencar, Leonel Figueiredo de. A computational implementation of
  periphrastic verb constructions in French. Alfa, São Paulo, v. 61,
  n. 2, p. 437-466, 2017.

Previous versions are described in the following introduction to LFG
and grammar development in XLE:

- Schwarze, Christoph & Alencar, Leonel F. de. Lexikalisch-funktionale
  Grammatik: Eine Einführung am Beispiel des Französischen mit
  computerlinguistischer Implementierung [Lexical-Functional Grammar:
  A French-based Introduction with Computational
  Implementation]. Tübingen: Stauffenburg, 2016. X, 271
  pp. Stauffenburg Einführungen, 30. ISBN 978-3-95809-411-6.

For bug reports, comments, and suggestions, please issue the issues
from GitHub repository.
