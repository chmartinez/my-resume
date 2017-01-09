# my-resume
Combining"resume-cli", "html-pdf" and "json-resume" libs to build my CV

Steps to use it
---------
* create a "resume.json" file following the format defined at https://jsonresume.org/.

* replace the current "resume.json" with the one previously created. **The file name must be "resume.json". Do not change it!**.
* run "npm install" in order to download required dependencies.

* run resume-cli "resume" command to create a new html with the desired theme for the .json file.

<pre>
resume export  --format html --theme "a_downloaded_theme" "output_file_name"
</pre>
In my case, I use the "jsonresume-theme-stackoverflow" theme. As the "resume-cli" README says:
<pre>
A list of available themes can be found here: http://jsonresume.org/themes/

Please npm install the theme you wish to use locally before attempting to export it.
</pre>

For example, use this:
<pre>
resume export  --format html --theme stackoverflow resume.html
</pre>
*Side note*: it may require that you install the theme globally (i.e: using the -g option from npm) so make sure to check that out.

* run the index.js file as following:
<pre>
node index.js
</pre>

After that, and if everything goes OK, a "resume.pdf" file will be created.

Want an HTML file, published in the web?
-------
Use the "publish" command from resume-cli using the console (check https://github.com/jsonresume/resume-cli#resume-publish for more info) 

Why not using "pdf" as output format?
-------
In my case, the generated pdf doesn't have margins, and I think that it could be useful to have a way to pass that kind of config options. That's why I'm using the *html-pdf* lib :).



### TODO'S
* pass configuration params to index.js
* use ES6 syntax
* create a command for this
* find out a way to integrate the tools in a more fashioned way.
* this Repo and node project is *so 2014*. Update it!
