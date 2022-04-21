# Learn XML (For Beginners)

Follow below links to learn XML:

- [W3Schools - XML Tutorial](https://www.w3schools.com/xml/)
- [Guru99 - XML Tutorial for Beginners](https://www.guru99.com/xml-tutorials.html)
- [Joe Marini - XML Essential Training](https://www.linkedin.com/learning/xml-essential-training-2)

## Getting Started

### <strong>What is XML?</strong>

![Alt](other/images/module_1_1.png)

![Alt](other/images/module_1_2.png)

![Alt](other/images/module_1_3.png)

### <strong>XML Technologies</strong>

![Alt](other/images/module_2_1.png)

In addition to XML itself, there are certain related technologies that make working with XML to solve certain problems easier and more productive.

### <strong>Describing Data with XML</strong>

One of the main purposes of XML is to structure and describe information. Let's understand it with an example.\
To illustrate this example, let's consider some information that you would typically find on a business card, such as a person's name, various phone numbers, and maybe an email address, and there might be some additional information on a business card, like a company name, but just to keep the example simple, let's just agree that this is some fairly common data you'd find on a business card.

```
John S.

- +91-99999999999 (home)
- +91-88888888888 (work)
- +91-77777777777 (mobile)
```

You see, there are labels to describe the information that's on the business card, and ***this is an example of what XML does.*** It applies description and structure to the data that you're working with. So if we were to take the same example and look at it in XML, we might be able to structure it in a certain way. So, for example, I might have a tag called \<BusinessCard\> and the business card tag might be the root tag that holds other data, like for example, the name. And there might be various tags like phone, and the phone tag might have an attribute that describes what kind of phone it is, whether home or work or mobile, and there might be a tag for email. Now, you might be looking at this and saying, well, wait a second, business card tag, phone tag, I've never seen anything like this, and you're right. Now, if there was a business card XML tag set existing already that I could use to solve this data problem, I could go ahead and use it, but imagine for a moment that there was no such XML standard and the truth is I don't know if there is or isn't, but I could decide to sit down and create my own XML language called business card.

```
<BusinessCard>
    <name>John S.</name>
    <phone type="home">+91-99999999999</phone>
    <phone type="work">+91-88888888888</phone>
    <phone type="mobile">+91-77777777777</phone>
    <email>john@john.com</email>
</BusinessCard>

```
Remember, the X in XML stands for extensible, so if you have a particular data related problem or task and you want to use XML to solve it, you could either use an existing XML language if there is one, or you could just make one up.

Now, once I've done this, once I've collected this data here in XML, I can now take this data and give it to any other XML aware program. That program can then parse and extract data from this business card. Now, that program may not know what a business card is or what the various tags mean, but because XML is an open text-based standard, any application that can read XML would at least be able to parse this data from the business card file.

### <strong>Advantages and Drawbacks of XML</strong>

<strong><u>Advantages</u></strong>

![Alt](other/images/module_4_1.png)

- XML keeps content separate from presentation. You can take the data that your application uses and store it separately from how it's presented to users. That way, regardless of what kind of presentation medium you're using, whether it's mobile or desktop or print media, you can just simply flow the data into various layouts, and you can maintain a good separation between the content from how it's presented.

- XML is also an open format that can be read by many applications, and many applications today have also the ability to output XML, like Microsoft Office. So, because it's an open format, you can store your data in a way that can be read by many different applications, even those that haven't been written yet.

- XML can be used on both the client and the server, because remember, it's just a data format. Today's modern browsers, like Firefox, Chrome, Edge, Safari, can work with XML data. You can also use XML data in your applications. Whether they're client apps or server apps, they're just a really good way of storing information.

- XML has widespread support in multiple languages and runtimes. You can use XML from Python and C# and .NET and Visual Basic and Java, and lots of other programming languages. Even JavaScript. This support extends to different runtime platforms. XML can be used on .NET, Java, iOS, Android. You can use XML pretty much just about everywhere.

- XML also makes it possible for disparate systems to exchange data. These could be systems that were never designed to talk to each other in the first place. Let's suppose you have two computers and you want to share information between them. The problem is, one of those computers is modern and speaks a certain language. And the other one of those computers is a little bit older and only knows a different language. So, what do you do? XML can be used to help solve this problem. XML can create a bridge between these two computer systems so that they can exchange data, even though they're not aware of each other's native way of working with data.

<strong><u>Drawbacks</u></strong>

![Alt](other/images/module_4_2.png)

- It's not suitable for very large data sets. When I say very large data sets, that might vary. It's really up to you to decide, but generally, once you start getting into multiple megabytes of data, XML is probably not the most efficient way of storing it. XML does make it easy to interchange data, but as far as storing large data sets, databases are probably still the way to go.

- Some formats, like JSON, might be better in some cases, depending on how you're going to use the data. If you know that the data is going to be used in a JavaScript execution environment, for example, they're might be some cases where JSON is just more efficient.

- Some data types, like images, aren't represented well in XML because it's a text format and images aren't. Now, there is a way to do this. You can encode images and insert them into XML documents, but that gets ugly pretty quickly. And even though it's possible, it may not always be the best way of doing it.

- In XML, when it gets really complex, can quickly get hard to read. Now, if you're not planning on having humans reading your XML files, this may not be a big deal. But, it is something to be aware of.

## XML Overview

In this section, we will learn about basic rules of XML.

### <strong>Types of XML Content</strong>

Let's start of by learning the contents of XML files. There are about a half dozen or so types of XML content that you'll typically run into when working with XML data. If you're already familiar with HTML then many of these probably already look familiar.

![Alt](other/images/module_5_1.png)

<strong><u>The Document Declaration</u></strong>

![Alt](other/images/module_5_1.png)

The document declaration looks like this. It's an opening bracket with a question mark followed by the letters xml and then a version and encoding and then optional standalone declaration. The document declaration is technically optional though the W3C recommends it. It's always a good idea to have the document declaration. It identifies the file as an XML document and provides a place for the encoding and standalone attributes. It has to be at the very beginning of a file. You can't even have whitespace before it.

<em>Encoding Attribute</em>

The encoding attribute defaults to UTF-8 if you don't include it but it's always a good idea to include it. And if you decide to use a character set other than UTF-8 like Unicode UTF-16 for example this is where you would put that declaration.

<em>Standalone Attribute</em>

The standalone attribute identifies whether or not the document stands by itself or depends on something else. If it requires other data then you should say standalone equals no. Otherwise if the XML data is complete by itself you can set this attribute to yes.

![Alt](other/images/module_5_3.png)

<strong><u>XML Elements (Tags)</u></strong>

Next are XML elements which are sometimes called tags and if you've ever worked with HTML these will entirely familiar to you. Elements must have valid names.

![Alt](other/images/module_5_4.png)

![Alt](other/images/module_5_5.png)

Attributes in XML work the same way they do in HTML. They're specified on opening elements tags only. They have to start with a letter or an underscore.

![Alt](other/images/module_5_6.png)

<strong><u>Comments</u></strong>

![Alt](other/images/module_5_7.png)

<strong><u>Character Data Section</u></strong>

![Alt](other/images/module_5_8.png)

Character data sections are specific using CDATA and they're part of the document content. The actual contents of CDATA sections are not parsed by the XML parser. It simply skips the internal content it doesn't try to figure what kinds of data might be in there. It just skips over the entire section. They're defined by using an open angle bracket followed by an exclamation point and then a square bracket, the word CDTATA and another square bracket and they end with two square brackets and a closing angle bracket. They're typically used to contain unescaped text data such as characters that aren't legal within parsed XML.

![Alt](other/images/module_5_9.png)

For example, suppose I had an XML document that contained a script tag and inside that script I had a function. Now this is going to cause a problem in XML because that return statement right there with ***a < b*** contains an angle bracket. This isn't an issue in HTML because the browser knows where a script tag is and when the browser is parsing the script tag it knows not to look for things like angle brackets and to treat them as opening tag names but an XML parser don't know. Remember you can make your own tags up so inside a tag if you have an illegal character that's going to cause a problem. So the way you get around this problem is by enclosing this in a CDATA section. This will cause the parser to skip over the contents and then you can put whatever characters you want in there.

<strong><u>Processing Instructions</u></strong>

![Alt](other/images/module_5_10.png)

Processing instructions are a way for XML content to delivery special instructions to the XML parser. They have the form of an open angle bracket followed by a questions with a targetName and an instruction followed by a question mark and a closing angle bracket. Now if you're paying attention you might be saying to yourself, well wait a second that's the same format as the XML document declaration and you're right. It is, it's pretty much the same format. The xml target name is reserved because it's part of the document declaration but a processing instruction can start with a number or a letter, and be followed by digits or letters, hyphens, periods and underscores.

An example of why you might use a processing instruction is maybe you have an application that has multiple spell-checking modes and a particular document might want to indicate to your app that a particular language should be used when a document is being spell-checked. It's just a way for the XML data to contain information that the parser itself can use to affect how the parsing is executed.

![Alt](other/images/module_5_11.png)

<strong><u>Entities</u></strong>

![Alt](other/images/module_5_12.png)

There are also character entities. For example, if you wanted to include a specific character which is not available in the keyboard in your XML data you can do that by using ampersand followed by a hash symbol and then the character's code number. Some character entities also have special names. For example the ampersand itself is written by ampersand then amp a semicolon or quote characters which are an ampersand Q-U-O-T and then a semicolon.

![Alt](other/images/module_5_13.png)

### <strong>Proper XML Syntax</strong>

![Alt](other/images/module_6_1.png)

- XML documents must have a single root tag. They have to have one, it's required, and if you remember back to the business card example, the business card tag was the root tag in that particular document.

- XML documents also must be what's called well-formed. In other words, there are certain syntax rules that XML documents have to adhere to. The first one is that empty tags have to be closed with a slash before the closing angle bracket. Now, this is different than HTML, for example, where image tags are empty, but they don't have that trailing slash, and the reason is because the browser knows what HTML is, it knows there's a tag called IMG, and it knows that it's empty. In XML, however, remember, you get to make up your own tags, and the program that's parsing the XML may not know what a particular tag is or what it means, so you have to indicate that a particular tag is empty by including that trailing slash there before the closing angle bracket.

![Alt](other/images/module_6_2.png)

- Attribute values can also not be what's called minimized, and you typically see this, for example, when you're working with ***select lists*** in HTML. On option tags, for example, you can just simply put the word **selected** as an attribute with no value, and the select list will show up in the web browser with that option selected. Now, in XML, again, there's no way for the XML program to know whether your attribute requires a value or not, so the way to get around this is by putting the name of the attribute and then equal to the name of the attribute as the value.

- Attribute values also have to be inside of quotes, either single or double. Now, in HTML, you can get away with just putting attribute equals value, but in XML that doesn't fly. You have to put the values inside quotes.

- And then finally, tags have to be properly nested inside of each other. Back in the old days, browsers let you get away with this because they could basically figure out what you meant. So, for example, if you had bold and italic text, you had an opening B tag and then an opening I tag, but then you closed the B tag and then closed the I tag, the browser would pretty much forgive you, 'cause it could figure out what was going on. In XML, that's illegal, you have to have the tags properly nested and completely inside of each other.

### <strong>Valid Documents</strong>

![Alt](other/images/module_7_1.png)

Suppose you have an XML parser represented by these **gears** in above figure. You give it an XML file and then as long as the syntax is proper and you've correctly named your elements and you've followed the XML syntax rules then good results come out the other side. And that's what we mean by saying that an XML file is well formed. But there's another way to make sure that XML documents are what's called valid. You can apply a set of rules which are applied to the parsing process in addition to the well-formness checks.

For example you can supply rules that say things like tag A is only ever allowed to incur inside of tag B and attribute X only has these values and so on. If the XML parser parses the document correctly and the document content passes the rules then the document is valid in addition to well-formed.

There are two ways to do this.

![Alt](other/images/module_7_2.png)

The first is called document type definitions. The second is called XML schema. Document Type definitions are simple to use but they're not very powerful. They give you basic ways of making sure that certain content meets basic rules. They're written using as syntax that's somewhat different than XML. It's similar but not exactly the same. XML schema on the other hand is much more powerful and flexible then DTDs are. And they're written using XML syntax rules.

### <strong>XML Namespaces</strong>

![Alt](other/images/module_8_1.png)

- XML Namespaces have the form of the letters XMLNS and then equal to some character string. And if you've used HTML before, you've probably seen something like as shown above in image. It usually appears on the HTML tag. Now the character string that goes inside that XMLNS attribute just has to be unique. It's usually a URL, but it doesn't have to be. The spec just says it needs to be a unique value. And in fact, the XML parser doesn't even try to access whatever is at that URL.

- XML Namespaces are used to prevent tags from different languages from conflicting each other when you try to use them in the same XML document.Now if I want to create an XML document that includes tags from different tag sets, there's the potential for someone using the same name for a tag that I've decided to use in my tag set.

![Alt](other/images/module_8_2.png)

So, let's take a look at an example. Suppose I have an HTML file with a table in it and HTML tables have things like table rows and table cells. They're used to lay out tabular data. However, if I create an XML document and I work for, say, a furniture company, to me, a table means something completely different. I'd have a table and my table definition for furniture might have a type. It's going to have a price, a material, how many I have in stock. Well if I try to use my XML table inside my HTML table, that's going to cause problems. The process is going to look at the table tag and say, "Wait a minute, what is type? What is Price? I've never seen this before." So if we want to take the XML data from the furniture table and include it in our HTML file, we need a way to make sure that the two table tags don't collide with each other. ***And that's where XML Namespaces come in.***

![Alt](other/images/module_8_3.png)

The way you'd solve this is by defining an XML Namespace for your tag set. Now here on my HTML tag, I would have the XMLNS equals and that's the XHTML Namespace. And it's followed by another Namespace definition. In this case, I've got XMLNS and then furn for furniture. And I'm pointing to a URL that I just completely made up. I have no idea whether that actually exists or not, but I'm just illustrating an example here. The first XMLNS definition, the one without the colon, is called the default Namespace. Any tag that doesn't have a prefix in front of it is assumed to be in the default Namespace.

![Alt](other/images/module_8_4.png)

So here in the HTML document, if there's a tag that appears in HTML, and there's no prefix, then the browser will just assume that's part of the HTML definition. So here's how you'd use this. Inside my HTML, I can define my table just like I always do. I have my table tag, my table row, table cell. But now, in order to include the furniture table definition, I simply put the prefix furn in front of the tags that appear in my furniture table Namespace. So you can see that that matches up with the XML Namespace definition I included at the top of the file. So now when the browser comes across a tag that has the furn prefix in front of it, it's going to say, "Okay, well I don't know what this is, but it's a well-formed tag and it's embedded in my content. And I'll parse it but I'm not going to try to interpret it or figure out what to do with it." This is how XML Namespaces are used, so that you can combine data from separate sources without having to worry about name collisions.

## Working with XML

### <strong>Our First XML</strong>

Checkout here - [First XML](03-Working_with_XML/01-firstXML.xml)

If you open this file in browser, you will find a message saying "This XML file does not appear to have any style information associated with it". And then it just shows the document tree here in the window. So you can see Browser is just simply showing the contents of the XML. So this is pretty straight forward, no styling information. Just the raw XML data.

So let's see if we can give our XML an appearance by associating some styling information with it.

### <strong>XML and CSS Style</strong>

Checkout here the XML file - [First XML](03-Working_with_XML/02-firstXML.xml)

Checkout here the CSS file- [CSS file](03-Working_with_XML/firstXMLstyle.css)

### <strong>Styling XML tags</strong>

Let's take our business card example and style it.

Checkout here the XML file - [First XML](03-Working_with_XML/03-BusinessCard.xml)\
Checkout here the CSS file- [CSS file](03-Working_with_XML/BusinessCardstyle-1.css)

If you open above XML file in the browser, you will see that each one of the individual elements is being styled by itself. However, if you're paying attention, you'll notice that there are no labels. The value of the attributes are not there. So that's a different kind of problem, and we'll have to handle that problem a little bit differently.

### <strong>Advanced CSS with XML</strong>

We've seen previously how to style XML code using CSS and have the browser to display the contents of XML tags instead of the XML document tree. But the problem that we run into is that we don't have a way to put the labels in front of the content of the XML that's being styled. In this section we're going to see how to do that using CSS.

Checkout here the XML file - [First XML](03-Working_with_XML/04-BusinessCard.xml)\
Checkout here the CSS file- [CSS file](03-Working_with_XML/BusinessCardstyle-2.css)

If you see the XML file, you will find that root tag has been changed from business card to business cards. This is done to to have a container that can hold more than one business card. And also new business card entry has been added. Other than that, attribute, primary is being used.

Checkout the CSS file above that put labels in front of the content in the XML file.

## Manipulating XML with DOM

In the previous section we saw how to define our first XML document and then use CSS to give the XML an appearance. The CSS approach though has some downsides.
- First, there's no easy way to reorder the XML content using CSS. And in fact, some people would argue that CSS shouldn't even be used for things like that.
- The second problem is that if you have an XML tag and that tag has a certain meaning and you want to take an XML tag and based upon its value it would perform some functions. CSS doesn't really give you a good way of doing that. It's mostly just a way of styling the appearance of the static XML data.

In this section however, we'll see how to use the DOM, or the Document Object Model, to exercise fine level control over XML content.

- The Document Object Model is a standard set of APIs or functions for working with document content. It's platform, browser, and language neutral. The examples we'll be shown here use JavaScript in a browser, but there are DOM implementations for other languages as well, like Python, Java, C#, and so on.

    ![Alt](other/images/module_13_1.png)

- The DOM represents the document content as a tree structure and the contents of the tree are called nodes.

- Let's take a look at an example and see how this works. Suppose I had an HTML document and this is a pretty simple one here on the left. I've got my html tag and inside there I've got the head and the body, the head has a title, the body has a paragraph. The DOM represents this document as a tree structure. At the top is the HTML node, inside the HTML node are the head and the body, and these are said to be child nodes of the HTML node, which is the parent. Then inside the head and body are the title and paragraph tags respectively. And so far we've talked about tags, but the actual content of these tags are themselves nodes within the DOM. So inside the title tag there's a text string called Document, and inside the paragraph there's a text string which has the value Paragraph Text. And each one of these is a node in the document. We can express the relationship between these nodes using familiar family-style names. So, for example, the head and the body are child nodes of the HTML node, which is said to be the parent. The title is a child of the head node and the document is a child of the title node. The head and body nodes are siblings of each other.

    ![Alt](other/images/module_13_2.png)

Let's talk about some important DOM properties that you'll come across when using these functions.

- Below 4 provide information about any given node.

    ![Alt](other/images/module_13_3.png)

- There are also properties for accessing the family relationships of nodes.

    ![Alt](other/images/module_13_4.png)

- There are functions for taking nodes and moving them around in the document.

    ![Alt](other/images/module_13_5.png)

- There are also properties and functions for doing things like accessing and creating document content.

    ![Alt](other/images/module_13_6.png)

- There are some other important miscellaneous properties.

    ![Alt](other/images/module_13_7.png)

### <strong>Discovering Document Content</strong>

Checkout this file which demonstrate how we can use the DOM APIs to discover information that's in a document - [Example-1](04-Manipulating_XML_with_DOM/01-Example.html)

You can see that I've got a pretty simple HTML file. In the HTML content, I've got an XML tag, which I'm using to embed XML content into the webpage. And in case you're wondering, yes that is perfectly legal to do within HTML. The browser will see the HTML tag and parse it like any other tag, it just won't know what to do with it, it won't do anything special with it. Now, in real world usage, you probably won't see XML used like this. Typically, XML data will be the result of some web service call or it will come from a database or you retrieve it using Ajax, and then operate on it separately. But in the interest of keeping these examples simple and self-contained, I'm just embedding the XML content right here into the webpage. Now I didn't have to use the name XML for the tag, I could just use any other tag, but I have it use XML to indicate what it is.

### <strong>Discovering Document Content</strong>

In the previous example, we saw how to use the DOM API to discover and extract document content. In this example, we're going to see how to use the DOM to create new document content.

Checkout this HTML file, [Example-2](04-Manipulating_XML_with_DOM/02-Example.html) and CSS file [CSS File](04-Manipulating_XML_with_DOM/BusinessCardstyle-1.css)

When you're working with the DOM, you can manipulate the content in any way that you want. You can use the presence of certain tags to trigger certain actions. You can reorder document content. You can selectively include content or derive new calculated content. So, using the DOM to manipulate xml is very very powerful.

### <strong>Practical Example</strong>

Checkout the code here, [Cafe](04-Manipulating_XML_with_DOM/practicalExample/)