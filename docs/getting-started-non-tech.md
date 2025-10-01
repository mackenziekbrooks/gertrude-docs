# Getting Started for Non-Tech People

## Digital Editions 

A digital edition is a particular version of a text published online. Unlike today, when an idea can go from our head to the screens of millions in half a second, texts of the past passed through the hands of multiple people and physical formats. A poet may have drafted several versions of their poem before typing the final version. A politician may have had their speech edited before it reached the newspaper. There are countless reasons that the myriads of people - printers, publishers, typesetters, family members - may have consciously or unconsciously changed words at some point between the author's hand and the final material form. 

Scholars who study these changes, their contexts, and their implications are performing **textual scholarship**. Scholars use their training, judgment, and the guidance of particular editorial theories to transcribe, edit, enrich, and ultimately create an edition. Some editions may make arguments for a "authoritative" version of a text, while others are more interested in uncovering texts that may not be widely accessible. 

In the past, an edition would have been confined to a single or set of books, but with the affordances of software, an edition can be reimagined. For example: footnotes can be embedded directly as pop-up windows or a button can toggle between the uncorrected and corrected versions of a text. Computational textual analysis can be performed on large amounts of a text (a corpus). Scholars are not limited in the amount of contextual material they can include. 

For more on definitions of scholarly editions, see Patrick Sahle's chapter, "What is a Scholarly Digital Edition?" in [Digital Scholarly Editing: Theories and Practices](https://www.jstor.org/stable/j.ctt1fzhh6v) available open access on JSTOR.


## Examples

There are countless examples of digital edition projects. The ones below were chosen to illustrate particular advantges of digital editions. 

