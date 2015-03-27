## Introduction

Late last year I stumbled upon a Node.js web framework called [Pencilblue](https://pencilblue.org). I have been investigating it ever since. Because of how powerful this platform is, I decided to share some of what I've learnt. In this post, we will just look at the basics.

 What is Pencilblue you might ask. According to the project's github page, it is a "Full stack online publishing and CMS for Node.js". Pencilblue been full stack means, it uses both client and sever-side frameworks which happens to be in the JavaScript programming language. The client-side framework it uses is [AngularJS](https://www.airpair.com/posts/tag/angularjs), and well [Node.js](https://www.airpair.com/node.js) for the server-side. It supports [MongoDB](http://www.mongodb.org) database by default. If you have used any of these tools to build for the web, you will understand why they were chosen by the team to build the framework. 

PencilBlue's "sweet spot is a brand or publication that wants a serious, data driven website, but also wants non-technical team members to be able to manage it easily". Because of this, it was built "to fit right in between three genres: blogging (WordPress), traditional CMS (Drupal), and point and click (Squarespace)".  


## 2. Installation

In this section, we will be looking at how to install PencilBlue on windows, mac and linux systems. 

### 2.1 Windows

<h4>Download and install Node.js</h4>

<ol>
   <li>In the browser, go to http://nodejs.org/download and download the latest version of the Node.js Windows msi installer for your processor type.</li>
   <li>Run the downloaded msi installer file and follow the instructions in the install program.</li>
</ol>

<h4>Download and install MongoDB</h4>
<ol>
   <li>In the browser, go to http://www.mongodb.org/downloads and download the latest version of the MongoDB Windows msi installer for your processor type.</li>
   <li>Run the downloaded msi installer file and follow the instructions in the install program.</li>
</ol>

<h4>Install git for Windows</h4>
<ol>
   <li>In the browser, go to http://git-scm.com/download/win to download the latest version of git for Windows.</li>
   <li>Run the downloaded exe installer file and follow the instructions in the install program.</li>
</ol>

<h4>Install the PencilBlue command-line interface tool</h4>
<ol>
   <li>Open a command prompt as an administrator (Microsoft how to).</li>
   <li>Run `npm install -g pencilblue-cli` to install the command-line interface through NPM.</li>
</ol>

<h4>Install and Run PencilBlue</h4>
<ol>
   <li>Once pencilblue-cli is installed, in the git bash window (Start Menu -&gt; Git -&gt; Git Bash), cd to the directory that you want the PencilBlue directory to install to.</li>
   <li>Run pbctrl install [directory] where directory is the name of the folder you want PencilBlue to be installed to. Follow the instructions.</li>
   <li>cd to the directory you installed PencilBlue to and run pbctrl start</li>
   <li>You should now be able to navigate to your install of PencilBlue through the URL you specified in the install.</li>
</ol>


<h3> 2.2 Mac</h3>

<h4>Download and install Node.js</h4>

<ol>
   <li>In the browser, go to http://nodejs.org/download and download the latest version of the Node.js Mac pkg installer.</li>
   <li>Run the downloaded pkg installer file and follow the instructions in the install program.</li>
</ol>

<h4>Download and install MongoDB</h4>
<p>The easiest way to install MongoDB on Mac is through Homebrew. If you want to install it manually, MongoDB provides instructions here.</p>

<ol>
   <li>If you don't have Homebrew installed, open a terminal window and run ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"</li>
   <li>In the terminal, run brew install mongodb</li>
</ol>


<h4>Install the PencilBlue command-line interface tool</h4>

<ol>
   <li>In the terminal, run `npm install -g pencilblue-cli` to install the command-line interface through NPM.</li>
</ol>


<h4>Install and Run PencilBlue</h4>

<ol>
   <li>Once pencilblue-cli is installed, in the terminal, cd to the directory that you want the PencilBlue directory to install to.</li>
   <li>Run `pbctrl install [directory]` where directory is the name of the folder you want PencilBlue to be installed to. Follow the instructions.</li>
   <li>cd to the directory you installed PencilBlue to and run `pbctrl start`</li>
   <li>You should now be able to navigate to your install of PencilBlue through the URL you specified in the install.</li>
</ol>

###2.3 Linux

<h4>Download and Install Node.js</h4>

<ul>
   <li>
      Ubuntu/Debian
      <ol>
         <li>Ubuntu's package manager has an outdated version of Node.js, so you'll need to add a repository to install</li>
         <li>In a terminal, run curl -sL https://deb.nodesource.com/setup | sudo bash -</li>
         <li>Then run `sudo apt-get install nodejs` to install the latest version of Node.js</li>
      </ol>
   </li>

   <li>
      Fedora
      <ol>
         <li>In a terminal, run `sudo yum install nodejs npm`</li>
      </ol>
   </li>

   <li>
      Arch
      <ol>
         <li>In a terminal, run `pacman -S nodejs`</li>
      </ol>
   </li>
</ul>



<h4>Download and Install MongoDB</h4>
<ul>
   <li>
      Ubuntu/Debian
      <ol>
         <li>In a terminal, run `sudo apt-get install mongodb`</li>
      </ol>
   </li>
   <li>
        Fedora
      <ol>
         <li>In a terminal, run `sudo yum install mongod`</li>
      </ol>
   </li>
   <li>
        Arch
      <ol>
         <li>In a terminal, run `pacman -S mongodb`</li>
      </ol>
   </li>
</ul>

<h4>Install the PencilBlue command-line interface tool</h4>

<ol>
  <li>In the terminal, run npm install -g pencilblue-cli to install the command-line interface through NPM.</li>
</ol>

<h4>Install and Run PencilBlue</h4>
<ol>
   <li>Once pencilblue-cli is installed, in the terminal, cd to the directory that you want the PencilBlue directory to install to.</li>
   <li>Run `pbctrl install [directory]` where directory is the name of the folder you want PencilBlue to be installed to. Follow the instructions.</li>
   <li>cd to the directory you installed PencilBlue to and run `pbctrl start`</li>
   <li>You should now be able to navigate to your install of PencilBlue through the URL you specified in the install.</li>
</ol>

## 3 Lets Build a Website with Pencilblue

I this section we will build a website using pencilblue. If you've not read the first two sections, please move up and read. This esction is based on them.

Now that we've gone through the process of installing all we need to build a website with pencilblue, let get build one. 

Open your terminal or command prompt and `cd` into your working directory (where you want the project code to reside). Run `pbctrl install hello-pencilblue`.

You will be asked the following questions. I've added what you will type as response.

<ol>
   <li>Pencilblue: Site Name: (My Pencilblue Site)</li>
   Type **'Hello Pencilblue'** and enter or you can leave it as **My Pencilblue Site**
   <li>Pencilblue: Site Root: (http://localhost:8080)</li>
   Just type enter to use the default. You can choose to change the port if 8080 has already been taken. e.g. **http://localhost:8081**
   <li>Pencilblue: Address to bind to: (0.0.0.0)</li>
   Just type enter to use the default.
   <li>Pencilblue: Site Port: (8080)</li>
   Just type enter to use the default. You can choose to change it if 8080 has already been taken. Note: Make sure the port you specify here is the same as the you specified on the site  root url.
   <li>Pencilblue: MongoDB URL: (mongodb://127.0.0.1:27017)</li>
   Just type enter to use the default or you can choose another url of the mongodb instance you want to use.
   <li>Pencilblue: Database Name: (pencilblue)</li>
   Just type enter to use the default or you can choose a different one.
   <li>Pencilblue: Do you want to install Bower components?: (y/N)</li>
   If you do not want to use cdn urls for you libraries like angularjs and bootstrap but want to use locally installed version type **y** and press enter or return but if you want to use cdns, then type **N** and press enter or return.
 </ol?
 
 Pencilblue will start cloning  the source files for the app from github, install the node dependencies and install the bower components if you selected yes to, **Pencilblue: Do you want to install Bower components?: (y/N)**.
 
 After All that, a config.js file will be generated for you which will be used by penciblue.
 
 Now, cd into the directory in which pencilblue has been intalled and type **pbctrl start**. Make sure your MongoDB instance is up and running before you start the app else you will get an error.
 
 Note: The name you chose for the app (like ) will be used to name the directory in which pencilblue will be installed.
 
 Now navigate to the url you specified in step 2 above in your browser. Pencilblue will present you with a form to enter details to setup an Administrator account for you to enable access to the admin section of pencilblue which will be located at [url]/admin (e.g. http://localhost:8080/admin)
 
And there you go. You have pencilblue up and running.

## 4 How to learn PencilBlue

There are several places you can learn about Pencilblue. The following are links to resources you can use.

* https://github.com/pencilblue/pencilblue/wiki
* http://pencilblue.github.io/
* https://pencilblue.org/section/tutorials
* https://pencilblue.org/blog
* http://www.reddit.com/r/pencilblue/

I encourage you to take a look at PencilBlue. 

In future posts, I will show you how to accomplish specific tasks like, building a plugin, theme, controllers and even building a simple blog theme.