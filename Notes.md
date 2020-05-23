# Notes on the project as I go on 

TODO's 

1. Build the project 
    - creating the folder structure 
    - adding files
    - connecting files

2. build the Nav bar 
    - with two links and a name

* The homepage of this website has sort of like a grid type of presentation 
where the elements images are positioned on rows of three buy columns of 
four elements, and it will use: *

3. build the portfolio item grid
    - adding files
    - images 
    - titles
    - animations (to accomplish this with JavaScript)

4. build the About Me page
    - image 
    - split column layout
    - content


TIPS:

1. When tackling a project like this, doing this type of todo list will help by giving me 
structure
2. this allows me to define clearly the structure of the project and what i need to do  
3. As I go thru the project I can later add, annotate or pin more detailed specs or ideas 
on these notes so that I can later refer to them as go on 
4. breaking the project into different steps allows me not to procrastinate or get paralized 
by the size of the project, because as I break it down into smaller pieces I can start working 
on a single small piece without being worried about the larger project overall. Taking big 
tasks and breaking them into smaller tasks makes the job easier to work in and to focus at 
one thing at a time


--------------------------------------------------------------------------------
    
1. Set up the project and add the general folder/file structure 

- created a repo on GitHub, then cloned it in my local machine (this is my project container)

- from the Terminal I go to my project repo as my pwd and open the text editor from there

- here I see my new README file, so I edit it and also create a NOTE md files, and edit them 
respectively

- now that I am inside my project repo (container) I now create a directory named: "portfolio-html-site". 
This directory will hold my projects folders, files and any other images, resources or assets 
Note: the README and Notes .md files will reamin outside this project folder for now ...

- inside the "portfolio-html-site" folder create two html files: index.html and about.html

- I type some heading text on both pages and "Live Server" them just to make sure they area working ok. 

--------------------------------------------------------------------------------

2. Lets start with the Styling part

- created a link and a stylesheet for it 

- now create two or more style rules for the html docs and "Live Server" them to make sure the css link is ok and we can now start working adding style and content to the project documents

--------------------------------------------------------------------------------

3. Images 

- create a folder within the project folder called images. This will hold the project images.

*A great source for **free** source for pictures is unsplash*


--------------------------------------------------------------------------------


4. For now we pretty much have the *architectural / structure* thing done: the folders, the files and the images are all set in place. Now comes the CODING stuff ....


--------------------------------------------------------------------------------

5. start building the nav bar 

- create both links for the index and about pages with anchor tags

- created a parent div class named container and within this have a child div class called nav-wrapper and within this have child elements: the two anchor tag for links index and about and another simple div for my name

- now if I want to have index and about on the left side of my page and I want my name on the right side of the page I can use div to create two different containers to separate these to the left and the right. Will then make two  div classes: left-side div class and right-side div class, each containing index and about anchor tags for the left most column, and the other containing the  regular div with my name for the right most column

What we're doing is we are wrapping the code in a way that is goin f to make it much more straight forward to select, manipulate and custome style these as individual pieces, or properly named: html elements.

Hence I will also create a div wrapper for each of my anchor tags, one for the inde.html and another for the about.html. Both wrappers will have a div class "nav-link-wrapper", also note this divs are child elements of the div classes: left-side and right-side respectively.

And also I am going to create another div wrapper class brand,  for the div containing the name text. It it will be a child of the right-side div class

For now the Nav bar has been set up as it relates to the structural tags. In other words tags that will allow us to  structure/layout it, and also style it.


--------------------------------------------------------------------------------

6. style the nav bar

- erase the initial styles rules we had at he stylesheet to corroborate the links were working

- here we area going to start working with flexbox, a tool of CSS

- first I will target the div class that holds the nav bar, and that is the nav-wrapper div, not the container but the nav-wrapper and give it a property/value rule of display: flex; ... once this happens and I refresh the html document the name in my html doc moves to the left instead of being beneath the Home and About text ...

