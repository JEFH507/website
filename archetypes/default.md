---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
slug: ""
description: ""
tags: [""]
series: [""]
series_order:
showAuthor: false
authors:
  - "javierfeliu"
  - "josefeliu"
showAuthorsBadges : false  
---
TEMPLATE!
 {{< typeit 
  tag=h2
  speed=50
  breakLines=false
  loop=true
>}}
Sub Tittle here,
Continue here. 
{{< /typeit >}}

{{< lead >}}
Tag Line
{{< /lead >}}


{{< lead >}}
Subscribe now for more articles like this. You'll get fresh ideas and practical advice you can use, in less than 3 minutes. Stay ahead of the curve!
{{< /lead >}}
<script async data-uid="99db4e9842" src="https://javier-feliu.ck.page/99db4e9842/index.js"></script>

{{< lead >}}
¡Suscríbete ahora por más articulos como este y mantenerte un paso por adelante! Obtendrás nuevas ideas y consejos prácticos, en menos de 3 minutos.
{{< /lead >}}
<script async data-uid="c675c53081" src="https://javier-feliu.ck.page/c675c53081/index.js"></script>

SHORT CODES!

**GENERALS**
{{< lead >}}
Text Here
{{< /lead >}}

{{< alert >}}
**Warning!** Text Here
{{< /alert >}}

{{< alert "twitter" >}}
Don't forget to [follow me](https://twitter.com/com/JavierFeliuH) on Twitter.
{{< /alert >}}

{{< alert icon="fire" cardColor="#e63946" iconColor="#1d3557" textColor="#f1faee" >}}
This is an error!
{{< /alert >}}

{{< badge >}}
New article!
{{< /badge >}}

{{< button href="#button" target="_self" >}}
Call to action
{{< /button >}}

{{< tweet user="SanDiegoZoo" id="1453110110599868418" >}}

{{< vimeo 55073825 >}}

{{< vimeo id="146022717" class="my-vimeo-wrapper-class" title="My vimeo video" >}}

{{< youtube w7Ft2ymGmfc >}}

{{< youtube id="w7Ft2ymGmfc" autoplay="true" >}}

{{< youtube id="w7Ft2ymGmfc" title="A New Hugo Site in Under Two Minutes" >}}

**LIST ARTICLES**
{{< article link="/docs/getting-started/" >}}

{{< list limit=2 >}}

{{< list title="Samples" limit=5 where="Type" value="news" >}}


**IMAGES** (where gallery is a folder inside the new post content root, IF there is no **"/gallery/*.jpg"** the file is substracted from the post content root folder)

{{< carousel images="{gallery/03.jpg, gallery/01.jpg, gallery/02.jpg, gallery/04.jpg}" >}}

{{< carousel images="gallery/*" aspectRatio="21-9" interval="2500" >}}
**The aspect ratio for the carousel. Either 16-9, 21-9 or 32-9. It is set to 16-9 by default.**

{{< icon "github" >}}
*Custom icons can be added by providing your own icon assets in the assets/icons/ directory of your project. The icon can then be referenced in the shortcode by using the SVG filename without the .svg extension.
Icons can also be used in partials by calling the icon partial.*

{{< figure src="elephant.jpg" title=">An elephant at sunset" >}}

**FIGURE**
 
figure is an extension of the image syntax in Markdown, which does not provide a shorthand for the more semantic HTML5 
<figure> element.

{{< figure
    src="abstract.jpg"
    alt="Abstract purple artwork"
    caption="Photo by [Jr Korpa](https://unsplash.com/@jrkorpa) on [Unsplash](https://unsplash.com/)"
    >}}

<!-- OR -->

![Abstract purple artwork](abstract.jpg "Photo by [Jr Korpa](https://unsplash.com/@jrkorpa) on [Unsplash](https://unsplash.com/)")


The figure shortcode can use the following named parameters:

src
URL of the image to be displayed.
link
If the image needs to be hyperlinked, URL of the destination.
target
Optional target attribute for the URL if link parameter is set.
rel
Optional rel attribute for the URL if link parameter is set.
alt
Alternate text for the image if the image cannot be displayed.
title
Image title.
caption
Image caption. Markdown within the value of caption will be rendered.
class
class attribute of the HTML figure tag.
height
height attribute of the image.
width
width attribute of the image.
attr
Image attribution text. Markdown within the value of attr will be rendered.
attrlink
If the attribution text needs to be hyperlinked, URL of the destination.


Blowfish also supports automatic conversion of images included using standard Markdown syntax. Simply use the following format and the theme will handle the rest:
![Alt text](image.jpg "Image caption")

**GALLERY**

gallery allows you to showcase multiple images at once, in a responsive manner with more varied and interesting layouts.

In order to add images to the gallery, use img tags for each image and add class="grid-wXX" in order for the gallery to be able to identify the column width for each image. The widths available by default start at 10% and go all the way to 100% in 5% increments. For example, to set the width to 65%, set the class to grid-w65. Additionally, widths for 33% and 66% are also available in order to build galleries with 3 cols. You can also leverage tailwind’s responsive indicators to have a reponsive grid.

