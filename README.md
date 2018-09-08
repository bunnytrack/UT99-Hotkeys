# UT99-Hotkeys
A collection of useful hotkeys (.cfg files) for Unreal Tournament

What is this repository?
------------------------
A place where people can contribute useful hotkeys (or other miscellaneous snippets) for Unreal Tournament.

What are hotkeys?
-----------------
A hotkey is a keyboard shortcut; a series of one or more commands which you assign to a single key on your keyboard. In UT, you may want a hotkey which switches between teams, for example.

How are hotkeys created in UT?
------------------------------
There are several ways to create hotkey commands in UT:

* **In-game**
  
  This method can only be used for relatively simple commands. Certain commands can be chained together, separated by a pipe character (`|`) although the limitations of this are unclear.
  
  1. Press `tab` (or open the in-game console)
  2. Type `set input X command` where `X` is your chosen key and `command` is the hotkey command

* **Via your UT settings file**

  Again, this method can't be used for very complex commands.
  
  1. Open `UT/System/User.ini`
  2. Under the `[Engine.Input]` section, specify a hotkey command in the format:
     `X=command`
  
* **Via aliases**

  Aliases simply allow you to give a shorter name to a group of commands.
  
  1. Open `UT/System/User.ini`
  2. Add a new `Aliases[n]` entry following the same format as existing entries
  3. Bind a key (as above) with the name of your new alias as the command
  
* **Via `.cfg` files**

  This is the most flexible method, allowing you to execute multiple commands from a single key.
  Keys can also be re-bound using multiple `.cfg` files to effectively create "toggleable" hotkeys.
  
  1. Open `UT/System/`
  2. Create a new text file called `example.cfg`
  3. Edit and save the file, adding commands (one per line)
  4. Execute the command in-game using `exec example.cfg` (or by binding this to a key as above)

How do I use the hotkeys in this repository?
--------------------------------------------
If the hotkey is in the form of a `.cfg` file, simply copy that file to your `UT/System/` folder. While in-game, run the hotkey by pressing `tab` and typing `exec example.cfg` where `example` is the name of the hotkey file. You can also bind this to a keyboard key using `set input X exec example.cfg` to create your hotkey.
