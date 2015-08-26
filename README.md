Bad Code Block Module
=====================
by Nick Bair

An edit-safe custom content editor module for Joomla! 3.x
---------------------------------------------------------

Create your own custom content blocks without worrying about HTML or JavaScript
being stripped away by the WYSIWYG editor.

### What is this thing?

Sometimes you need a bit of JavaScript on one or two pages and it doesn't make
sense to hard-code it into your template. In those cases, it's common to use
Joomla's Custom HTML module to add the page-specific code. The problem with
mod_custom is that if someone edits the module with TinyMCE or another WYSIWYG
editor, all the <script> tags will be eradicated.

the Bad Code Block module is intended to circumvent this problem by providing a
strictly CodeMirror-based editor window with all content filtering disabled.

### Cool! How do I use it?

To use it, simply create a new Bad Code Block module and paste in your code.
Because this module is intended for code, all module chrome is eliminated by
overriding the user-selected module style and setting this value to "none". This
means that the *Show Title* field will be ignored, as will the *Module Style*
field under the *Advanced* tab.

### But I need module chrome!

If you need module chrome but want to avoid having your code stripped, simply
nest your Bad Code Block module within a Custom HTML module. To do this, create
a Custom HTML module and configure your desired module style settings. Under the
*Options* tab, be sure to set *Prepare Content* to **Yes**. Then include your
Bad Code Block module within the Custom HTML content editor using Joomla's
[{loadmodule} or {loadposition} facilities](https://docs.joomla.org/How_do_you_put_a_module_inside_an_article%3F).
