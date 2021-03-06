---
layout: page
# title: Sidebar Fixed
---

<nav class="toc-fixed" markdown="1">
<br>
<img src="pictures/pfp (2).png" width="150">
<h1>Andrew Wang</h1>
* TOC
{:toc}
</nav>

This example puts the Table of Contents in the Sidebar.  The sidebar
is locked in place as you scroll up and down.  Just paste the following in 
your page.


<button class="favorite styled" type="button">
  <a href="https://github.com/jwrr/minima-sidebar">Clone It</a>
</button>



```
<nav class="toc-fixed" markdown="1">
* TOC
{:toc}
</nav>
```

And create assets/main.scss with the following content.

```
---
---

@import "minima";

div.wrapper {max-width:960px;margin-left:5%;}
div.post-content > p {width:65%;max-width:640;}
nav.toc-fixed {position:fixed;top:50px;left:60%;max-width:320px}
nav.toc-fixed ul {list-style:none;padding-left:0;margin-left:0;}
table {width:65%;max-width:640;}
```


Examples
--------
Check out [Sidebar](/sidebar-toc), [Sidebar2](/sidebar-toc2) and [Sidebar Fixed](/sidebar-fixed) for more 
examples.

Jekyll Serve
------------

You can view this repo locally with the following command (I'm assuming you've
already installed [jekyll](https://jekyllrb.com/docs/) and cloned this repo.

```
jekyll serve --trace
```

You may get an error similar to the following:

```
/usr/lib/ruby/2.7.0/bundler/runtime.rb:312:in `check_for_activated_spec!': You 
have already activated rouge 3.20.0, but your Gemfile requires rouge 3.19.0. 
Prepending `bundle exec` to your command may solve this. (Gem::LoadError)
```

This means the `gem.lock` file is out of date.  To fix run the following 
command.  You may have to iterate multiple times if more than one gem is 
out of date.

```
bundle update rouge
```

Please send me a pull request with your fix.


Lorem Ipsum
-----------

You can ignore the following documentation.  I'm using the
[Lued Text Editor](https://jwrr.github.io/lued/)
documentation as Lorem Ipsum.


<hr>


Key bindings are defined in <code>lued/lua_src/bindings/lued_bindings.lua</code>.
This is fairly straight-forward, easily understandable Lua code.  You are 
encouraged to modify the bindings to suite your style. You don't Lua
knowledge to figure out what to do.

## Basic Control Key Commands
<table class="">
<tr><td><kbd>Ctrl+@</kbd></td><td>Called when resuming from Ctrl+Z (fg at shell prompt). Not directly used by you. </td></tr>
<tr><td><kbd>Ctrl+Q</kbd></td><td>Quit or Exit. Similar to Sublime Ctrl-Q. </td></tr>
<tr><td><kbd>Ctrl+W</kbd></td><td>Close window or tab. Similar to Sublime Ctrl-W. </td></tr>
<tr><td><kbd>Ctrl+E</kbd></td><td>Move to End of Line. Similar to Sublime &lt;End&gt;. </td></tr>
<tr><td><kbd>Ctrl+R</kbd></td><td>Move right defined number (4) of char </td></tr>
<tr><td><kbd>Ctrl+T</kbd></td><td>Select file tab menu </td></tr>
<tr><td><kbd>Ctrl+Y</kbd></td><td>Redo (undo undo). Similar to Sublime Ctrl+Y </td></tr>
<tr><td><kbd>Ctrl+U</kbd></td><td>Spare </td></tr>
<tr><td><kbd>Ctrl+I</kbd></td><td>Terminal interprets as `Tab` key </td></tr>
<tr><td><kbd>Ctrl+O</kbd></td><td>Open File. Similar to Word Ctrl+O </td></tr>
<tr><td><kbd>Ctrl+P</kbd></td><td>Open File from partial name. Similar to Sublime Ctrl+P </td></tr>
<tr><td><kbd>Ctrl+A</kbd></td><td>Move to Start of Line. Similar to Sublime &lt;Home&gt;. </td></tr>
<tr><td><kbd>Ctrl+S</kbd></td><td>Save File. Similar to Sublime Ctrl+S. </td></tr>
<tr><td><kbd>Ctrl+D</kbd></td><td>Select Word under cursor. Similar to Sublime Ctrl+D </td></tr>
<tr><td><kbd>Ctrl+F</kbd></td><td>Find. Similar to Sublime Ctrl+F.  If text is selected the find selected text (Similar to Sublime Ctrl+F3). </td></tr>
<tr><td><kbd>Ctrl+G</kbd></td><td>Goto Line Number. Similar to Sublime Ctrl+G </td></tr>
<tr><td><kbd>Ctrl+H</kbd></td><td>Find and Replace. Similar to Sublime Ctrl+H. </td></tr>
<tr><td><kbd>Ctrl+J</kbd></td><td>Do Not Use. Same as Enter Key </td></tr>
<tr><td><kbd>Ctrl+K</kbd></td><td>Spare </td></tr>
<tr><td><kbd>Ctrl+L</kbd></td><td>Select entire line. Similar to Sublime Ctrl+L </td></tr>
<tr><td><kbd>Ctrl+Z</kbd></td><td>Undo. Similar to Sublime Ctrl+Z </td></tr>
<tr><td><kbd>Ctrl+X</kbd></td><td>Cut. Similar to Word and Sublime Ctrl+X </td></tr>
<tr><td><kbd>Ctrl+C</kbd></td><td>Copy. Similar to Sublime Ctrl+C </td></tr>
<tr><td><kbd>Ctrl+V</kbd></td><td>Paste. Similar to Sublime Ctrl+V </td></tr>
<tr><td><kbd>Ctrl+B</kbd></td><td>Spare. - let's keep that way for tmux compatibility </td></tr>
<tr><td><kbd>Ctrl+N</kbd></td><td>Create New File. Similar to Word. </td></tr>
<tr><td><kbd>Ctrl+M</kbd></td><td>Do Not Use. </td></tr>
</table>
## File Tab Commands
<table>
<tr><td><kbd>Alt+tt</kbd></td><td>Change to next file tab. Similar to Sublime next_view Ctrl+Tab or Command+Shift+]. </td></tr>
<tr><td><kbd>Alt+TT</kbd></td><td>Change to previous file tab. Similar to Sublime prev_view Ctrl+Shift+Tab or Command+Shift+[. </td></tr>
</table>
## Select Commands
<table>
<tr><td><kbd>Alt+si</kbd></td><td>Similar to Sublime Ctrl+shift+J.  Select lines with the indentation. </td></tr>
<tr><td><kbd>Alt+sb</kbd></td><td>Select inside curly brace. Similar to Sublime Ctrl+Command+M </td></tr>
<tr><td><kbd>Alt+se</kbd></td><td>Select from cursor to End of line </td></tr>
<tr><td><kbd>Alt+SE</kbd></td><td>Select from cursor to starting End of line </td></tr>
<tr><td><kbd>Alt+sb</kbd></td><td>Select to Bottom of File Buffer </td></tr>
<tr><td><kbd>Alt+SB</kbd></td><td>Select to Beginning of File Buffer </td></tr>
<tr><td><kbd>Alt+sm</kbd></td><td>Select from mark (alt+mm) to cursor. Similar to Sublime Ctrl+K </td></tr>
<tr><td><kbd>Alt+ss</kbd></td><td>Turn off/on selection. Similar to Sublime ESC-Key. </td></tr>
<tr><td><kbd>Alt+sw</kbd></td><td>Select to End of word. </td></tr>
<tr><td><kbd>Alt+SW</kbd></td><td>Select to starting End of word. </td></tr>
</table>
## Movement Commands
<table>
<tr><td><kbd>Alt+bb</kbd></td><td>Goto bottom of file. Similar to Sublime END </td></tr>
<tr><td><kbd>Alt+BB</kbd></td><td>Goto top of file. Similar to Sublime HOME </td></tr>
<tr><td><kbd>Alt+ww</kbd></td><td>Move right one word. Similar to Sublime Ctrl+right_arrow. </td></tr>
<tr><td><kbd>Alt+WW</kbd></td><td>Move left one word. Similar to Sublime Ctrl+left_arrow. </td></tr>
<tr><td><kbd>Alt+ee</kbd></td><td>Express mode - arrow keys move faster </td></tr>
<tr><td><kbd>Alt+></kbd></td><td>Move right half the distance </td></tr>
<tr><td><kbd>Alt+<</kbd></td><td>Move left half the distance </td></tr>
<tr><td><kbd>Alt+rn</kbd></td><td>replay named keystroke sequence </td></tr>
<tr><td><kbd>Alt+rr</kbd></td><td>replay keystroke sequence again </td></tr>
</table>
## Ctags /  Exuberant Tags
<table>
<tr><td><kbd>Alt+cb</kbd></td><td>ctag back </td></tr>
<tr><td><kbd>Alt+cf</kbd></td><td>ctag forward in stack  </td></tr>
<tr><td><kbd>Alt+ct</kbd></td><td>ctag jump. Similar Sublime Ctrl+R </td></tr>
<tr><td><kbd>Alt+CT</kbd></td><td>ctag jump back. </td></tr>
<tr><td><kbd>Alt+cr</kbd></td><td>ctag read </td></tr>
<tr><td><kbd>Alt+cx</kbd></td><td>ctag delete history </td></tr>
</table>
## Delete, Cut, Copy and Paste Commands
<table>
<tr><td><kbd>Alt+ce</kbd></td><td>Copy current pos to eol </td></tr>
<tr><td><kbd>Alt+CE</kbd></td><td>Copy sol to current pos </td></tr>
<tr><td><kbd>Alt+cw</kbd></td><td>Copy word </td></tr>
<tr><td><kbd>Alt+DD</kbd></td><td>Duplicate line. Similar to Sublime Ctrl+Shift+D </td></tr>
<tr><td><kbd>Alt+dd</kbd></td><td>aslt+dd214 duplicates 214 lines. 214 can be any number </td></tr>
<tr><td><kbd>Alt+d</kbd></td><td>del N char </td></tr>
<tr><td><kbd>Alt+xb</kbd></td><td>Delete to Bottom of Tab/Buffer/Window/File </td></tr>
<tr><td><kbd>Alt+XB</kbd></td><td>Delete to Beginning of Tab </td></tr>
<tr><td><kbd>Alt+xe</kbd></td><td>Similar to Sublime Ctrl+KK </td></tr>
<tr><td><kbd>Alt+XE</kbd></td><td>Similar to Sublime Ctrl_K+&lt;Backspace&gt; </td></tr>
<tr><td><kbd>Alt+xl</kbd></td><td>Delete line </td></tr>
<tr><td><kbd>Alt+xm</kbd></td><td>Delete from mark (alt+mm) to cursor </td></tr>
<tr><td><kbd>Alt+xs</kbd></td><td>Delete spaces from cursor to non-whitespace.  If on non-whitespace then go to next line and do it. </td></tr>
<tr><td><kbd>Alt+XS</kbd></td><td>Delete spaces to the left </td></tr>
<tr><td><kbd>Alt+xx</kbd></td><td>Delete word under cursor </td></tr>
<tr><td><kbd>Alt+xw</kbd></td><td>Similar to Sublime Ctrl+KW </td></tr>
<tr><td><kbd>Alt+XW</kbd></td><td>Similar to Sublime Ctrl+Backspace </td></tr>
<tr><td><kbd>Alt+x</kbd></td><td>Cut multiple lines alt+x42&lt;enter&gt; </td></tr>
<tr><td><kbd>Alt+pl</kbd></td><td>Paste Line after current line </td></tr>
<tr><td><kbd>Alt+PL</kbd></td><td>Paste Line before current line </td></tr>
</table>
## Find and Replace Commands
<table>
<tr><td><kbd>Alt+df</kbd></td><td>find word under cursor </td></tr>
<tr><td><kbd>Alt+DF</kbd></td><td>find reverse word under cursor </td></tr>
<tr><td><kbd>Alt+fa</kbd></td><td>Similar to Sublime Ctrl+Shift+F. search all open files for match </td></tr>
<tr><td><kbd>Alt+fb</kbd></td><td>find back. return to position before find operation. </td></tr>
<tr><td><kbd>Alt+ff</kbd></td><td>Similar to Sublime F3. Find next occurrence of search text. </td></tr>
<tr><td><kbd>Alt+FF</kbd></td><td>Similar to Sublime Shift+F3. Find previous occurrence. </td></tr>
<tr><td><kbd>Alt+kb</kbd></td><td>show sidebar with list of open files </td></tr>
<tr><td><kbd>Alt+KB</kbd></td><td>hide sidbar with list of open files </td></tr>
<tr><td><kbd>Alt+FR</kbd></td><td>Find previous occurrence. </td></tr>
<tr><td><kbd>Alt+fc</kbd></td><td>set find case sensitive </td></tr>
<tr><td><kbd>Alt+FC</kbd></td><td>clear find case sensitive (case insensitive) </td></tr>
<tr><td><kbd>Alt+fw</kbd></td><td>set find whole word </td></tr>
<tr><td><kbd>Alt+FW</kbd></td><td>clear find whole word </td></tr>
<tr><td><kbd>Alt+hh</kbd></td><td>Find and Replace again. </td></tr>
<tr><td><kbd>Alt+VV</kbd></td><td>Paste and Find Prev </td></tr>
<tr><td><kbd>Alt+vv</kbd></td><td>Paste and Find Next </td></tr>
<tr><td><kbd>Alt+_minus_</kbd></td><td>Jump back to previous position before Find. Similar to Sublime lued.jump_back. </td></tr>
<tr><td><kbd>Alt+_</kbd></td><td>Jump forward to next position in jump stack. Similar to Sublime lued.jump_forward. </td></tr>
</table>
## Line Swap Commands
<table>
<tr><td><kbd>Alt+sl</kbd></td><td>Swap current line with next line. Similar to Sublime Ctrl+DOWN arrow </td></tr>
<tr><td><kbd>Alt+SL</kbd></td><td>Swap current line with prev line. Similar to Sublime Ctrl+UP arrow </td></tr>
<tr><td><kbd>Alt+bl</kbd></td><td>line sinks down towards bottom of file. Similar to sublime Ctrl+Shift+Down </td></tr>
<tr><td><kbd>Alt+BL</kbd></td><td>line floats up towards top of file. Similar to Sublime Ctrl+Shift+Up </td></tr>
<tr><td><kbd>Alt+br</kbd></td><td>swap current word with next word. Similar to Sublime move_word_right </td></tr>
<tr><td><kbd>Alt+BR</kbd></td><td>swap current word with prev word. Similar to Sublime move_word_left </td></tr>
</table>
## Indent and Align Commands
<table>
<tr><td><kbd>Alt+ii</kbd></td><td>Indented selected lines one space </td></tr>
<tr><td><kbd>Alt+II</kbd></td><td>Unindent selected lines one space </td></tr>
<tr><td><kbd>Alt+ir</kbd></td><td>Reindents selected per defined lued.indent size </td></tr>
<tr><td><kbd>Alt+is</kbd></td><td>Set lued.indent size </td></tr>
<tr><td><kbd>Alt+aa</kbd></td><td>Select All (Entire File). Similar to Sublime Ctrl+A. </td></tr>
<tr><td><kbd>Alt+al</kbd></td><td>Align char on next line with current line </td></tr>
<tr><td><kbd>Alt+af</kbd></td><td>Align First char on next line with current line. If lines selected then align all lines with first line. </td></tr>
</table>
## Center Cursor Commands
<table>
<tr><td><kbd>Alt+kc</kbd></td><td>Recenters cursor to center, press again and recenters to top. Similar to Sublime's CTRL+KC. vim's zz/zt.  </td></tr>
<tr><td><kbd>Alt+KC</kbd></td><td>Recenters cursor to top, press again and recenters to center. Similar to Sublime's CTRL+KC. vim's zz/zt.  </td></tr>
</table>
## Comment Commands
<table>
<tr><td><kbd>Alt+cc</kbd></td><td>Comment out line. Similar to Sublime Ctrl+slash. </td></tr>
<tr><td><kbd>Alt+CC</kbd></td><td>Uncomment selected lines. </td></tr>
<tr><td><kbd>Alt+cs</kbd></td><td>Comment set. Change start of comment string. </td></tr>
</table>
## Upper / Lower Case Commands
<table>
<tr><td><kbd>Alt+kl</kbd></td><td>Similar to Sublime Ctrl+KL. Convert to Lower Case </td></tr>
<tr><td><kbd>Alt+ku</kbd></td><td>Similar to Sublime Ctrl+KU. Convert to Upper Case </td></tr>
</table>
## Mark Commands
<table>
<tr><td><kbd>Alt+sm</kbd></td><td>Similar to Sublime Ctrl+KA. Select from mark to cursor (set mark with alt_mm) </td></tr>
<tr><td><kbd>Alt+dm</kbd></td><td>Similar to Sublime Ctrl+KW. Delete from mark to cursor (set mark with alt_mm) </td></tr>
<tr><td><kbd>Alt+m</kbd></td><td>Set Named Marker  </td></tr>
<tr><td><kbd>Alt+M</kbd></td><td>Goto Named Marker </td></tr>
<tr><td><kbd>Alt+mm</kbd></td><td>Similar to Sublime Ctrl+K+space. Set Mark </td></tr>
<tr><td><kbd>Alt+MM</kbd></td><td>Goto previous mark </td></tr>
<tr><td><kbd>Alt+mn</kbd></td><td>Goto next mark in stack </td></tr>
</table>
## Insert Line Before / After Commands
<table>
<tr><td><kbd>Alt+ll</kbd></td><td>Goto to end of line and insert new line. similar to vi's o. Similar to Sublime Ctrl+Enter </td></tr>
<tr><td><kbd>Alt+LL</kbd></td><td>Goto beginning of line and insert new line. similar to vi's O. Similar to Sublime Ctrl+Shift+Enter </td></tr>
</table>
## Page Up / Down Commands
<table>
<tr><td><kbd>Alt+p</kbd></td><td>Move down N lines </td></tr>
<tr><td><kbd>Alt+P</kbd></td><td>Move up N lines </td></tr>
<tr><td><kbd>Alt+pp</kbd></td><td>Similar to Sublime &lt;PageDn&gt; (or ctrl+u in vintage mode) , move down half page </td></tr>
<tr><td><kbd>Alt+PP</kbd></td><td>Similar to Sublime &lt;PageUp&gt; (or ctrl+d in vintage mode), move up half page </td></tr>
</table>
## Remove Tabs and Spaces
<table>
<tr><td><kbd>Alt+ralt</kbd></td><td>Replace all leading tabs with spaces at start of line </td></tr>
<tr><td><kbd>Alt+rats</kbd></td><td>Remove all trailing spaces at end of line </td></tr>
<tr><td><kbd>Alt+ratsall</kbd></td><td>Remove all trailing spaces in all files </td></tr>
<tr><td><kbd>Alt+z</kbd></td><td>Similar to Sublime Ctrl-z. Undo. After alt-z is used, ctrl-z becomes unix suspend command. </td></tr>
<tr><td><kbd>Alt+incr</kbd></td><td>Read number at current position, go down a line, and replace number with incremented value. </td></tr>
<tr><td><kbd>Alt+decr</kbd></td><td>Decrement next line's index. </td></tr>
</table>
## Configuration Commands
<table>
<tr><td><kbd>Alt+.c</kbd></td><td>Toggle Ctrl+C between Cut and Kill Process </td></tr>
<tr><td><kbd>Alt+.ind</kbd></td><td>Turn auto-lued.indent on/off </td></tr>
<tr><td><kbd>Alt+.edi</kbd></td><td>Change from Lua mode to Edit mode. You almost always want to be in edit mode.  </td></tr>
<tr><td><kbd>Alt+.lua</kbd></td><td>Toggle to Lua mode to enter lua commands. Rarely used. </td></tr>
<tr><td><kbd>Alt+.mlt</kbd></td><td>Set minimum lines to from top of page to cursor </td></tr>
<tr><td><kbd>Alt+.mlb</kbd></td><td>Set minimum lines from cursor to bottom of page </td></tr>
<tr><td><kbd>Alt+.ps</kbd></td><td>Change number of lines for page up/down command </td></tr>
<tr><td><kbd>Alt+.sl</kbd></td><td>Toggle on/off the status line </td></tr>
<tr><td><kbd>Alt+.slr</kbd></td><td>Toggle status line being shown in reverse video </td></tr>
<tr><td><kbd>Alt+.tab</kbd></td><td>Toggle replace tabs with spaces as you type (defaults to replace) </td></tr>
<tr><td><kbd>Alt+.rts</kbd></td><td>Toggle on/off remove trailing spaces as you type (defaults to don't remove) </td></tr>
<tr><td><kbd>Alt+p_squote</kbd></td><td>Put string into lued.paste buffer </td></tr>
</table>
## Misc Commands
<table>
<tr><td><kbd>Alt+^</kbd></td><td>Delete from cursor to start of line </td></tr>
<tr><td><kbd>Alt+$</kbd></td><td>Delete from cursor to end of line </td></tr>
<tr><td><kbd>Alt+//</kbd></td><td>Find forward </td></tr>
<tr><td><kbd>Alt+:w</kbd></td><td>Save File. Similar to Vi :w </td></tr>
<tr><td><kbd>Alt+colors</kbd></td><td>Show colors </td></tr>
<tr><td><kbd>Alt+cd</kbd></td><td>Change directory </td></tr>
<tr><td><kbd>Alt+ed</kbd></td><td>Change to EDIT mode. You almost always want to be in EDIT mode. </td></tr>
<tr><td><kbd>Alt+help</kbd></td><td>Help. Open lued_bindings.lua </td></tr>
<tr><td><kbd>Alt+jj</kbd></td><td>Similar to Sublime Ctrl+J. Join lines. </td></tr>
<tr><td><kbd>Alt+ln</kbd></td><td>show absolute line numbers </td></tr>
<tr><td><kbd>Alt+LN</kbd></td><td>hide absolute line numbers </td></tr>
<tr><td><kbd>Alt+rln</kbd></td><td>show relative line numbers </td></tr>
<tr><td><kbd>Alt+RLN</kbd></td><td>hide relative line numbers </td></tr>
<tr><td><kbd>Alt+ls</kbd></td><td>unix ls command. dos dir command </td></tr>
<tr><td><kbd>Alt+LU</kbd></td><td>Change to LUA mode. You rarely want to be in lua mode. </td></tr>
<tr><td><kbd>Alt+nop</kbd></td><td>No Op. (same as Alt+NOOP) </td></tr>
<tr><td><kbd>Alt+noop</kbd></td><td>No Op (same as Alt+NOP) </td></tr>
<tr><td><kbd>Alt+qq</kbd></td><td>Wrap line at cursor. Subsequent lines end at previous line. Similar to Sublime Alt+q </td></tr>
<tr><td><kbd>Alt+QQ</kbd></td><td>set join wrap </td></tr>
<tr><td><kbd>Alt+reinit</kbd></td><td>Reload lued script </td></tr>
<tr><td><kbd>Alt+review</kbd></td><td>Review mode prevents saving file </td></tr>
<tr><td><kbd>Alt+refresh</kbd></td><td>Reload current file </td></tr>
<tr><td><kbd>Alt+sa</kbd></td><td>Similar to Sublime Ctrl+Shift+S. File Save as. </td></tr>
<tr><td><kbd>Alt+SaveSession</kbd></td><td>Save session file </td></tr>
<tr><td><kbd>Alt+LoadSession</kbd></td><td>Load session file </td></tr>
<tr><td><kbd>Alt+Seti</kbd></td><td>Set Scope Indent SI2 SI3 SI4 </td></tr>
</table>


