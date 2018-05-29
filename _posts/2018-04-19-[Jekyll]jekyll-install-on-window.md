

###2018-04-19

#[Jekyll] jekyll install on window



> #####Be careful!
>
> If the first part of the repository doesn't exactly your username, it won't work, so make sure to get it right.



## 1. Install ruby (with DEVKIT)

Go to https://rubyinstaller.org/downloads/ and install ruby with DEVKIT



## 2. Make Git Repository management blog page on Github

The repository must be named [Githubusername].github.io, so that you can access it directly from the web browser.



## 3. Install jekyll (on Ruby Command Prompt)

~~~
$ gem install jekyll

#Packages with dependencies
$ gem install bundler
$ gem install minima
$ gem install jekyll-feed
$ gem install tzinfo-data
~~~



## 4. Make jekyll new folder

~~~
$ jekyll new [Githubusername].github.io
~~~



## 5. Connect localhost

~~~
$ cd ./[Githubusrname].github.io
$ bundle exec jekyll serve
~~~

 Then, you can connec to http://localhost:4000 on browser



## 6. Connect with Github pages

~~~
$ git add . -A
$ git add -A && git commit -m "Initial commit"
$ git remote add origin [Git URL]
~~~



## 7. Github push

~~~
$ git add . -A
$ git commit -m [commit contents]
$ git push -u origin master
~~~

