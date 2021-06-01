# 404 and url Redirect With Htaccess

## Hello there,
In our project where you will redirect 404 and url with htaccess, I will present how to create a 404 page not found page and redirect all errors to 404, as well as redirect with RewriteRule.

#### Our Project Content
* Redirecting all errors on the website to 404 page
* Hiding .php or .html extensions of the url part of our website


#### 404 page redirect in .htaccess
* With " ErrorDocument 404 " write the name of the page you want to redirect errors to right next to the " / " sign (eg: 404.php)

**Important**
- If a space or wrong page name is written to the right of the "/ " sign, your project may give an error.
- Do not delete the space to the left of the "/" sign. Otherwise it may fail
```
RewriteEngine On
ErrorDocument 404 /404.html
```
![alt text](https://github.com/FRTYZ/404-and-Url-Redirect-With-Htaccess/blob/main/ss/404.png?raw=true)


#### Hide .php or .html extensions in .htaccess
* Just next to the "^" sign, write the page name you want without the extension and leave a space.
* Write the real name of the page in the space left and leave a space.          

```
RewriteRule ^homepage index.html [L,NC]
RewriteRule ^about about.html [L,NC]
```

* With RewriteRule, we wrote the name of the page in the href part of the a tag of the file that I had hidden. So we changed the name from "index.php" to "homepage".
```
 <a class="nav-link" href="homepage">Home Page</a>
 a class="nav-link" href="about">About</a>
``` 
![alt text](https://github.com/FRTYZ/404-and-Url-Redirect-With-Htaccess/blob/main/ss/home-page.png?raw=true)
![alt text](https://github.com/FRTYZ/404-and-Url-Redirect-With-Htaccess/blob/main/ss/about-page.png?raw=true)

#### .htaccess
```
RewriteEngine On
ErrorDocument 404 /404.html

RewriteRule ^homepage index.html [L,NC]
RewriteRule ^about about.html [L,NC]
```

Good Encodings
