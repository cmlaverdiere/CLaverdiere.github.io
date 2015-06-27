---
layout: post
title: Hey Emacs, You're pretty cool.
date: 2015-06-23 10:06:33
---

I used Vim religiously for around 3 years. I started using Emacs for most of my
tasks around 2 months ago. Luckily,
[evil-mode](http://www.emacswiki.org/emacs/Evil) for Emacs is nearly perfect, so
I could test drive Emacs without ever leaving the comfort of Vim.

Here's a quick overview of my experience:

- Emacs is slower. Still completely usable, but often not as responsive as I'm
  used to with Vim.

- The way Emacs integrates the shell, IRC, REPLs, and everything else feels easier
  to manage than several tmux sessions / panes.

- Manipulating text in any buffer is a bigger win than you might think.

- It is a major time investment to configure compared to Vim.

Let's see what else Emacs does that makes it so ballin.

**NOTE**: This is not a guide to switching to Emacs, just my observations on the
journey. If you're looking for one, use this
[migration guide](http://juanjoalvarez.net/es/detail/2014/sep/19/vim-emacsevil-chaotic-migration-guide/)

## LISP everywhere

You can evaluate an elisp expression in any buffer. For example:

{% highlight elisp %}
(insert (shell-command-to-string "date"))
{% endhighlight %}

This runs the `date` shell command and inserts the results into the buffer,
similar to Vim's `r!`.

This also lets us change the configuration of Emacs without restarting it (most
of the time). This is nice for someone who constantly changes their config.

## REPL integration

With Vim, we can whip up support for a Python or Haskell REPL using tools that
somewhat integrate (tmux + vim-slime is what I used). Emacs has support right
out of the box for this though, using functions of the family
`python-shell-send-x`, with support for buffers, regions, etc. No difficult
setup required, and it feels damn good.

## Everything is text

Working with shell output was always tedious, even with good tools like tmux. In
Emacs, we can move around any buffer with Vim bindings, and manipulate that text
in any way. It's very convenient.

## IDE features

*Projectile*, *helm*, and *irony* alone give a setup for my C/C++ projects that would
be difficult to get in Vim. Something like navigating the Linux kernel source
becomes a breeze.

## The bad

Emacs takes a lot more effort to setup than Vim. I've not yet become good enough
at elisp to add complex functionality to Emacs, but it feels so much better than
Vimscript hacks. Still, the Emacs learning curve is definitely higher than the
Vim one, and it will take a lot of effort to get a comfortable setup.

It's also noticeably slower.

## Am I done with Vim?

I still use Vim for quick access to files, and small edits. I've stopped trying
to turn Vim into an IDE, and have turned to Emacs for that, and it feels much
less like trying to fit a square peg through a round hole.

If anyone is a Vim user on the fence about learning Emacs, go for it, as
evil-mode is phenomenal. Regexes, ex / global commands, even cryptic insert mode
movement commands that nobody ever uses work. Give it a shot.