The flex value to property display it is applied to the div class nav-wrapper and this is applied to the child elements of nav-wraper, which are two: the left-side div class and the right-side div class. It just ignores whatever is inside the left-side and right-side div elements. 

So now flex will now not have the div child elements of nav-wrapper to be stacked on top of each other but lined up next to each other.

- also add to nav-wrapper the property/value: justify:content; ... this will do as it says, it will justify the content by spacing the two child elements of nav-wrapper, which are left-side and right-side will all the space it has to do so. Take a look now to see how the name text moves to the extreme right side of the page. 

- add 38 pixels to padding. 

- up until we have added styles to the entire vav bar, now we can start adding different styles to the left-side and right-side divs 

- so to the left-side div class I can add display:flex.
Since this left-side div class has two child elements: two nav-link wrappers, now flex will make them be, instead of one on top of the other, be one next to the other. Refresh and take a look. 

- now to style by traversing the three in CSS is like this: we will apply a style to the nav-wrapper, then left-side-wrapper then div. Whatever style rule I apply will traverse form the nav-wrapper, going thru left-side-wrapper until amy div that is the child of left-side-wrapper, and that's where the style rules will be applied. And to this I will apply a margin-right: 20px to separate the two  elements nav-link-wrapper that have one the index. html and the other the about.html. And also change the font size to font-size: 0.9em;

The way em works it is the percentage of the normal size of the font. So 1em will be the actual size of the font, and 0.9em will be 90% of the actual size of the font.

I can also do not have to type text on the HTML document as uppercase, as I can do it at CSS. So for the Home and About text within the anchor tags I can also include text-transform: uppercase.

- now I can add style specifically to each of the nav-link-wrapper (there are two, one holds the anchor tag for the index.html and the ohter holds the anchor tag for the about.html). So I add height of 22px, and then border-bottom: 1px solid transparent and then transition: border-bottom 0.5s, that means half a second.

I will not going to be able to see the border now but will it work on animations. 

Transition will call upon the part taht will want to animate, so here we want to animate the border-bottom for half second. 

Now that I have that nav-link-wrapper styled I can go and style the anchor tags within that div. And I do that like this: 
.nav-link-wrapper a. This means that insde of the nav-link-wrapper jsut grab the a link. And we can add a different color: #8a8a8a, also if I take a look a the links of Home and About at the html document, I will see that they area undelined. It is ugly but that's how they come with the standard basic HTML underline when used. I can eliminate this by telling not to have any underline at all. So we're going to use the border-bottom attribute to manage that style. So we say text-decoration: none; and transition: color 0.5s.

What we are doing here is we area setting it up so that we can have two animations because we want to animate the color and also want to animate the border-bottom.  

If we look at the html doc the underline is gone and we have changed the color.

- we're pretty much about to end styling the nav bar, we just have two more styles to do: The first one is the hover action. So that when the cursor hover above the Home and About elements we want it to change the style. 
For this I type: 
.nav-link-wrapper:hover {}

And that's how I tell CSS to use a hover state action. So I type: 
border-bottom: 1px solid black;

And then type another rule: 
.nav-link-wrapper a:hover {}
and add color: black;

Actually we have two different hover states, one for the div and one for the link itself. AND THAT'S HOW IT WORKS ... NO EXPLANATION OF WHY .... :-/

--------------------------------------------------------------------------------

7. Portfolio items 
This is what takes the majority of the screen real estate so this

Now I can go into the top of the CSS style sheet to include my master style rules, so I am giving to body tag a margin of 0px, because it comes by default of 8px. SO to get rid of that we need to overrid it by turning intol to 0px. Right on top of the style sheet. 

Also in this portfolio page we want the images budding up against the sides of the page. 

Now we are going to use CSS Grid. It has a lot of similarities to flexbox, it also a tool directly built into CSS and gives you the ability to align items. 

## The teacher Jordan Hudgens says his rule of thumb is to do his layouts in Grid and to build out the small eelements like a nav bar in flexbox. 

