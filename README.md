# static_website

Assignment 3: Static Website
To deploy a static website using Hugo (a static web site generator) and host it on GitHub Project Pages.

This is a group activity. Hence, participation of all group members is mandatory.

Static web site generator
A static web site generator is an application that takes plain text files and compiles them to HTML files.

Hugo


Hugo is a static HTML and CSS website generator written in Go. It is optimized for speed, ease of use, and configurability. Hugo takes a directory with content and templates and renders them into a full HTML website.

Hugo relies on Markdown files with front matter for metadata, and you can run Hugo from any directory. This works well for shared hosts and other systems where you don’t have a privileged account.

Hugo renders a typical website of moderate size in a fraction of a second. A good rule of thumb is that each piece of content renders in around 1 millisecond.

Hugo is designed to work well for any kind of website including blogs, tumbles, and docs.

Instructions
Install Hugo
Create a repository in GitHub
repository name: static_website
Clone the repository to your computer
git clone https://github.com/<USERNAME>/static_website.git
Create a webiste using Hugo
Website name: static_website
hugo new site static_website --force
Add this line publishDir = "docs" to the config.toml file (set the publish directory)
echo 'publishDir = "docs"' >> config.toml
Replace baseURL in the config.toml file
baseURL = "https://<USERNAME>.github.io/static_website/"
Your config file should look like this:
 baseURL = "https://<USERNAME>.github.io/static_website/"
 languageCode = "en-us"
 title = "MSIG XXI - My New Hugo Site"
 theme = "ananke"
 publishDir = "docs"
Customise your website, for example:
Add a theme
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
echo 'theme = "ananke"' >> config.toml
Add posts
hugo new posts/my-first-post.md
Create extra sections
more...
Test your website, start the Hugo server
hugo server -D
Navigate to your new site at http://localhost:1313/
Build static pages
hugo -D
Commit & Push your changes to the remote directory
git add .
git commit -m "my first website..."
git push
Setup GitHub Project Pages
Go to Settings → GitHub Pages
From Source, select “master branch /docs folder”. If the option isn’t enabled, you likely do not have a docs/ folder in the root of your project.
fig_GitHubPages
Test it
https://<USERNAME>.github.io/static_website/
Configuration file
Example of a config.toml file:

   baseURL = "https://<USERNAME>.github.io/static_website/"
   languageCode = "en-us"
   title = "MSIG XXI - My New Hugo Site"
   theme = "ananke"
   publishDir = "docs"
Replace the <USERNAME> for your actual GitHub username
publishDir = "docs" is mandatory to work on GithHub Project pages
Deliverable
Link to the website
Screenshot of the contributors' activity
Collaboration
While working on your website, you can post screenshots and your website link on the below issue:

https://github.com/alopezag/WT-2020I/issues/1
The idea, it is to share your knowledge with others.
