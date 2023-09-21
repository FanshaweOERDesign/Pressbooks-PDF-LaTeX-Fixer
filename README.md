# Pressbooks-PDF-LaTeX-Fixer
Resolves some issues encountered when exporting LaTeX with colour codes from Pressbooks to print PDF format. Specifically, the Pressbooks PDF renderer requires LaTeX colours to be specified using their semantic labels rather than RGB codes, and also has very specific bracketting requirements as well -- for example
    [latex]{\color{red}{\text{red text}}}[/latex] 
will render, but
    [latex]{\color[rgb]{1.0, 0.0, 0.0}\text{red text}}[/latex]
will not. 

The live version can be found at 
## NOTE 
- When using this utility with especially complex LaTeX expressions (arrays nested within arrays, for example) the placement of curly braces in the results may need to be adjusted.
- This utility will not fix ALL of the issues that might interfere with LaTeX rendering properly in PDF exports, and applies to a limited palette of colours only. Other possible causes of problems include leading or training spaces within \text or \mbox elements, or unnecessary spaces within the the LaTeX expression more generally.
- Ensure that the LaTeX expression to be reformatted is enclosed with [latex] and [/latex] tags