To apply the grid system to the whole page we have to select the container clas div. There's just one and everything in this page is within this div tag. 

So I type .container {} and give it: 
display: grid; and grid-template-columns: 1fr;

This is telling that I want the container to use grid and then I want to create these template columns using 1fr, which stands for fraction units. That means that our entire layout is going to be considered as having columns. 

1fr means 100%, I want the column to take up 100% of the page; in this case I want the nav bar column to go from end to end. 

Our portfolio items should go from end to end. 

Just like Flexbox was able to take those div elements and separate them out, Grid does the same thing. And when I say 1fr that means a hundred percent. I want you to take up one fractional unit, which menas this column of the nav bar should go from end to end. Just like our portfolio items should go from end to end. So everything we add below the nav bar is going to be considered in that next row down below; and that's all the styles we need to add to our container class. 


--------------------------------------------------------------------------------

8. Now we are goint to style the portfolio styles

By first we can first write a comment identifying the master styles, nav styles and portfolio styles. This I can reference this comments to guide myself when looking where to make changes into my css stylesheet.  

Since we already worked the nav bar we are going to work out that div class, so we check our nav-wrapper and we are going to do the same thing for the portfolio items. So I look where is the closing div tag for the nav-wrapper div class and after that closing tag I create a div class:
content-wrapper, and inside this I will create another wrapper called portfolio-items-wrapper, and inside this wrapper I will create wrapper called portfolio-item-wrapper. 

The class content wrapper is everything below the nav bar, then tghe portfolio items-wrapper this is what stores the collection of all the portfolio items, then inside that we area going to have the portfolio-item-wrapper (item in singular), and this will hold a single one item. 

So now inside the portfolio-item-wrapper I will create a portfolio-img-background div class. 

The names declaration helps us to be consistent and give meaningful names to our classes, and this last class will have an image as its background. I will also add an inline style to that one div class or portfolio-image-background and that is style="background-image:url(images/portfolio1.jpg)" (this is a css snippet that has a path to the iamge that I want to grab)

This image is not gonna show up yet because we have not given it height yet, but we can go to the html dev tools inspector to make it is there. And indeed it is.

The image didnt show up is because we are going to do a little trick. Because if you notice that we have text that is layered on top of the image and this cool little animation and its fading, and that is something that HTML and CSS right off the box really does not do, so we nee to have a way of implementing that kind of style, so the way we did it is creating a div and it's only job is to have an image and to have that image as it's background. 

Now we area gonna have the text in a completely separate div so lets add that part now. 

Now I make sure I am outside of that last portfolio-img-background but still inside the portfolio-item-wrapper.
And create a div class:
image-text-wrapper and inside this wrapper I create another wrapper to manage the logo, so will call it as logo-wrapper. And inside of this last div I am gonna have the image. 

There are two ways of working with images with HTML and CSS: the first is when you want a background image then you use straight CSS code with a call to a URL of wherever it's at, just like we area using it at this div: 
<div class="portfolio-img-background" style="background-image:url(images/portfolio1.jpg)">

If you see here the image is used by adding an inline style attribute to the div html tag with a portfolio-imag-background div class.

But if I am using images inside my html then I want to use the IMG tag and pass in the src attribute which is short for source and then I pass in the path. 

So for the first one is: 
<img src="images/logos/crondose.png> 

And make sure you dont have any spelling mistakes or anyting like that or else it will find find the image. 

And so that is going to be the logo wrapper and below that img tag outside the logo-wrapper div but inside the image-text-wrapper div is going to be the subtitle class:
and then type text into it. in my case was: I built this o 2017.


Now i can go ahead and copy from the singular portfolio.item-wrapper div class and copy until it's closing tag and paste it eleven times. 

And then I am going to call the appropriate logos. 


--------------------------------------------------------------------------------


9. now is time to style the portfolio items

So I go to the stylesheet at the bottom where a have a comment titled: Portfolio Styles and start adding the styles.

First I add a the grid value to the class .portfolio-items-wrapper. I am adding Grid to this container that holds all my portfolio items.

