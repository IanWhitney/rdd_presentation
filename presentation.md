This is a story of how I wrote a gem.


Ok, that's not very exciting.


This is the story about how I wrote a gem without knowing the
implementation, the API or even what clever name I would give it.


Still needs some excitement.


Let's say there were ninja pirates attacking me as I worked.


The gem I wrote is unimportant. The problem I faced when writing it is
more universal. I more or less knew what the end result of the gem had
to be, but...


I didn't know:
- the API
- the features
- the implementation


Remembering an idea I heard on Ruby Rogues (epsiode #44), I decided to
try Readme Driven Development. Before I wrote any code, I would write
the Readme. Then I would implement tests that assert the Readme is
correct. Then I would write code that passes the tests.


History


Readme Driven Development is not a new idea. Like most programming
techniques, it crops up again and again under new names:


2010

Tom Preston-Werner writes the RDD blog post:

"Writing a Readme is absolutely essential to writing good software. Until you've written about your software, you have no idea what you'll be coding."



1984

Donald E. Knuth's _Literate Programming_, in which a natural-language
file could generate a working program.


http://docs.python.org/2/library/doctest.html
http://coffeescript.org/#literate


1971

UNIX introduces man pages, which were initially written after
implementation. I can't prove it, but surely someone wrote a man page before writing the program. If they had blogs, they would have blogged about it.


Thanks to GitHub (co-founded by Tom Preston-Werner, he of the RDD blog
post), Readmes are more important that ever, they are how programmers
for years will learn about your code.


Ok, how does this work


Before writing code, before writing tests, document how your application
will work.


Now the document is done you can write tests that assert your
documentation is true, then write code that gets the tests to pass.


So, I have a full documented spec of my application before I write any
code? Wait, this sounds familiar.


BDUF


We've heaped so much scorn on BDUF that we've forgotten what was
terrible about it and what actually had some value:


The Terrible:
  - Wrangling with Product Managers and Stakeholders through endless
    meetings
  - The huge hassle of changing a spec that had been signed off on


The Value:
  - The optimism of a clean design, unfettered be actual code
  - The greater understanding of a problem that can come from writing
  - Spotting API or implementation problems before you have a bunch of
    libraries that do it wrong.


So, ditch the terrible, keep the good. Writing a Readme lets you
document the working of a tool the way you **want** it to work. No
worrying about implementation, technology or timelines. Make the best
API you can. Describe a gem that would make you happy.


I had a Rails gem to write, so I needed to document how it would be
configured and used:

Configuration sample


Use Sample


Now, here's where I hit a speedbump. I had no idea how to implement
this. I knew it was what I wanted, but I didn't know how to get from
point A to B.


Yet.


The exact details of how I implemented this aren't important. All that
matters is that I did, kind of.


My inital README was wrong in a lot of ways. That's fine. The syntax
doesn't need to be perfect. It's a guide, not a railroad track.


Some wrongness


Some more wrongnesss


And, for me at least, documenting features in this way makes other
things more clear.


My inital intent was to do all configuration through yaml. Co-worker
suggested also doing class-level macros. I went along with that and
documented it. After documenting it, I realized the data structure was
exactly the same, so implementing both would be a snap and might make
the gem more useful. That's a win.


Adding new features:
  - Document
  - Test
  - Implement


Getting really jiggy with it

https://github.com/avdi/keyword_params


When to use it:
  - Small gems
  - Greenfield work


Bad situations:
  - Huge applications
  - A replacement for existing API


The accolades:
  The README is top notch.  Really. - James Edward Gray II


Thanks
  - GitHub: IanWhitney
  - Twitter: iwhitney
  - The Gem: hstore_radio_buttons
