### Ordering Question ###

#### Overview ####
This question gives students points when they put items in order.

In addition, this problem has a version that is accessible to blind and partially sighted users who are employing a screen reader.

Student state is recorded via Logger.log() when a grade is calculated, but not at other times.

#### Creating Your Own Ordering Problems ####

Here's how to adapt this example to create your own ordering problems.

1. Come up with the items.
2. Find images or write text (full HTML ok) for the items. Consider front-loading the text of your items so that students hear the most important or identifiable parts of them first when using a screen reader.
3. Download the files used in this problem.
4. Update the Ordering\_Elements.js file. Fill in the 'type' property with either 'text' or 'image', and fill in the according property with the image's filename or with your text. The text field is used as alt text for images.
5. Upload all your images and files to the "Files and Uploads" section of Studio, or just dump them in the proper directory if you're using the XML approach.
6. Create a new Custom Javascript Display and Input problem (under the "Advanced" problem tab). Copy and paste the contents of Ordering.xml into that problem, fix up the `right_answer` variable so that it contains the answer you want, and add your own instructions for the students.
7. Get the python library from  [https://github.com/Colin-Fredericks/hx-py](https://github.com/Colin-Fredericks/hx-py). Download the zipped version, and upload it (still zipped) into Files & Uploads.
8. Use your browser's javascript console for debugging - for instance, if your cards' text or images aren't showing up, it may point you to the line in your Ordering\_Elements.js file that is causing the problem.

##### Using Multiple Matching Problems #####

If you have multiple ordering problems in your course, you need to have different Ordering\_Element files for each one. You will need to number or name them differently, and update the link in the HTML page.

#### Files: ####

Inside you will find many pieces used to create this problem:

- `jschannel.js`: the javascript file that allows javascript-type problems to work at all. You should not need to change this. I didn't make this one.
- `underscore.js`: This does some nice array equality checking for us. You should not need to change this. I didn't make this one.
- `jquery.ui.touch-punch.min.js`: [Touch Punch](https://github.com/furf/jquery-ui-touch-punch), an awesome JQuery extension that maps touch events into mouse events. Used for mobile compatibility. Should not need to alter.
- `Ordering.js`: the javascript file that does the majority of the work and allows you to drag items around and stuff. You should not need to change this.
- `Ordering.css`: the css file that makes things look pretty (or as close as I could get them). You should not need to change this.
- `Ordering.html`: the HTML file that will be iframed into the page. If you have more than one ordering problem in your course, you will need to point this at the correct \_Elements file.
- `Ordering.xml`: the XML used to create the problem within Studio. You will need to make changes to this: updating `right_answer` to be the actual right answer you want, pointing it at the right .html file, and filling it with your own instruction text. You can also turn partial credit and feedback off if you prefer; just set them to False.
- `Ordering_Elements.js`: holds the item and ordering names. You will need to update this to have the items you want.

When creating your own matching problem, you will upload almost every file in this directory to the Files and Uploads section. There are two exceptions: the XML file (which you cut-and-paste into Studio) and the image files (which you replace with your own).
