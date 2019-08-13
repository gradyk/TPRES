TPRES is an XML schema derived from the Text Encoding Initiative schema for documents. The TPRES schema and the associated XML tags are designed for the unique and not-so-unique requirements of encoding texts associated with tribunal proceedings and resolutions. It leverages the rich history of the TEI encoding system and adds to it so that those interested in tribunal proceedings and resolutions have a tag set that meets their specific needs.

### What is TPRES XML Encoding?

XML is an abbreviation for eXtensible Markup Language. It is not a Turing complete software language. But, it is a widely-used language for encoding documents. It allows the user to place tags around text so that a computer (or human) can place meaning to the text. The following code snippet (which uses TPRES tags) should help you understand what XML can do:

    <senText>
      <segText>This is a segment, </segText>
      <quoteText rend="dq">followed by a quote,</quoteText>
      <segText> with a concluding segment.</segText>
    </senText>

It is easy for both the computer and a human to interpret this code block. The &lt;senText&gt; element wraps an entire sentence. Within that element, there are three child elements. The first, &lt;segText&gt; wraps a segment. The second, &lt;quoteText&gt; wraps a quote, and the final, another &lt;segText&gt;, wraps another segment. Finally, the rend attribute in the &lt;quoteText&gt; element tells us (and the computer) that double quotes should be used before and after the quote.

Using combinations of the elements, attributes, and datatypes available in TPRES, an encoder can put structure and meaning to the documents that make up a tribunal proceeding and resolution. For example, the encoder could code an opinion by the Supreme Court of the United States (including providing information on majority, dissenting, concurring, and joining opinions), the briefs submitted in the case, and the transcript of the oral argument. The encoder could do the same thing for all cases decided in a term, or all cases in which a specific justice wrote the majority opinion. Using XSLT (eXtensible Stylesheet Language Transformations), the encoder could extract various features from the texts and then apply content analysis tools to the text. This is one of many applications.

### Using TPRES

To use TPRES you need only one file, the TPRES rnc schema. You can get this file from the TPRES repository. It is a RELAX-NG compact syntax schema specifically for TPRES. You should use this schema to validate your TPRES encoded XML documents. Of course, there is a bit more to TPRES than simply having the schema. TPRES has hundreds of elements, attributes, datatypes, models, and macros that make up the system. Trying to guess which one to use where and how they interrelate from the schema alone would take a long time. Instead, you can learn about each of these TPRES parts using the TPRES Schema Guide. 

### The TPRES Guidelines

While the TPRES Schema Guide gives you details about each TPRES part, it can be difficult to see how those parts fit together. This is where the TPRES Guidelines come in. The Guidelines provide a comprehensive overview of the system, how the parts fit together, how you can use them, and strategic ways you can make your texts easier to analyze. As of August 2019, the Guidelines are still being developed. When they are finished, you will find them in the GitHub TPRES repository.

### TPRES Continuing Development

TPRES Version 1.0.0 was built using the minimum viable product philosophy. As such, it leaves enormous room for further development. Some of the development will come from users. **If you see problems or have suggestions, please submit a ____________ on the TPRES repository.** 

Meanwhile, development of TPRES will continue. Plans call for extending TPRES to administrative tribunals, foreign tribunals, and capturing more tribunal texts. TPRES will be integrated with Akoma Ntoso for legislative materials. TPRES will be extended through XInclude so that users can develop multiple coding ______ for texts. These are just some of the plans for TPRES.

### Contact

If you would like more information about TPRES, contact me at gradyken@msu.edu.

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

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.
