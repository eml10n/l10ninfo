---
title: A General Guide to Localization
alias:
- general
- generalguide
- guide
- quickguide
---

## Translation vs localization vs internationalization vs globalization

- [Introduction to globalization](https://helpx.adobe.com/coldfusion/developing-applications/developing-cfml-applications/developing-globalized-applications/introduction-to-globalization.html) – Adobe
- [Localization Strategy: What Is I18n? A Simple Definition of Internationalization](https://phrase.com/blog/posts/i18n-a-simple-definition/) – Phrase
- [Localization VS Globalization VS Internationalization VS Translation](https://www.milestoneloc.com/localization-vs-globalization-vs-internationalization-vs-translation/) – Kristina Temelkova, Milestone Localization
- [Software Translation, Localization, Internationalization, Globalization: What’s The Difference?](https://www.at-it-translator.com/software-translation-localization-internationalization-globalization-whats-the-difference/) – Anthony Teixeira

## Dos and don'ts

#### Do familiarise yourself with the article or application

Before you start translating, you should familiarise yourself with the product. If you are translating an article or a piece of writing, read it first. If you are translating an application or a piece of software, try it first. Consider who might be reading the article or using the application, how they are likely to be reading or using it, and for what purpose. This will help you form a better idea of the style and tone that you should use in your translation.

#### Do refer to the style guide and glossary

A well-maintained localization project would have a robust style guide and glossary to ensure consistency and accuracy of translations across different target languages. If they are available, you should make full use of these resources when translating.

#### Do look up similar translations

You can use the search function in the continuous translation tool that you are using to look up similar translations in the same target language. If you are familiar with languages that belong to the same genus, you can also look up similar translations across different languages. Doing this will help ensure consistency and accuracy when translating.

#### Do give feedback and ask questions

Use the commenting function to give feedback and ask questions. This helps the localization project managers and other localizers improve the translation. For example, you give feedback to other localizers on how to improve the grammar, style, tone and terminology used in the translation or ask questions to the project managers to get more context and understand the where a particular string might appear in the user interface. 

#### Don't translate if unsure

If you are not sure about the context of a particular string, where it might apear in the user interface, or how it should be formatted, do not translate it. You may skip the string or leave a question in the comments for the project manager to respond.

#### Don't rely on machine translation

While tools like Google Translate and Microsoft Translator are getting better with large language model, they are not always reliable because of the imperfect feedback loop. You may use them to give you suggestions on how to translate a string but they should never be accepted completely without human checking and editing. Relying on machine translation will make the localization review and testing process more difficult and time-consuming as more work needs to be done to ensure consistency and accuracy. 

#### Don't translate variables or placeholders

You may find variables or placeholders in the source strings. Instead of translating these variables or placeholders, you need to keep them in the translated strings where they should appear keeping in mind consistent grammar and style. Depending on how the developers internationalize the application or software, the variables or placeholders are typically enclosed in brackets, braces, chevrons, percents, underscores, or any combination of these symbols:

    [something]	[[something]]	{something}	{{something}}

    <something>	%something%	<%something%>	__something__

Sometimes, variables and placeholders may appear with a single per cent sign:

	Integer variable	%d	1%d	2%d	3%d

	Character variable	%c	1c	2%c	3%c

	Float variable		%f	1%f	2%f	3%f

	Double variable	%lf	1%lf	2%lf	3%lf

	String variable	%s	1%s	2%s	3%s

	Octa variable		%o	1%o	2%o	3%o

	Hexadecimal variable	%x	1%x	2%x	3%x

Another way variables or placeholders typically appear in strings is with a single leading dollar sign:

	$something1     $something2     $something3

You should note translate these variables or placeholders.

#### Don't translate everything in a front matter

The [front matter](https://www.npmjs.com/package/front-matter) contains metadata or parameters for a web page. It is typically written as a set of keys and values in TOML, YML/YAML, or JSON. For example:

	---
	categories:
	- Globalization
	- Internationalization
	- Localization
	- Translation
	date: "2012-04-06"
	description: An example of front matter written in YAML/YML.
	slug: yaml-yml-front-matter-example
	tags:
	- General Guide
	- Translation Guide
	title: YAML/YML example
	---

	+++
	categories = ['Globalization', 'Internationalization', 'Localization', 'Translation']
	date = '2012-04-06'
	description = 'An example of front matter written in TOML.'
	slug = 'toml-front-matter-example'
	tags = ['General Guide', 'Translation Guide']
	title = 'TOML example'
	+++

	{
		"categories": [
			"Globalization",
			"Internationalization",
			"Localization",
			"Translation"
		],
		"date": "2012-04-06",
		"description": "An example of front matter written in JSON.",
		"slug": "json-front-matter-example",
		"tags": [
			"General Guide",
			"Translation Guide"
		],
		"title": "JSON example"
	}

Do not translate the keys and only translate the values that should appear in the target language. In the above example, only the values of `categories`, `description`, `tags`, and `title` should be translated and everything else should be kept the same. Do not translate boolean values `true` or `false`. Make sure you keep the translated front matter in the same format. If you are unsure, skip strings like this or ask the project managers to give more guidance.

#### Don't translate everything in HTML elements

HTML elements help internet browsers render a webpage. A link element is usually written with HTML tag `<a>`:

	<a href="https://engagemedia.org/" title="EngageMedia">This is a link that you can click</a>

An image has `<img>` tag:

	<img src="https://assets.engagemedia.org/logomark-white.svg" alt="EngageMedia Logomark in White">

Watch out for semantic elements that have HTML tags in English:

	<header>
		...
	</header>

	<article>
		Some content of the article
		<br>
		Another line of this content
	</article>

	<section>
		<p id="para1">Some content for this section</p>
		<p id="para2">Another paragraph in the section</p>
	</section>

	<aside>
		<ul>
			<li>This unordered list</li>
			<li>probably appears</li>
			<li>in a sidebar</li>
		</ul>
	</aside>

	<footer>
		...
	</footer>

You should not translate an HTML tag and only do the text inside the HTML element that should appear in the target language. Some HTML tags contain attributes like `title`, `alt`, `description`, and others. You should only translate the values of these attributes if it makes sense. Do not translate values to `id`, `class`, or other similar attributes. If you are unsure, skip strings like this or ask the project managers to provide guidance.

#### Don't start translating without understanding a product

Localization is not just about transforming text from one language into another without changing its meaning. Beyond that, the purpose of localization is to make the product available and accessible in other languages taking into account the appropriate contexts and experiences of the end-user using the product. This requires you, as a localizer, to understand how the product works from the end-user perspective.

## See also

- [Translation and Review Guidelines](https://wiki.localizationlab.org/index.php/Translation_and_Review_Guidelines) – Localization Lab
- [Dos and Don'ts in Content Translation](https://blog.pangeanic.com/dos-and-donts-in-content-translation) – Aurora Ramírez, Pangeanic
