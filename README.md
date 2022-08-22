# Template for Writing an eBook

- Has book template(asciidoc) for creating html, pdf, epub/mobi.
- Uses [asciidoctor](http://asciidoctor.org) to make the book.
- See `master.adoc` for the build list

## Edit

```bash
git clone git://github.com/rochacbruno/asciidoctor-book-template.git
cd asciidoctor-book-template
bundle
rake
```

## Generate the book

```bash
rake ascii
```

## Auto run on every file change

```bash
find . -name '*.adoc' | entr docker run --rm -v $PWD:/documents/ asciidoctor/docker-asciidoctor asciidoctor-pdf -vwt -o output/mybook.pdf master.adoc 
```

## Learn more

- [Quick guide on syntaxes](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/)

![Sample](./sample.png)
