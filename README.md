# Polmer in Meteor

It took me ages to figure out how to get the Polymer elements into a Meteor app.  Here's how I did.  There are almost certainly much better ways to do this.  If someone thinks this is terrible or knows one of those better methods, please let me know.

## Credits
Most of this is forked from https://github.com/pixto

## How To

```
meteor create polymer-test
cd polymer-test
mkdir packages
```

I put the polymer git repos in <meteor_project>/packages so I didn't have to bother with the Atmosphere stuff.  This is probably bad, but it works.  For this project:

```
cd packages
git clone git@github.com:stephenwilley/polymer-installer.git stephenwilley:polymer-installer
git clone git@github.com:stephenwilley/polymer-iron-elements.git stephenwilley:polymer-iron-elements
git clone git@github.com:stephenwilley/polymer-paper-elements.git stephenwilley:polymer-paper-elements
cd ..
meteor add stephenwilley:polymer-installer
meteor add stephenwilley:polymer-iron-elements
meteor add stephenwilley:polymer-paper-elements
```

Then I modified the client/main.html to include the link refs and paper-fab element.  Have a look at the one in this repo.
Next, I modified client/main.js to watch the paper-fab for clicks instead of the regular button.

Once those mods are done, just run it with:

```
meteor run
```

Hope it helps.  Any problems getting it to work, create an Issue and I'll try my best to answer.