* [The Shelley-Godwin Archive](http://shelleygodwinarchive.org/) - hosts a version of [Frankenstein](http://shelleygodwinarchive.org/sc/oxford/frankenstein/volume/i/#/p1/mode/std) with a toggle to show the editorial interventions of Percy Shelley.
* [Huon d'Auvergne Digital Archive](https://www.huondauvergne.org/) - the [Turin manuscript](https://www.huondauvergne.org/t-edition/t-edition-001r) was burned in a fire, but the text has been reconstructed and restored from a 19th century transcription.  
* [Furnace and Fugue](https://furnaceandfugue.org/) - this [edition of *Atalanta fugiens*](https://furnaceandfugue.org/atalanta-fugiens/emblem01.html) uses the Music Encoding Initiative and allows users to hear the music alongside the manuscript image and the transcription.


## Publishing

The majority of digital editions use the guidelines of the [Text Encoding Initiative](https://tei-c.org/) (TEI) to encode their texts in an XML-based file format. The TEI is both a consortium of people and institutions as well as a technical standard. While it is possible to paste some text onto a website and call it an edition, the process of taking a text from print to digital is ultimately an interpretive act. The TEI guidelines and the TEI-XML format exist to 1) create a semantically-meaningful and machine-readable format to your text and 2) document and enrich the editorial decisions and process. 

Practically, this means that texts are put into a text file and XML tags (also called elements) surround the text to add structure and other information. This is what is known as **semantic markup**. The tags tell the computer that a piece of text exists as a separate chunk of content and what the role or function of that content is in relation to the whole text.

TEXT EDITORS!!!! 

Here's the basic template: 

```
<TEI xmlns="http://www.tei-c.org/ns/1.0">
 <teiHeader>
<!-- ... -->
 </teiHeader>
 <text>
  <front>
<!-- front matter of copy text, if any, goes here -->
  </front>
  <body>
<!-- body of copy text goes here -->
  </body>
  <back>
<!-- back matter of copy text, if any, goes here -->
  </back>
 </text>
</TEI>
```

You can learn more about TEI from their [website](https://tei-c.org/support/learn/) and in other parts of this documentation. 

Once the texts have been encoded, they need to be published to the web. However, in what can feel like a backward step, the TEI-XML files need to be transformed into another format so they can be displayed in modern browsers. There are many options for how to do this and your choice will depends on your resources and the goals of the project. Gertrude is just one possible route, others include [TEI Publisher](https://teipublisher.com/) built on the XML-based database eXistDB or [XSLT](https://www.w3schools.com/xml/xsl_intro.asp) stylesheets that convert your TEI to HTML. Gertrude uses the JavaScript library [CETEIcean](https://github.com/TEIC/CETEIcean) to convert the TEI to custom HTML elements so they can customized using CSS and JavaScript.


## Web development 

Some of the main concepts and issues to be aware of: 

### Servers
Websites are hosted on **servers**, which are essentially just files and folders on someone else's computer that is connected to the internet in a particular way. Often, projects are developed locally on a single computer before being published or **deployed** to a server. A staging server or location might also be helpful for testing. 

### HTML, CSS, and JavaScript
The core languages used by websites are HTML, CSS, and JavaScript. HTML looks similar to TEI-XML and creates the structure of a page. CSS is the list of styles that tells the browser how to display the HTML (think colors, fonts, margins). JavaScript is a programming language that controls dynamic interactions that the user might have within the browser and with the website (a pop-up window or a button). 

- Basic websites consist of just HTML, CSS, and JavaScript. These might also be called "flat" or "static." You can upload these files to a server to create your website, then never have to touch them again and the site will be relatively stable. In contrast, today most websites are run by web applications that include databases (i.e. mySQL), programming languages (i.e. PHP), and more complex server software (i.e. Apache). Web applications require more administration by IT professionals to keep them secure, up to date, and accessible. Web applications can also host more complex and custom projects and data. Websites with individual user accounts or dashboards are built with web applications. 

- Static websites have reemerged in popularity in recent years because they are more sustainable and secure. They also fall under the label of **[minimal computing](https://go-dh.github.io/mincomp/about/)**. However, they still require technical know-how to execute. There are numerous options for creating static sites, including just writing HTML by hand. Gertude uses the static site generator [Jekyll](https://jekyllrb.com/), but there are other options like [Hugo](https://gohugo.io/), [NextJS](https://nextjs.org/), and [Gatsby](https://www.gatsbyjs.com/). Jekyll is now an older platform, not necessarily as sexy as other options, but it has proved reliable over time. 

- To create a website with Jekyll, you will need to install and run the Ruby programming language on your computer. If you aren't much of a tech person, this part is a little scary and annoying. It's a task best suited to the tech person with a Mac who is comfortable using the command line. Jekyll consists of some Ruby code that will take your content and your templates and generate a static website. Fortunately, once the site is created, there are easier options for editing and adding content.

- Many people who write code or other text-based projects use version control software called **git** and the website component known as **GitHub**. These two components allow teams to collaborate on code or text-based projects without having to send files to one other. Changes are tracked and can be reverted. GitHub also provides a way to publish websites with a service called GitHub Pages. It uses Jekyll by default, but you can also deploy other types of websites. Your default URL will be `https://yourusername.github.io`. The Gertrude project will assume that project team members will make edits to content via the GitHub website. 

- You might want a specific domain or URL for your project. A domain is the address of a project and can point to any server. You can purchase a domain on a site like [Hover.com](https://www.hover.com/). If you want a URL that includes the `.edu` of your institution, you will need to work with your IT department and possibly abide by additional policies. Domains are possible to change or redirect, but it can be annoying and messy, so best to think through this decision early on. 

- Web accessibility. 


## Institutional resources

- If you're a non-tech person, you will probably want to enlist the assistant of an IT or library colleague who can collaborate on this project. You should ensure that this type of work is within the bounds of their job description. 

- If you want your institution to host the project from a technical standpoint, you should pursue a memorandum of understanding about resources and length of time of support. IT departments can be hesitant to host one-off, custom projects. The [Socio-Technical Sustainability Roadmap](https://sites.haa.pitt.edu/sustainabilityroadmap/) is a great resource for thinking through the lifespan of your project. 

- If you want your project URL to include a `.edu` domain, you will need to secure that with your IT department. You may have to be involved in updated a security certificate annually. 

- You should consider how much storage your project will require. Digital edition projects tend to be lightweight, but there may be additional media components that will need to be hosted somewhere. 

- If digitized images of your text are to be included, where will these images be hosted? What is the copyright situation? Gertrude is designed to work with images that have been hosted on a [IIIF](https://iiif.io/)-compliant image server. Many digital repositories meet this standard but not all. Self-hosting images is a possibility as well.

## Students

There are numerous ways to involve students in digital edition projects. Here are a few scenarios and recommendations: 

- Students can transcribe, translate, edit, and encode text. Particularly after students have been oriented to a text through a class or research assistance experience, students are well-equipped to work closely with a text. 

- Students can prototype and design the website. They can research other digital editions, make a list of desired features, create a [wireframe](https://wireframe.cc/) or mockup of the website, and design logos or other branding materials. This is an area where students can bring expertise and grow in their web design or user experience skills. 

- Students with more of a tech or computer science background can contribute to setup and development of the platform. Note: not all computer science programs teach the front-end web development skills required for Gertrude. Students may have picked up these skills on their own and be amazing developers, but it can't be assumed that a CS major brings the necessary training. Students should be required to thoroughly document their code and any technical decisions so that the work can be picked up by someone else in the future. Students should not be the sole owners of logins or admin rights. 



