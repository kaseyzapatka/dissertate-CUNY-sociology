# Dissertate-CUNY-sociology

R markdown (w/ Latex) Template for writing a dissertation at CUNY

This follows the CUNY formatting guide for dissertations and theses ([CUNY format guide](https://libguides.gc.cuny.edu/dissertations/format)). This repo is based on the work of Nicholaus P. Brosowsky[https://github.com/nbrosowsky/dissertate-CUNY], who built on the work of others: 

 - [DissertateUSU](https://github.com/TysonStanley/dissertateUSU) 
 - [Dissertate](https://github.com/suchow/dissertate)) 
 - CUNY latex template created by George Leibman ([GC latex thesis](https://www.gc.cuny.edu/Page-Elements/Academics-Research-Centers-Initiatives/Doctoral-Programs/Mathematics/Course-Notes/LaTeX-template-for-GC-theses))

This repo contains all necessary code for knitting a dissertation in R Markdown. Specifically, it contain example code for chapters, figures, tables, appendices. The logic of editing is as follows: 

  - The `manuscritp.Rmd` file is the master file that pull together everything else. Write the dedication and acknowledgements directly in this file but call each of the other chapters and appendix separately using the `child` call in the R chunks in the `manuscript.Rmd` file. The chapters are located in the "chapters" folder. Edit each chapter there and they will be called into the manuscript file to `knit` the full dissertation manuscript. Just knit the `manuscript.Rmd` file to assemble the dissertation. 
  - `DissertateCUNY.cls` is the file that provides the bulk of the formatting for the dissertation. Any major changes you might want to make if adapting to another university would likely be made in here. For example, I adjusted the formatting in the Nick's template so that all the text was fully justified (using the `\justifying` Latex command) instead of having it justified right (using the `\RaggedRight` Latex command under "%Text Layout").
  - `ASA_format.csl` is the file that formats the dissertation according the American Sociological Association guidelines. If you want to adapt to another format, you will need to edit this file. You might be able easily Google a template online, which is what I did. 
   - `referencs.bib` is an export in .bib format of all dissertation citations. I used Zotero for this. 
  - All figures and tables used in the dissertation are located in the respective folders and called in R chunks in each of the respective chapters. I used the `here` package to call them, which I found to be easiest. 