.portfolio-items-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
}

And then grid-template-columns 1fr 1fr 1fr ... so what this is means is that there's going to be  three columns and is going to give each one of them give each one of the columns their own full size column, one next to the other. 

And now I style class .portfolio-item-wrapper (the singular one) with position: relative;

What this is going to do is allow us to have some more more  flexibility with how we position each one of the items inside of it. 

Was already mentioned how behavior like this, like having text or images sitting on top of other images, is not allowed by default HTML and CSS for that kind of thing, so we are gonna have to force that to happen. 

The first step is by adding a position relative on the item (singular) wrapper and then we are going to style that iamge background so I do: portfolio-img-background {
    height: 300px;
    width: 100%;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

With a height of 350pixels and a width of 100%, that means the width will adjust automatically relative to the picture height.

What the  background-size of cover does, is imagine a scenario in which you have images that are not all the same size (which is our case in this project), then we want to make sure that  we are cropping the images in a way that they all sit nicely    
next to each other. Thats what this style rule does.

And then background-position: center; and background-repeat: no-repeat; 

This is the reason why Hudgens set a background image on each one of those elements and why he used inline styles so instead of us putting all the images in image HTML elementds, the background images were put with a CSS inline style and the logo images with a regular img src HTML tag.


--------------------------------------------------------------------------------

10. now we need to work with the text 

If we take a look at the page right now, we area going to see that the text that corresponds to each image div element is sitting below the image, and that's the default behavior for HTML to handle this. 

Whenever you have two divs sitting next to each other, or below each other when you code, HTML is going to say: inside that div you just slide on right underneath and then is gonna continue on. 

But we are saying nope, I want to position the html right on top of this other div.

So the way we do that is first by selecting it with: 

.image-text-wrapper {
    position: absolute;
    top: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    text-align: center;
    padding-left: 100px;
    padding-right: 100px;
}

IMP
- one key thing to note here: 
position relative is required if you want to have any position absolute element nested isndie of it. So that's why we have position realtive in .portfolio-item-wrapper and position absolute in image-text-wrapper which happens to be a child element of portfolio-item-wrapper.

Position aboslute is saying we are forcing this element someplace where it usually is not there, and in other to do that it has to have a parent element that has a relative position. 

We are saying that this image text wrapper is going to be positioned at the very top (top: 0), then inside of it we are going to use flexbox (display: flex and flex-direction: column) we area going to center the content with justify: center and align-items: center; 

justify-contents aligns from the sides right to left and align-items aligns them from top to bottom

We want it to take the full parent height the full 100% percent height: 100%

And all other text to be centered, with the padding, etc 


--------------------------------------------------------------------------------

11. now the logos, and target those with 
.logo-wrapper img {
    width: 50%;
    margin-bottom: 20px;
}



--------------------------------------------------------------------------------

12. we are now going to the part into where we are adding that dark fade animation, in whcih when I hover my cursor on top of any portfolio item the background photo darkens and the subtitles appear THIS WILL REQUIRE JAVASCRIPT 

So lets first do the colors and styles for this subtitles: 

.subtitle {
    font-weight: 600;
    color: lightseagreen;
}

font weight is used to bolden the text and color to color it

As it is the past rule technically works but we have to add a temporary note that says that "it needs to be more specific with selector" ... it is a note so that we dont forget to address it later ...



So now lets get those images get dark: 

So I am going to create a class: 
.img-darken {
    transition: 1s;
    filter: brightness(10%)
}

The transition will take 1 second and the brightness is set for 10%

This is not gonna work yet, because we have not called it or applied it anywhere in our HTML index file, but how it is going to work is we are gonna use it with our own special function.  

We are gonna have JavaScript dynamically add and remove this class when someone is hovering over it. 

This trick is possible to implement with CSS but it is tricky. 

Now we can go over the .subtitle class that had a note "this needs to ..." that we had and change it to: 

.image-text-wrapper:hover .subtitle {
    font-weight: 600;
    color: lightseagreen;
}

Now when I refresh this is working if the subtitle changes form black to seagreen when I hover over it. 

Now we have to add the start sort of state. So the text should be seen only when someone is hovering over the element, so lets remove the hover value and add the transition.

For this I create another rule that is the startig point, meaning when the text is not visible. So on top of (before of) of this rule:

.image-text-wrapper:hover .subtitle {
    font-weight: 600;
    color: lightseagreen;
}

I will create this other rule: 
.image-text-wrapper .subtitle {
    transition: 1s;
    color: transparent;
}

meaning that the transition take 1 second and the color of the text is transparent. 

And that is the starting state of this element.

If until now I refresh and check the transition I will see that the text jumps a little bit from size when it appears, and that is because at:

.image-text-wrapper .subtitle {
    transition: 1s;
    color: transparent;
}

we have not declared a font weight, whereas in:

.image-text-wrapper:hover .subtitle {
    font-weight: 600;
    color: lightseagreen;
}

we declared a font weight. SO what happens is when we hover over the image, the animation works well and the text appears, but it appear at one size and then jumps into another a little bigger size creating sort of like weird stange effect. And that is because ot start:
.image-text-wrapper .subtitle {
    transition: 1s;
    color: transparent;
}

the font weight was not included as part of the rules. So just have to add it to the same value as the end state

to if like this:
.image-text-wrapper .subtitle {
    font-weight: 600; 
    transition: 1s;
    color: transparent;
}



--------------------------------------------------------------------------------

13. now the JavaScript part 

JavaScript is always at the very bottom of the page, and the reason for that is because JavaScript works with selectors just like CSS do, but you would not like your JavaScript code to run before the entire page is loaded. 

So after the body closing tag we include a script tag.

And now we are going to select all the portfolio items on the page.  

So I open the console on my html doc. Here we area going to build a selector, so type: 
$('.portfolio-item-wrapper') and hit enter.

This will return: 
<div class="portfolio-item-wrapper"> with all its child elements

So that means that it got and pulls in the first element in the html doc page that corresponded to this class definition. This ultimately means that this is working properly.

This $('.portfolio-item-wrapper') syntax is different than the JavaScript syntax but this initial code snippet was to illustrate the power of JavaScript within the browser. 


So let's get started with javaScript: 

What we want to do is to store this portfolio item in a variable. 

So we type: 

const portfolioItems = document.querySelectorAll(.portfolio-item-wrapper)

I am saying, I want to find all the elements on the page that have that selector (.portfolio-item-wrapper) 

When I type this nothing gets returned but next if I type  portfolioItems (which is the name of the variable I just created), it will return a node list.

If I expand it I will it has a length of 12 and all the items are  actually inside this variable. So we are now sure this is working as it is supposed to, which is that it grab all the twelve elements. 

Event Listener
The same way we were sent to the hover state in CSS, we can do that in JavaScript as well. 

So for JavaScript you have be more explicit. 

So what we tried on the console, the whole const variable initialization, since we confirmed that it is working, we can go and grab it (copy it) and paste it in our html doc script tag. 


And now we want to loop over this. 

So I am going to add an event listener, so I type: 

portfolioItems.forEach()


- forEach is a callback function, meaning that it takes a function as an argument

- a function is just a process that runs

So we are saying: we want this process to run for each one of the portfolio items

We need to be explicit so we need to work with all of them. The portfolioItem inside the forEach paretheses is not anything in particular, it could be x, y or z. So the name portfolioItem is to be very explicit, it is just an iterator variable (a variable that will hold a different value each time an iteration is complete)

portfolioItems.forEach(portfolioItem => {

})

See the code above this text: so now everything inside the curly brackets is going to be run and applied on each of the portfolio items.


portfolioItems.forEach(portfolioItem => {
    portfolioItem.addEventListener('mouseover)
})

See the code above this text. Inside the curly braces I add 
portfolioItem.addEventListener('mouseover')

This means that as it iterating I can grab one single item and we can whatever we want with it. Just like we added our hover state in CSS here we dont call it hover, here is called a "mouseover" event. 

And the mouseover event, also takes a function:

portfolioItems.forEach(portfolioItem => {
    portfolioItem.addEventListener('mouseover, () => {

    })
})


Is exactly as when we declared the forEach function initially, but we passed an argument which was the arrow function portfolioItem => { }. But here we do not have any argument so we are just running whats called an anonymous function. We are saying just go and run this process. 

Here we can console log it to see if it works: 

portfolioItems.forEach(portfolioItem => {
            portfolioItem.addEventListener('mouseover', () => {
                console.log(portfolioItem);
            })
        })

Now when I paste this into my html script tag element and I go into the page with the console open, each time I hover over a portfolio item it logs the info of this portfolio item on the console and if I expand it logged item it gives me exactly the details of this item, the entire div. This corroborates that my forEach function is working properly.

Remember we are doing this because we want to add the darken class thing to each portfolio item whenever someone hovers (mouseover) that particular portfolioItem. So now that we got access to this items thru this forEach add listener process, lets do it.

What we are doing here is we are taking that html object of that div and those classes and we area using JavaScript to manipulate them. 

But lets first use console.log again but with portfolioItem and childNode. 
When I console logged before with portfolioItem, this gives us a lot of data, the full div but we only want one of the items here, and this childNode method does that.  

portfolioItems.forEach(portfolioItem => {
            portfolioItem.addEventListener('mouseover', () => {
                console.log(portfolioItem.childNodes):
            })
        })


With the childNodes, what that means if you remember we had those child nodes we saw at the console. They are nested divs, and with this childNodes, we can have them come out. So we can console log them to see them. 

When I do so now when I hover over any portfolioItem in the console I can see each portfolio item aI hover over will return me an item called: nodelist(5),  and when I expand it, it looks like an array, a colelction of data. For each portfolioItem there's an array, and we have indices, the first one is text, but we want the data contained in the second index (1:div.portfolio-img-background) so when I expand this one I can see the info:
<div class="portfolio ......>

This is the portfolio-img-background that I want to manipulate and it is index 1, and it is the one that I want to grab, so and I am going to add the method classList and log it to see what happens. 

Now I see a DOMTokenList each time a hover over a portfolio item. 

Notice how we have traversed this entire element:
we first started of bu grabbing them all, then we narrowed it down, filtered down until we got the exact div we wanted, and then from there we filtered it down even more, and we said just give me the class list. 

And so now that we have all of that I can just leave the console.log there for a moment and add a method add with the image darken class like this: 

portfolioItems.forEach(portfolioItem => {
            portfolioItem.addEventListener('mouseover', () => {
                console.log(portfolioItem.childNodes[1].classList);
                portfolioItem.childNodes[1].classList.add('img-darken');
            })
        })
and hit refresh and go to the page to see if the darken animation effect takes place and it is working 

However the images are staying dark. and that's because we need to add one more eventListener. So I go and copy the whole eventlistener code block and edit it like this: 

Instead of adding another mouseover event, we change it to mouseout, and instead of class list add we change to class list remove. AN remove all the consolelog statements on both as they are no longer needed.  

portfolioItems.forEach(portfolioItem => {
            portfolioItem.addEventListener('mouseover', () => {
                portfolioItem.childNodes[1].classList.add('img-darken');
            })

            portfolioItem.addEventListener('mouseout', () => {
                portfolioItem.childNodes[1].classList.remove('img-darken');
            })
        })




Running all these consolelogging contantly, and run these debugging steps and processes, to check and see all the values that over there verify the data. Because as long as we know the values I will not get stuck. One of the biggest challenges is not knowing enough about the data thats when we run into bugs. So try to always listen and watch what the data is telling you.    

Up until now, I know not only how to work with animations and all kinds of styles like that, and create my layouts, I also now know how to traverse the entire DOM, all of this HTML nodes, and to apply dynamic styles based on the user behavior. 























    



