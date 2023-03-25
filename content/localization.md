---
title: Localization
---

## Dos and Don'ts

#### Do familiarise yourself with the article or application

Before you start translating, you should familiarise yourself with the product. If you are translating an article or a piece of writing, read it first. If you are translating an application or a piece of software, try it first. Consider who might be reading the article or using the application and why they are doing it. This will help you form a better idea of the style and tone that you should use in your translation.

#### Do refer to the style guide and glossary

A well-maintained localization project would have a robust style guide and glossary to ensure consistency and accuracy of translations across different target languages. You should refer to these resources when translating.

#### Do look up similar translations

You can use the search function to look up similar translations in the same target language. If you are familiar with languages that belong to the same genus, you can also look up similar translations across different languages. Doing this will help ensure consistency and accuracy when translating.

#### Do give feedback and ask questions

Use the commenting function to give feedback and ask questions. This helps the localization project managers and other localizers improve the translation. For example, you give feedback on how to improve the grammar, style, tone and terminology of a string or ask questions to get more context and understand the application of a particular string. 

#### Don't rely on machine translation

While tools like Google Translate and Microsoft Translator are getting better, they are not always reliable. You may use them to give you suggestions on how to translate a string but they should never be used without human editing. Relying on machine translation will make the reviewing process more difficult and time-consuming as more work needs to be done to ensure consistency in grammar, style, tone, and terminology. 

#### Don't translate variables or placeholders

You may find variables or placeholders in the source strings. Instead of translating these variables or placeholders, you need to keep them in the translated strings where they should appear keeping in mind consistent grammar and style. Depending on how the developers internationalize the application or software, the variables or placeholders are typically enclosed in brackets, braces, chevrons, percents, underscores, or any combination of these symbols:

    [something]	[[something]]	{something}	{{something}}
    <something>	%something%	<%something%>	__something__

Sometimes, variables and placeholders may appear with a single per cent sign:

	Integer variable	%d	1%d	2%d	3%d

	Character variable	%c	1c	2%c	3%c

	Float variable		%f	1%f	2%f	3%f

	Double variable	      %lf	1%lf	2%lf	3%lf

	String variable	%s	1%s	2%s	3%s

	Octa variable		%o	1%o	2%o	3%o

	Hexadecimal variable	%x	1%x	2%x	3%x

Another way variables or placeholders typically appear in strings is with a single leading dollar sign:

	$something1     $something2     $something3

#### Don't start translating without understanding a product
Localization is not just about transforming text from one language into another without changing its meaning. Beyond that, the purpose of localization is to make the product available and accessible in other languages taking into account the appropriate contexts and experiences of the end-user using the product. This requires you, as a localizer, to understand how the product works from the end-user perspective.
