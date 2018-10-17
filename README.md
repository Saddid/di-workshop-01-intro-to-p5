# Workshop 1: Introducing JavaScript with P5.js

Collaborators: [your github username] & [your partners github username]

Make sure you’re working in pairs - on a single laptop. You’ll be **pair
programming**. In pair programming, there are two roles - **driver** and
**navigator**.

The **driver** is at the keyboard. They’re responsible for typing and figuring
out syntax. They shouldn’t make decisions though! That’s the responsibility of
the **navigator**. They make decisions, and ask the driver to implement them.

Start by forking this repo:
![fork button](https://readme-pics.s3.amazonaws.com/fork_button.jpg)

Forking creates a copy of this repo in your own GitHub account. Add your partner
as a collaborator by going to 'Settings' > 'Collaborators & teams' and entering
their GitHub username in the 'Collaborators' box. That means you'll both have
access to the repo.

You should now have a copy of this git repository in your own github account.
Now, we need to get a copy on our own laptop for us to work with. Start by
opening a terminal and creating a projects/ada folder if you don't already have
one:

```sh
cd Desktop
mkdir Projects
cd Projects
```

Next, we need to clone the repo. This copies all the files and history from
github to our own computer:

```sh
git clone https://github.com/<your github username>/di-workshop-01-intro-to-p5.git
cd di-workshop-01-intro-to-p5
```

You can see that it's a git repository and some of the history by running these
commands:

```sh
git status
git log
```

> **Note:** If you get stuck in `git log`, it's because you're in something
> called a pager. This is a really old bit of software from before computers
> could scroll in the way we're used to. You can move up and down in the pager
> with your arrow keys, and exit it by pressing `q`

Finally, we need to install some bits and pieces that in our new repo to finish
setting it up:

```sh
npm install
```

---

We’ll be working with some software called P5. P5 is a **JavaScript library**
for drawing shapes - it’s used for making simple games and cool generative art.

For each of the **bold** questions below:

<h3 align="center">
  🗣 Discuss &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  👩‍💻 Change &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  👀 Observe &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  🔄 Repeat
</h3>

1. **🗣 Discuss** the question with your partner
1. **👩‍💻 Change the code** - what do you expect your changes to do?
1. **👀 Observe the results** - what happened when you ran your code? How did it
   differ from your expectations
1. **🔄 Repeat** - keep discussing, changing, and running the code until you
   feel you understand it

**The aim of this workshop is _exploration_, hopefully leading to
_understanding_. It’s really important that you _take your time_. The questions
below are _guidelines_, meant to prompt your _curiosity_. If you can’t answer a
question, use a search engine or ask someone nearby. Don’t move on until you
_fully understand_ what’s happening.**

**Explore and have fun! Be curious!**

# Setup

Now you've got the repo cloned and installed, we need to start it up:

```sh
npm start
```

This runs a web server - a little program that your browser can connect to so
that the files you write in this project can run in there. Now, when you visit
http://localhost:5000/, you'll see all your files right there.

Open the workshop folder in your editor. In VSCode, choose File > Open and
select the folder - _not any of the files inside it_. You should see all the
workshop files in the left-hand file pane.

Open this file - README.md - in your editor. Make notes in here about everything
you do. If you don't know the answer to a question, it's your job to experiment
with the code to see what you can find out.

# Sketch A

Open the `part-a` sketch in your browser, and open `part-a/sketch.js` in your
editor. The code in `sketch.js` is what's running on the page. Every time you
make a change in `sketch.js`, you need to save the file (ctrl-S or cmd-S) and
refresh your web browser (ctrl-r or cmd-r) to see the change.

---

Look at these lines:

```js
var r = 255
var g = 80
var b = 0
```

**What might these lines do?**
it creates three variables and sets numbers 
**What happens if you change the numbers?**
the colour of the box changes
**What numbers are allowed / What numbers have an effect?**
Positive numbers up to 255
Look at this line:

```js
createCanvas(400, 400)
```

**What does createCanvas do?**
it determines the size of the shape
**What happens if you change the numbers?**
first number changes the width, second number changes the height
**What numbers are allowed/what numbers have an effect?**
Negative numbers make the shape disappear, but you can use any positive number
**What happens if you add/remove a number?**
removing a number gets rid of the shape, adding a numbe changes nothing

**Can you guess what the `function setup() {` part does? What happens if you
change the name of setup?** 

Look at this line:

```js
background(r, g, b)
```

**What does background do?**
The background sets the colour of the shape according to the values stored in the variables r,g and b.

**What happens if you change the order of the letters in background? What does
this tell you about how the computer uses them?**
This will change the colour. The computer does not associate a variable name with a type of input, so it just takes it in standard rgb order. 
**What happens if you change the number of letters?**
The colour of the box turns grey
**What happens if you change the letters for different ones?**
It gets rid of the box because there is no variables set up unde rthe new letters. The letters of the variables can be changed and not make any difference.
# Sketch B

Open the `part-b` sketch in your browser, and open `part-b/sketch.js` in your
editor.

Read the code and play with the sketch in your browser.

> **Note**: There's two main sections in the code - the bit called `setup` and
> the bit called `draw`. The code in the `setup` section runs **once**, when
> your program first starts up. The code in the `draw` section runs again and
> again and again - 60 times every second.

Look at these lines:

```js
function setup() {
  createCanvas(400, 400)
  background(0, 0, 0)
}
```

**What does setup do?**

**What do `{` `}` mean? What happens if you remove one?**
The Square dissapears. 
**What do the numbers in `background(0, 0, 0)` do? What happens when you change
them? How is this different from Sketch A?**

Now look at these lines:

```js
function draw() {
  fill(255, 0, 0)
  ellipse(mouseX, mouseY, 30, 30)
}
```

**What does draw do?**

Now look at:

```js
fill(255, 0, 0)
```

**What do these numbers do? What happens when you change them?**
changes the colour of the circles
**What does fill mean? What happens if you change it to stroke?**
the colours in fill set the colour of the whole circle, whereas with stroke, it sets the colour of the outline.
**What happens if you remove (or comment out) this line? What about if you
include both fill and stroke on seperate lines?**
if yo include both on different lines it sets the fill colour and the outline colour
Now look at this line:

```js
ellipse(mouseX, mouseY, 30, 30)
```

**What does `ellipse` do?**
 creates a shape at your current mouse position with a height and width as specified in the parentesis
**What happens if you change the numbers?**
it changed the shape of the circle. You can make it taller or fatter (oval)
**What do `mouseX` and `mouseY` mean?**
It is the mouse position X and Y value as if the canvas shape is a table/grid 
**What happens if you change the order of the items between the `(` `)`?**

---

**What happens if you add `background(0)` after `draw() {`? Why?**

Replace the ellipse with a triangle. Use https://p5js.org/reference/ (the 2D
primitives section) to help.

