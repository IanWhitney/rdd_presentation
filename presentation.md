This is a story of how I wrote a gem.


Ok, that's not very exciting.


This is the story about how I wrote a gem without knowing the
implementation, the API or even what clever name I would give it.


Still needs some excitement.


Let's say there were ninja pirates attacking me as I worked.


The gem I wrote is unimportant. The problem I faced when writing it is
more universal. I more or less knew what the end result of the gem had
to be, but I didn't know:


- the API
- the features
- the implementation


Remembering an idea I heard on Ruby Rogues (epsiode #44), I decided to
try Readme Driven Development. 


Before I wrote any code, I would write the Readme. 


Then I would implement tests that assert the Readme is
correct. 


Then I would write code that passes the tests.


"Writing a Readme is absolutely essential to writing good software. Until you've written about your software, you have no idea what you'll be coding." - Tom Preston-Werner


Ok, so what am I writing about?


### The readme should:
  - Explain what the gem does
  - Installation & Configuration
  - Examples of use
  - API documentation


So, I have a full documented spec of my application before I write any
code? Wait, this sounds familiar.


## BDUF
<img src="http://images-mediawiki-sites.thefullwiki.org/09/3/1/6/40424692559461574.png">


We've heaped so much scorn on BDUF that we've forgotten what was
terrible about it and what actually had some value:


### The Terrible:
  - Wrangling with Product Managers and Stakeholders through endless
    meetings
  - The huge hassle of changing a spec that had been approved


### The Value:
  - The optimism of a clean design, unsullied by actual code
  - The greater understanding of a problem that can come from writing in
    natural language
  - Spotting API or implementation problems before you have a bunch of
    libraries that do it wrong.


Ditch the terrible, keep the good. 


Describe a gem that would make you happy.
<aside class='notes'>Writing a Readme lets you document the working of a tool the way you **want** it to work. No
worrying about implementation, technology or timelines. Make the best
API you can.</aside>


I already had the start of a design, but it didn't make me happy:

  - Fiddly
  - Required a lot of objects serialzed into hashes


Keeping only my end requirements in mind, I wrote a Readme that
functionality in a way I found pleasing:

  - Easy to configure
  - No hashes
  - Metaprogramming the behavior I wanted into an object
  - Simple form helpers for easy display, keeping Rails helpers if I need more complex behavior.


Great! Now if I only knew how to make that happen.


The unfettered freedom of natural language gives you more than enough rope to hang yourself.


## Prevent accidental hangings:
  * YAGNI
  * Focused gem functionality
  * Stay within the possible


### Use that rope for something good


![alt text](http://www.backachersranch.com/images/girl_with_lasso.png "Title")
<aside class='notes'>Describing a feature you want, but don't quite now
how to implement lets you learn a new technique. Starting with code, or
even tests first can lead you towards familiar implementations and
stagnation.</aside>


My inital README was wrong in a lot of ways. That's fine. The syntax
doesn't need to be perfect. It's a guide, not a railroad track.


Just don't forget to update your readme as you go.


  1. Document feature
  2. Test feature
  3. Implement feature
  4. Goto 1 and revise


Writing is Rewriting


Works great even for features you're not sure you want:
<aside class='notes'>My inital intent was to do all configuration through yaml. Co-worker
suggested also doing class-level macros. I went along with that and
documented it. After documenting it, I realized the data structure was
exactly the same, so implementing both would be a snap and might make
the gem more useful. That's a win.</aside>


## Getting really jiggy with it
https://github.com/avdi/keyword_params


### When to use it:
  - Small gems
  - Greenfield work


### Less Good Situations:
  - Huge applications
  - A replacement for existing API


### The accolades:
    The README is top notch.  Really.  
    - James Edward Gray II


## Thanks
  - GitHub: IanWhitney
  - Twitter: iwhitney
  - The Gem: hstore_radio_buttons
