# simple-terminal
Simple dumb-terminal prototype

```lisp
(defvar *theme*
  (xterm::{new}  "background" "black"
          "foreground" "green"
          "cursor" "yellow"))

(defvar *options*
  (xterm::{new} :rows 20
         :cols 132
         :theme *theme*
         "fontSize" 13
         "rightClickSelectsWord" t
         "rendererType" "canvas"
         "fontFamily" "consolas"))

(xterm:make-terminal *options*)
(xterm:term.open "terminal")
(format xterm:stdout "~%Hello ~%")
(xterm:cursor.position 10 30)
(xterm:term.write "Hello")
(xterm:term.write #\Newline)
(xterm:term.write #\Newline)
(xterm:term.write (code-char 13))
```

Better to launch with Chromium. 

Have a fun


  