# pdf2ebook

Documentazione tools per passaggio da pdf a ebook

## versione rapida:

1. ocr da pdf a txt:
```
ocrmypdf --remove-background --deskew --clean --clean-final -l ita --sidecar out.txt in.pdf out.pdf
```

2. proofreading txt, aggiustamenti markdown
```
% My Book
% Sam Smith

This is my book!

# Chapter One

Chapter one is over.

# Chapter Two
```

3. da markdown a epub

```
pandoc in.md -o out.epub
```

## OCR

https://pypi.org/project/ocrmypdf/

uso:
```
 ocrmypdf in.pdf out.pdf
```

ocrmypdf main task is the creation of an mixed-mode (image, text) PDF.

Per epub usare opzione `--sidecar file.txt` per creare un file di testo con il testo rilevato da ocr.
Risultati decenti con:

```
ocrmypdf --remove-background --deskew --clean --clean-final -l ita --sidecar out.txt in.pdf out.pdf
```

## conversione da md a epub

https://pandoc.org/epub.html

```
pandoc in.md -o out.epub
```


## conversione da pdf a epub

via calibre: https://ostechnix.com/convert-pdf-to-epub-in-linux/

uso:
```
ebook-convert file.pdf file.epub --enable-heuristics
```

## modificare file epub

vigil: https://itsfoss.com/sigile-epub-editor/

## programmi per scrittura 

https://itsfoss.com/open-source-tools-writers/
