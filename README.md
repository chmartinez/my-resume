# my-resume

Combining"resume-cli", "html-pdf" and "json-resume" libs to build my CV

Steps to use it
---------
* run "npm install" in order to download required dependencies.
* create a "resume.json" file following the format defined at https://jsonresume.org/.
* replace the current "resume.json" with the one previously created. **The file name must be "resume.json". Do not change it!**.
* modify the json as needed
* run `npm run build` and voilá! A new html and a pdf version!
*NOTE*: since this is a personal project, I'm hardcoding the "theme" being used. 
If you want to set an specific "theme" for your resume, you will have to do the following:
* check out the list of available themes that jsonresume offers: http://jsonresume.org/themes/
* npm install the theme you wish to use locally before attempting to use it (it may require that you install the theme globally (i.e: using the -g option from npm) so make sure to check that out).
* replace the theme param on the`json2html` script at `package.json` with yours.
* run `npm run build` and check the html and the pdf that are generated.

Want an HTML file, published in the web?
-------
Use the "publish" command from `package.json` (check https://github.com/jsonresume/resume-cli#resume-publish for more info) 
* Make sure to first login to your "resume-cli" account by using "resume login" command.

Why not using "pdf" as output format?
-------
In my case, the generated pdf doesn't have margins, and I think that it could be useful to have a way to pass that kind of config options. That's why I'm using the *html-pdf* lib :).



### TODO'S
* pass configuration params to index.js
* use ES6 syntax
* create a command for this
* find out a way to integrate the tools in a more fashioned way.
* this Repo and node project is *so 2014*. Update it!
