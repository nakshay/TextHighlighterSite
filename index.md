# TextHighlighter [ ![Download](https://api.bintray.com/packages/akshaynaik/maven/TextHighlighter/images/download.svg) ](https://bintray.com/akshaynaik/maven/TextHighlighter/_latestVersion)

TextHighlighter is simple android API for developers to show highlighted text in android apps, also provides methods to show styled text.

<H2>Description:</H2>

The purpose of TextHighlighter API is provide the simplest way to highlight the text in android apps.
The API can be used with all andriod views which allows the rendering of text using ```Html.fromHtml()``` method.

<H2>Usage</H2>

Add below line in app ```build.gradle```
 
```gradle
dependencies {
	compile 'com.github.nakshay:texthighlighterapi:1.2.1'
}
```

<H2>Code snippets</H2>

Create the object of TextHighlighter

```TextHighlighter highlighter=new TextHighlighter();```

Set the color for specific word

```
highlighter.setColorForTheToken("Awesome","red");
highlighter.setColorForTheToken("Text","purple");
highlighter.setColorForTheToken("Highlighter","blue");

```
OR

set color for multiple words
```
highlighter.setColorForTheToken(String[],"color");
```
To set default color, if no color is specified.

```
highlighter.defaultColor="black" 
```

Call the method ```getHighlightedText(String textToBeHighlighted)``` and pass the text to be highlighted

set styles for specific word

```
highlighter.setStyleForTheToken("Awesome",TextHighlighter.BOLD);
highlighter.setStyleForTheToken("Text",TextHighlighter.UNDERLINE);
highlighter.setStyleForTheToken("Awesome",TextHighlighter.ITALIC);

```

OR

set style for multiple words

```
highligter.setStyleForTheToken(String[],style);
```

Call the method ```getStyledText(String textToBeStyled)``` and pass the text to be styled.

```
String highlightedText=highlighter.getHighlightedText("Awesome Text Highlighter");
```

both highlited and styled text can be used by passing highlited text to styled text and vice versa.


Pass the returned string to ```Html.fromHtml()``` to get highlighted text

``` textViewobj.setText(Html.fromHtml(highlightedText)); ```

you can add extra tags by appending tags inside ```Html.fromHtml()``` 

**More methods**

```
String = getColorForTheToken(String token);
String = getStyleForTheToken(String token);

String[] = getColorForTheToken(String[] token);
String[] = getStyleForTheToken(String[] token);
```


<H2>Note:</H2>

Named colors may not work always, you can use Hex values insted of named colors, hence using Hex values instead of named colors is recommended.


Example:-

```highlighter.setColorForTheToken("Awesome","#D83400"); ```

##Supported tags for text styling

 ```
 <b>
 <i>
 <u>
 <sup>
 <sub>
 ```


Visit [www.htmlcolorcodes](http://htmlcolorcodes.com/) for awesome colors and their Hex values. 


<H2>Screenshot</H2>


![alt tag](https://raw.githubusercontent.com/nakshay/TextHighlighter/master/screenshot.png) ![alt tag](https://raw.githubusercontent.com/nakshay/TextHighlighter/master/TextHighlighter.png)

<H2>License</H2>

Copyright 2016 AKSHAY NAIK

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.