Play around with the sketch - how else can you change it?

# Sketch C

Open the `part-c` sketch in your browser, and open `part-c/sketch.js` in your
editor.

Read the code, then play with the sketch and observe what happens - try clicking
the mouse on the sketch.

Look at:

```js
if (mouseIsPressed) {
  fill(255, 0, 0)
} else {
  fill(0, 255, 0)
}
```

**What does `mouseIsPressed` mean?**
When the left button is clicked. 
**What happens if you change `mouseIsPressed` to `keyIsPressed`?** 
it changes the control to a key, so you can press any key to change the colour.
You’ll need
to click on the sketch so it registers keyboard events – use the ctrl key if you
have issues with the keyboard.

**What does if / else do?**
this gives the code a pathway
**What happens if you remove the { } or ( )? Why?**
the code doesnt work 
**What happens if you change 255 to mouseX ? Why?**

**Remove the outline of the circle. Use Google and the P5.js reference to help
you.**

# Challenge

In your pairs, take the code in sketch c and adapt it into a simple paint
program. The user should be able

- click and drag to paint on the screen
- press keys on the keyboard to choose a colour
  - e.g. pressing ‘r’ changes the paint colour to red, pressing ‘g’ changes the
    paint colour to green.

Use this code as a starting point:

```js
if (keyIsPressed) {
  if (key == 'r') {
    // set paint colour to red
  }
  if (key == 'g') {
    // set paint colour to green
  }
  // add more keys/colours
}
```

**Document your process in this file.**

## Extension

- Change the shape of the brush (explore other shapes like squares or triangles)
  based on a key pressed
- Change the size of the brush based on a key pressed.
