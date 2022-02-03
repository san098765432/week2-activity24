# week2-activity24

AIM:
 Add an icon next to every <a> element that has a link to a downloadable CSS file in its href attribute.

Insert the 📝 emoji after the link text.

It's done when the 📝 emoji is inserted using only CSS.

step 1: identify the <a> which limk to .css only as that is what we are targeting

step 2: every anchor tag within the ul '(unordered list)
you want the icon to be inserted AFTER the anchor tag and to follow AFTER the the link to .css which is why we specify the word AFTER in the CSS e.g. ul a:: after
the ::after is refered to as a pseudo element

step 3:copy and paste the icon in the brackets 
ul a::after {
  content: '📝 '

step 4: this is not specific enough however as the icon is paster besides every single link within the HTML including the nav bar, this needs to be more specific so it meets the acceptance criteria and is only inserted besides the <A> which links to a .css

step 5: use something called an ATTRIBUTE SELECTOR
a [ href$='.css']   -> the $ means you are asking CSS to insert the icon besides any <a> which contains anything '.css', it doesnt have to ONLY include .css e.g. href ='.css' it could be href = 'hellohellohello.css' anything which contains the phrase .css AT SOME POINT in its link, it isnt looking for an exact match
step 6:  using the $ sign is way to target multiple elements within the HTML which contain whatever you're looking for
step 7: if you want to target a specific line however, then you should use href= NOT href$=
href= is MORE SPECIFIC.
step8: essentially, href$ allows you to target a file by its extension etc 



TO INSERT THE ICON AFTER A LINK:
ul a::after {
  content: '📝 '






  TO INSERT THE ICON AFTER A ONLY THOSE ANCHOR TAGS WHICH CONTAIN A HREF (a link to something) :

a [href$= '.css'] :: after {
content: '📝 '
  }
 
 what are we targeting? Here, we are targeting anchor elements by including 'a' before the [href$].

 are we targeting ALL anchor elements? No.Bu inserting the [href$='.css'] we are going to insert the icon next to those anchor tags which contain the .css extension




 IF YOU WANT TO TARGET A SPECIFIC LINE (use a diff format):

 a [href="./assets/css/style.css"]  ->the icon is ONLY inserted after this, you do NOT use $ when you target something specifically.