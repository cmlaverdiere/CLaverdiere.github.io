---
layout: post
title: Transcribing music with cscribe
date: 2015-06-24 22:06:10
---

This summer I wanted to sharpen my music transcription skills on guitar (ie: not
looking at tabs for songs, but instead figuring them out by ear). There are
already a lot of good programs to help with transcribing
([Transcribe!](http://www.seventhstring.com/xscribe/overview.html) for example),
but I didn't feel like I needed the full feature set of a program like that. All
I wanted was to be able to load a song and

- Skip forward / backward by seconds
- Mark song sections and replay from marks
- Slow / speed up the tempo

Basically, all things something like *mplayer* does, but with an interface
focused on transcribing music. Using the mouse is frustrating when transcribing,
so it would have to have decent keybindings too.

So far, it's come pretty close to what I imagined. It's a simple ncurses tui
with vim keybindings for typical song actions (play, pause, mark, etc). The only
thing not yet implemented is the tempo changing.

Screenshots:

![cscribe main screen](/assets/cscribe/cscribe_main.png){: .center :}

And a list of keybindings:

![cscribe help screen](/assets/cscribe/cscribe_help.png){: .center :}

Source on [Github](https://github.com/CLaverdiere/cscribe)