Example 1: normal gallery

{{< gallery >}}
  <img src="gallery/01.jpg" class="grid-w33" />
  <img src="gallery/02.jpg" class="grid-w33" />
  <img src="gallery/03.jpg" class="grid-w33" />
  <img src="gallery/04.jpg" class="grid-w33" />
  <img src="gallery/05.jpg" class="grid-w33" />
  <img src="gallery/06.jpg" class="grid-w33" />
  <img src="gallery/07.jpg" class="grid-w33" />
{{< /gallery >}}

Example 2: responsive gallery

{{< gallery >}}
  <img src="gallery/01.jpg" class="grid-w50 md:grid-w33 xl:grid-w25" />
  <img src="gallery/02.jpg" class="grid-w50 md:grid-w33 xl:grid-w25" />
  <img src="gallery/03.jpg" class="grid-w50 md:grid-w33 xl:grid-w25" />
  <img src="gallery/04.jpg" class="grid-w50 md:grid-w33 xl:grid-w25" />
  <img src="gallery/05.jpg" class="grid-w50 md:grid-w33 xl:grid-w25" />
  <img src="gallery/06.jpg" class="grid-w50 md:grid-w33 xl:grid-w25" />
  <img src="gallery/07.jpg" class="grid-w50 md:grid-w33 xl:grid-w25" />
{{< /gallery >}}





**VISUALIZATION**
**CHART**
{{< chart >}}
type: 'bar',
data: {
  labels: ['Tomato', 'Blueberry', 'Banana', 'Lime', 'Orange'],
  datasets: [{
    label: '# of votes',
    data: [12, 19, 3, 5, 3],
  }]
}
{{< /chart >}}

{{< mermaid >}}
graph LR;
A[Lemons]-->B[Lemonade];
B-->C[Profit]
{{< /mermaid >}}
*Refer to the official Mermaid docs for details on syntax and supported diagram types.*

{{< swatches "#64748b" "#3b82f6" "#06b6d4" >}}

{{< timeline >}}

{{< timelineItem icon="github" header="header" badge="badge test" subheader="subheader" >}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus non magna ex. Donec sollicitudin ut lorem quis lobortis. Nam ac ipsum libero. Sed a ex eget ipsum tincidunt venenatis quis sed nisl. Pellentesque sed urna vel odio consequat tincidunt id ut purus. Nam sollicitudin est sed dui interdum rhoncus. 
{{< /timelineItem >}}


{{< timelineItem icon="code" header="Another Awesome Header" badge="date - present" subheader="Awesome Subheader" >}}
With html code
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
{{< /timelineItem >}}

{{< timelineItem icon="star" header="Shortcodes" badge="AWESOME" >}}
With other shortcodes
{{< gallery >}}
  <img src="gallery/01.jpg" class="grid-w33" />
  <img src="gallery/02.jpg" class="grid-w33" />
  <img src="gallery/03.jpg" class="grid-w33" />
  <img src="gallery/04.jpg" class="grid-w33" />
  <img src="gallery/05.jpg" class="grid-w33" />
  <img src="gallery/06.jpg" class="grid-w33" />
  <img src="gallery/07.jpg" class="grid-w33" />
{{< /gallery >}}
{{< /timelineItem >}}

{{< /timeline >}}

**TypeIt**
{{< typeit >}}
Lorem ipsum dolor sit amet 
{{< /typeit >}}

{{< typeit 
  tag=h1
  lifeLike=true
>}}
Lorem ipsum dolor sit amet, 
consectetur adipiscing elit. 
{{< /typeit >}}

{{< typeit 
  tag=h3
  speed=50
  breakLines=false
  loop=true
>}}
Lorem ipsum dolor sit amet, 
consectetur adipiscing elit. 
{{< /typeit >}}

Parameter	Description
*tag*	[String] html tag that will be used to render the strings.
*classList*	[String] List of css classes to apply to the html element.
*initialString*	[String] Initial string that will appear written and will be replaced.
*speed*	[number] Typing speed, measured in milliseconds between each step.
*lifeLike*	[boolean] Makes the typing pace irregular, as if a real person is doing it.
*startDelay*	[number] The amount of time before the plugin begins typing after being initialized.
*breakLines*	[boolean] Whether multiple strings are printed on top of each other (true), or if they’re deleted and replaced by each other (false).
*waitUntilVisible*	[boolean] Determines if the instance will begin when loaded or only when the target element becomes visible in the viewport. The default is true
*loop*	[boolean] Whether your strings will continuously loop after completing

**KATEX**
{{< katex >}}
\\(f(a,b,c) = (a^2+b^2+c^2)^3\\)

% KaTeX inline notation
Inline notation: \\(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\\)

% KaTeX block notation
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
$$

**CODE**
{{< github repo="nunocoracao/blowfish" >}}
{{< gitlab projectID="278964" >}}



LVE BRADCASRT SKYPY
LAPTOP
CAMERA
IPHONE


