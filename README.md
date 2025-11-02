# jornada-im.github.io

This is the website repository for [jornada-im.github.io](https://jornada-im.github.io), the home site of the data science and information management team for Jornada programs, including the [Jornada Basin LTER](https://lter.jornada.nmsu.edu) (JRN) and USDA-ARS [Jornada Experimental Range](https://jornada.nmsu.edu) (JER) programs. Most content here is documentation for researchers, data managers, and staff who are working with data collected or managed by these programs. 

The website is created using the [Quarto](https://quarto.org) documentation publishing system and served by [GitHub Pages](https://docs.github.com/en/pages). The `main` branch of this repository contains all source files for the web pages, which Quarto renders into HTML files that are served from the `gh-pages` branch. These HTML files are what you see when you visit [the site](https://jornada-im.github.io) with your web browser. Source files are written in the Quarto variant of [Markdown](https://www.markdownguide.org/getting-started/) - a simple, plain-text markup language. The website and the documentation it contains are intended as a community-supported resource, and if you are so-inclined we welcome your contributions. For more on this, see "Contributing" below.

## Site and repository layout

 The [jornada-im.github.io](https://jornada-im.github.io) site has a landing page, collections of documentation for researchers and data managers, a listing of posts (like a blog), and a few more standalone pages. The Quarto build system also provides a top menu bar, side navigation, and search indexing to tie the website together and make pages discoverable. Content for all web pages is created in source files written in Quarto-flavored markdown stored throughout the repository file system. These files have the `.qmd` file extension. This repository is structured as shown below:

```
jornada-im.github.io/
|-- archive/                    # Archived files, forms, etc.
|-- docs/                       # Documentation files
|  |-- im/                      #   Information manager documents
|  |-- researcher/              #   Researcher documents
│  ` refs-and-links.qmd         #   Collected external resources
|-- img/                        # Images for embedding in documents
|-- posts/                      # Blog posts ("Updates" on website)
|-- proposals-and-reports/      # Data management plans and periodic reports
|-- templates/                  # Forms, metadata templates, etc.
|-- index.qmd                   # The website landing page
|-- _quarto.yml                 # Quarto structure
`-- README.md                   # This file
```

The `index.qmd` file is the source for the HTML index, or landing page, of the website. The `_quarto.yml` file is a YAML file that defines how the website is structured, the navigation system, and the rendering options that Quarto uses to build the HTML and other files. The IM (`docs/im/`) and researcher (`docs/researcher/`) directories contain numerous subdirectories and source files, but some guideposts are provided in the `overview.qmd` pages in each directory.

## Contributing

Jornada researchers, staff, and data managers are welcome to contribute to this documentation. Contributions could include fixing typos and errors, suggesting new and improved text, or just pointing out documentation that should exist but doesn't. There are a few ways you can do this:

1. The easiest method is to file an issue in [this repository](https://github.com/jornada-im/jornada-im.github.io). Go to the Issues tab at the top of the repository page and then select **New issue**. Provide a thorough description of your issue and suggested changes. You can even put suggested text into your issue. Once you submit it, the IM team will review and make changes.
2. Use the "fork and pull request" method by forking this repository to your own GitHub profile using the **Fork** button at the top right of the page. Then make your changes and submit a pull request from your fork. Someone on the IM team will review and merge them in. You can read more about GitHub [forks](https://docs.github.com/articles/fork-a-repo) and [pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) in the GitHub documentation.
3. If you would like to contribute directly to this repository without using the fork and pull request method, request to join th Jornada IM team on GitHub so that you can contribute changes directly. We still recommend creating a branch first, instead of committing directly to `main`.

Note that for contribution methods 2 and 3, you can make changes directly in the GitHub web interface using the **Edit** button at the top right of any page (it has a pencil icon on it), or you can clone the repository locally, make changes using your favorite editor, and push them back to GitHub. 

### Markdown

When you create new documentation you should use [Markdown](https://www.markdownguide.org/getting-started/) to write the text. Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes many text formatting and styling conventions for publishing documents.

```markdown
This is a Markdown syntax-highlighted code block

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

The [Quarto](https://quarto.org) publishing system we use has its own additions to standard Markdown and there is quite a bit you can do with the Quarto Markdown variant. Consult the [Quarto authoring guide](https://quarto.org/docs/guide/) for more on writing documentation pages.

## Building and deployment

Whenever a new Git commit is pushed to the `main` branch of this repository, a GitHub Action (see it in `.github/workflows/`) will run to rebuild the website with any new content changes in the source files. This action takes all content in the `main` branch and uses Quarto to render HTML and other files, then commits the result to the `gh-pages` branch. It is these files that are served to visitors at <https://jornada-im.github.io>.

Some of these documents can be built independently with [pandoc](https://pandoc.org/), and to some extent this is what Quarto uses to render the documents under the hood. For example, here is how you can render MS Word files for the JRN Metadata Standards document

    pandoc JRN_metadata_standards.qmd --toc --metadata date="$(date +%Y-%m-%d%n)" -o ../JRN_metadata_standards.docx

or an annual report.

    pandoc JRN_IM_annual_report_2020.qmd --toc --metadata date="$(date +%Y-%m-%d%n)" -o ../JRN_IM_annual_report_2020.docx

## Contact us

If you have questions or concerns about the website or its content, or you'd like to know more about contributing, please contact the Jornada IM team at <jornada.data@nmsu.edu>.