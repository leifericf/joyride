# Joyride Examples

Demonstrating some ways to [Joyride VS Code](https://marketplace.visualstudio.com/items?itemName=betterthantomorrow.joyride).

<img src="../assets/joyride-logo.header.png" width=500></img>

In the `.joyride/scripts` folder you'll find mostly small examples:

## Create a Webview

`webview/example.cljs`

Create a Webview. Uses [scittle](https://babashka.org/scittle/) + [reagent](https://github.com/reagent-project/reagent) for the contents of the webview.

Live demo here: https://twitter.com/borkdude/status/1519607386218053632

## Terminal

`.joyride/scripts/terminal.cljs`

Create a Terminal, send text to it and show it.

![](../assets/joyride-demo-terminal.gif)

## Fontsize

`.joyride/scripts/fontsize.cljs`

Manipulates the editor font size.

Live demo: https://twitter.com/borkdude/status/1519709769157775360

## Structural Editing

`.joyride/scripts/ignore_form.cljs`

Adds a command for ignoring out (Clojure-wise) the current enclosing form. Depends on that the [Calva](calva.io) extension is installed, because it is what helps us find out of the current list in order to insert the ignore tag (`#_`).

* Video here: https://www.youtube.com/watch?v=V1oTf-1EchU
* Tweet to like/comment/retweet: https://twitter.com/pappapez/status/1519825664177807363