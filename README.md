
# Website Performance Optimization portfolio project
## About the project
*  To optimise the portfolio site so that it have pagespeed insights score greater than 90
* To optimise  <kbd>pizza.html</kbd> so that it have 60 FPS

## Getting started 
### Download
  > To download this Repo use
  > git clone https://github.com/arulk8/projoptim.github.io.git 
  
  
### To view as github page
> click on the link  [https://arulk8.github.io/projoptim.github.io/](https://arulk8.github.io/projoptim.github.io/) 
### software used
* Google chrome **Dev tools**
*  ngrok

### Create local server

 You can run a local server using
```bash
$> cd /path/to/your-project-folder
$> python -m SimpleHTTPServer 8080
Open a browser and visit localhost:8080
```
Then  Publishing it on Web using  ngrok 

```bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
```
  
   > **Note:**
   >  ngrok and local host should be on same port number . in this case it is 8080

Copy the public URL ngrok gives you and try running it through PageSpeed Insights! . If ngork doesn't work  use github pages.

## My Modifications:

#### Part 1: Optimize PageSpeed Insights score for index.html

* Added ``` media ="print"  ``` in ``` print.css ```
* Removed goggle fonts.
*  Minified ```style.css ``` and added at the bottom of HTML
*  Added `` aync `` attribute  to ``Analytics.js ``

#### Part 2: Optimize Frames per Second in pizza.html
* The value of phase which is created by long iterative `` for `` loop is changed by simple `` for `` loop
* ``document.queryselectAll ``is  replaced``document.GetElementById``
* This Dom asses element is cached in variable and placed outside the  updatePosition( )  function so that it is not access again and again.
* reduced 200 pizza to 25
*  In the  pizza slider removed all `` document.querySelectorAll( ) `` and cached in a variable 
* removed unnecessary function which caused forced synchronous layout



