## Getting Started ##

Installation instructions can be found on the [GNU website](http://www.gnu.org/software/emacs/#Obtaining). If you run Mac OSX, you will find that Emacs is already installed. For Linux, Emacs can be installed with the default package manager. For instance, with Arch Linux: `sudo pacman -S emacs`

## Emacs Basics ##

  * `C-` is the control key pressed in junction with another key
  * `M-` is the meta key or option key pressed in junction with another key

> ### Movement ###
    * `C-v`: Move down a page
    * `M-v`: Move up a page
    * `C-l`: Center page on cursor
    * Arrow keys are applicable here, but these shortcuts are generally faster
      * `C-f`: Move cursor 'forward' one character
      * `C-b`: Move cursor 'backward' one character
      * `C-n`: Move cursor to the 'next' line
      * `C-p`: Move cursor to the 'previous' line
    * `M-f`: Move cursor to end of next word
    * `M-b`: Move cursor to beginning of previous word
    * `C-a`: Move cursor to beginning of line
    * `C-e`: Move cursor to 'end' of line
    * `M-a`: Move cursor to end of sentence
    * `M-e`: Move cursor to beginning of sentence
> ### Buffer Commands ###
    * `C-g`: Cancel mini-buffer
    * `C-x C-f`: Open/Create file
    * `C-x C-s`: Save current Buffer
    * `C-x 1`: Close all other buffers except current
    * `C-x 2`: Splits buffer vertically
    * `C-x 3`: Splits buffer horizontally
    * `C-x o`: Switches to next buffer
> ### Text Manipulation ###
    * `Backspace`: Deletes the character before the cursor
    * `M-Backspace`: Deletes the word before the cursor
    * `C-d`: Deletes the character after the cursor
    * `M-d`: Deletes the word after the cursor
    * `C-k`: 'Kills' the string in front of the cursor and stores it in the clipboard
    * `M-k`: 'Kills' the rest of the sentence the cursor is in and stores it in the clipboard
    * `C-space`: Sets marker at cursor position
    * `C-w`: 'Wipes' the text from the marker to the cursor and stores it in the clipboard
    * `Esc-w`: Copies the text from the marker to the cursor and stores it in the clipboard
    * `C-y`: 'Yanks' the text from the clipboard and pastes it at the cursor
    * `C-_`: 'und'oes the previous command
> ### GUI Management ###
    * `C-x 1`: Closes all windows except current
    * `C-x 2`: Creates a window below the current
    * `C-x 3`: Creates a window to the right of the current
    * `C-x o`: Switches to 'other' window
> ### Exiting Emacs ###
    * `C-z`: Pauses Emacs, and places it into the background
      * You can resume Emacs by entering `fg` (foreground) into terminal
    * `C-x C-c`: Quit Emacs
> ### Miscellaneous ###
    * `M-x tetris`: Starts Tetris