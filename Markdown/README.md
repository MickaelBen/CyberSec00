## Lien vers les Docs

- MarkDown
	- [GitHub_Docs -> Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
	- [GitHub_adam-p -> Markdown Cheatsheet ](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
	- [MarkDownGuide.org -> Basic Syntax](https://www.markdownguide.org/basic-syntax/#links)
	- [Obsidian -> Docs](https://help.obsidian.md/How+to/Internal+link).

___
<br> 

## Synthese Docs

### Headers

```md
# This is a heading 1
## This is a heading 2
### This is a heading 3 
#### This is a heading 4
##### This is a heading 5
###### This is a heading 6
```

___
<br> 

### Emphasis

1.
```md
*This text will be italic*

_This will also be italic_
```

_This text will be italic_
_This will also be italic_

2. 
```md
**This text will be bold**

__This will also be bold__
```

**This text will be bold**
**This will also be bold**

3. 
```md
_You **can** combine them_
```

_You **can** combine them_

4. HightLigne
```md
~The world is flat.~~
```

~The world is flat.~~

___
<br>

### Lists

- #### Unnumbered lists

```md
- Item 1
- Item 2
  - Item 2a
  - Item 2b
```

-   Item 1
-   Item 2
    -   Item 2a
    -   Item 2b


- #### Numbered Lists

```md
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

1.  Item 1
2.  Item 2
3.  Item 3
    1.  Item 3a
    2.  Item 3b


- #### Task list

```md
- [x] #tags, 
- [ ] [links](), 
- [ ] **formatting** supported
```

- [x] #tags , 
- [ ] [links](), 
- [ ] **formatting** supported

___
<br> 

### Blockquotes

```md
> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

\- Doug Engelbart, 1961
```

> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.

- Doug Engelbart, 1961

- #### Other Blockquotes

1. 
```md
> Human beings face ever more complex and urgent problems, and their effectiveness 
>
> > Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.
```

> Human beings face ever more complex and urgent problems, and their effectiveness
>
> > Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society.


2. 
```md
> [!error]
> efzef

> [!Warning]
> warning

>[!info]
> test

>[!note]
> test
>> [!warning]
>> info info
>>> [!error]
>>> error info
```

> [!error]
> efzef

> [!Warning]
> warning

>[!info]
> test

>[!note]
> test
>> [!warning]
>> info info
>>> [!error]
>>> error info

___
<br> 

### Code

- #### Inline code

```md
Text inside `backticks` on a line will be formatted like code.
```

Text inside `backticks` on a line will be formatted like code.


- #### Code blocks

You can add syntax highlighting to a code block by adding a language code after the first set of backticks.

````md
```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
````

```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
 
```python
s = "Python syntax highlighting"
print s
```
 
```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```

___
<br> 

### Horizontal Rule

```md
___
---
```

___
---


___
<br> 

### Link

- #### External links

Markdown style links can be used to refer to either external objects, such as web pages, or an internal page or image.

```md
http://obsidian.md - automatic!
[Obsidian](http://obsidian.md)
```

- #### 


- #### Anchor
You can make a link on the same page like this.

```md
See the section on [`code`](#code).
```

See the section on [`code`](#code).


- #### Other Links

> [title](https://www.example.com)
>
> <https://www.markdownguide.org>
>
> <fake@example.com>

> I love supporting the **[EFF](https://eff.org)**
>
> This is the *[Markdown Guide](https://www.markdownguide.org)*
>
> See the section on [`code`](#code).


___
<br> 

### Image

1. 
```md
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

Resizing images
![Engelbart|100](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

2. 
```md
![[og-image.png]]
```

![og-image.png](https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/og-image.png)


3. 
> ![alt text](image.jpg)  


___
<br> 

### Video

```md
<iframe src="https://www.youtube.com/embed/NnTvZWp5Q7o"></iframe>
```

<iframe src="https://www.youtube.com/embed/NnTvZWp5Q7o"></iframe>


___
<br> 

### Table

```md
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
```

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |


___
<br> 

