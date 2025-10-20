## Welcome to the GitHub Pages site for Jornada Informatics and Data Science

You can use the [editor on GitHub](https://github.com/jornada-im/jornada-im.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

## Jornada LTER IM documentation pages

/docs contains documentation of the IM system

/standards contains data and metadata standards used for publishing JRN data

/reports contains periodic reports from the IM system

not sure yet where these pages will end up.

## standards

A directory of documents about best practices and standards for metadata creation at Jornada Basin LTER.

Please refer to these as you are packaging data and creating EML documents for Jornada Basin research products.

**Edit as you see fit, but please track your changes when possible and Greg will try to sync with the GitHub version of this repository.**

### Building the standards document

    pandoc JRN_metadata_standards.md --toc --metadata date="$(date +%Y-%m-%d%n)" -o ../JRN_metadata_standards.docx

### Building annual reports

    pandoc JRN_IM_annual_report_2020.md --toc --metadata date="$(date +%Y-%m-%d%n)" -o ../JRN_IM_annual_report_2020.docx
