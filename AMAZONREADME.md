# Activity: Click Handlers #

For this activity, you will be creating an interactive web page that gets updated or modified when various buttons are clicked. 

 - Begin by creating a project folder called `js_click_handlers`
 - add an `index.html` file to the project
 - Open that project in VS Code
 - Add the following as the contents of index.html
 
```html

<!DOCTYPE html>
<html>
    <head>
        <title>An interactive web page</title>
        <style>
            #color_box { width: 200px; height: 200px; }
            .gray { background: gray; }
            .blue { background: rgb(67, 111, 255); }
            .pink { background: pink; }
        </style>
    </head>
    <body>
        <h1>An interactive web page</h1>

        <h2>1. Color changer</h2>
        <button id="gray_button">Gray</button>
        <button id="blue_button">Blue</button>
        <div id="color_box" class="gray"></div>        
        <script>
            const color_box = document.getElementById("color_box");
            
            const gray_button = document.getElementById("gray_button");
            gray_button.onclick = function() {
                color_box.className = "gray";
            };
            
            const blue_button = document.getElementById("blue_button");
            blue_button.onclick = function () {
                color_box.className = "blue";
            };

            /* TODO 1
             *
             * Add a third button (and the associated event handler)
             * to support an additional color: pink
             */
        </script>

        <hr>

        <h2>2. Counter</h2>
        <button id="counter_button">This fabulous button</button>
        has been clicked <span id="countspan">0</span> times.
        <script>
            let count = 0;
            const countspan = document.getElementById("countspan");
            
            const counter_button = document.getElementById("counter_button");
            counter_button.onclick = function() {
                /* TODO 2
                 *
                 * Fill in this function so that it increments
                 * (adds one to) the variable named count,
                 * then updates the text content of "countspan"
                 * to show the current value of "count".
                 */
            }
        </script>

        <hr>

        <h2>3. Even or Odd?</h2>
        <button id="even_or_odd_button">Is the count even or odd?</button>
        <script>
            const even_or_odd_button = document.getElementById("even_or_odd_button");
            even_or_odd_button.onclick = function() {
                /* TODO 3
                 *
                 * Fill in this function so that it shows an
                 * alert dialog stating whether the count
                 * (from part 2, above) is even or odd.
                 */
            }
        </script>
    </body>
</html>

```

If you open that file in your web browser, you will see three numbered sections.

Clicking on the "blue" and "gray" buttons in section 1 will change the color of the square. The other buttons on the page don't do anything ...yet.

There are three separate sections of JavaScript code embedded within the HTML, enclosed within `<script>` tags.

Inside each of those three sections of code, you will find a JavaScript comment specifying a "TODO".

Each TODO indicates a place where you need to write some additional JavaScript code in order to complete the functionality of the page. Complete all three of the TODOs.

* * *

![Edwin_the_duck.jpg](https://i.snag.gy/xZgaDe.jpg)

**Edwin the Duck Says:**
_In this exercise, the HTML, CSS, and JavaScript have all been combined together into a single file. That's OK for a small project like this. In general, though, it's a good practice to separate the markup, stylesheets, and scripts into independent files._

* * *

### Math Hint ###

Your reading introduced JavaScript's addition and multiplication operators, `+` and `*` respectively.

The third TODO will require you to figure out whether a number is even or odd.

To determine this, you will use JavaScript's modulus, or remainder, operator, `%`.

The modulus operator gives you the [remainder left over when one number is divided by another](https://www.mathsisfun.com/numbers/division-remainder.html).

In arithmetic, a number can be checked even or odd by checking the remainder of the division of the number by 2.

-	`3 % 2` = 1 _(hence 3 is odd)_
-	`4 % 2` = 0 _(hence 4 is even)_

### Programming hint ###

Make sure you understand the difference between JavaScript's assignment operator (which updates the value of a variable) and the equality operator (which returns true or false depending on whether two values are the same or not).

### Finishing up ###

Once you have completed all three TODOs, your index.html file should display five buttons, and clicking on any of those 
buttons should produce the desired behavior. Push your code into a GitHub repository. Please submit your GitHub for review (OPTIONAL)

