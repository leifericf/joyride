# Take VSCode on a Joyride!

<img src="assets/joyride.png" height=300></img>


Modify your editor by executing ClojureScript code in your REPL adn/or run scripts via keyboard shortcuts you choose. The Visual Studio Code API is at your command!

Joyride is Powered by [SCI](https://github.com/babashka/sci) (Small Clojure Interpreter).

## WIP

You are entering a construction yard. Your feedback is highly welcome!

## Quickstart

Create a script in your workspace under `.joyride/scripts`, e.g. `example.cljs`:

``` clojure
(ns example
  (:require ["fs" :as fs]
            ["path" :as path]
            ["vscode" :as vscode]
            [clojure.string :as str]))

(defn info [& xs]
  (vscode/window.showInformationMessage (str/join " " xs)))

(info "The root path of this workspace:" vscode/workspace.rootPath)

(fs/writeFileSync (path/resolve vscode/workspace.rootPath "test.txt") "written!")
```

This script gives one information message and writes to a file `test.txt` in
your workspace.

Then in your keyboard shortcuts, add:

``` json
 {
        "key": "cmd+1",
        "command": "joyride.runWorkspaceScript",
        "args": "example.cljs"
 }
```

Now you can run the `example.cljs` script by just hitting Cmd+1!

See [doc/configuration.md](https://github.com/BetterThanTomorrow/joyride/blob/master/doc/configuration.md) for full configuration options

## There's a REPL server

While developing Joyride scripts you should of course do it leveraging Interactive Programming (see [this video](https://www.youtube.com/watch?v=d0K1oaFGvuQ) demonstrating it). Here are the steps:

1. Issue the command <kbd>**Joyride: Start nREPL**</kbd>. This will start Joyride's nREPL server.
2. Connect your Clojure editor (we suggest [Calva](https://calva.io) for super biased reasons.)
3. Open a script (presumeably in the `.joyride/scripts` folder)
4. Hack away!

## Support and feedback

You'll find us in the `#joyride` channel on the [Clojurians Slack](http://clojurians.net)

## News

### Twitter

Follow the [#vsjoyride](https://twitter.com/search?q=%23vsjoyride&src=typed_query&f=live) hashtag on Twitter!
