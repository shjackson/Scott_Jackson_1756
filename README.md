# Scott_Jackson_1756
 olapic-js-assessment-201906


Hi team,

Here are basic steps I went through to solve the "Carousel" challenge.

I read through the test instructions and set up a Github account, which I've never used before. I watched a few youtube tutorials for beginners, and decided to use the Github Desktop app for managing my repositories. I created a test project to get the feel for the app and it seemed to be working fine.

I created a repository on Github called "shjackson/Scott_Jackson_1756" and uploaded the unedited versions of the Carousel files (i.e. the ZIP files) into the repository. These are essentially the "before" version of the files, which will be overwritten with subsequent change/commits.

+++++++++

After opening the files in the zip called "olapic-js-assessment-201906.zip" (hereinafter referred to as ZIP), I double clicked on index.html. It appeared blank in the web browser. Using Notepad++, I examined the code in the index.html and the files in the /js and /css directories.

After some initial consulting on http://apiv2-docs.photorank.me/index.html

I found a link to the following tutorial:

http://developer.olapic.com/articles/tutorial-apiv2-carousel-example.html

This tutorial (hereinafter referred to as ONLINE) seemed to contain a close match of the existing code that was included in the test files within the ZIP. I copy/pasted this ONLINE version of the script.js code and compared it side-by-side in Excel with the ZIP version of the script.js code.

I noticed immediately that the ONLINE version of the script.js code was longer, so I assumed that I would need to find the differences between the online version of the code and merge them with the ZIP version.

In addition to blocks of code that were present in the ONLINE version but missing in the ZIP version, I noticed that a few parameters were set to "False" in the ZIP version, but set to "True" for the online version. These parameters were "nav: false" and "autoplay: false" in the ZIP version. I set both of them to "true" to match the ONLINE version.

Since the ONLINE version is meant as a "production" tutorial for general use, I assumed that the wherever there was a "true/false" discrepancy (as mentioned above), I would need to change the use the settings included in the ONLINE version.

When examining the differences between the ZIP version of index.html and the ONLINE version, the only noticeable difference was on line 21:

ZIP:
<script src="js/script.js"></script>

ONLINE:
<script src="js/api_examples.js"></script>

This seems like the ONLINE version may contain a mistake since "api_examples.js" is not mentioned anywhere else in the ONLINE tutorial and is not included in the corresponding folder structure. For my commit, I kept "script.js".

I used an Excel formula to check for exact match between the "auth_token" value that was provided with the test instructions and the ONLINE version.

0a40a13fd9d531110b4d6515ef0d6c529acdb59e81194132356a1b8903790c18 == 0a40a13fd9d531110b4d6515ef0d6c529acdb59e81194132356a1b8903790c18

(TRUE)

I visually confirmed exact match between the customer ID provided with the test instruction and the ONLINE version

215757 == 215757

(TRUE)

At this point, after reconciling the script.js and index.html files with the ONLINE version, the index.html file displays a Carousel widget in the web browser, but it is only approx 1.5 images wide, and the NAV arrows were in the middle of the widget, not toward the extremes. I decided to keep investigating.
	
After further online research I discovered that this exact Widget was hosted on Olapic's github account (hereinafter GITHUB) at:

https://github.com/Olapic/PublicDocs/tree/gh-pages/code_examples/apiv2-carousel

I recreated the project structure in a separate local folder (i.e. away from my test version of the same files) using all of the corresponding files and folder structure that was in hosted in the GITHUB version of the same widget.

I opened the index.html version of the GITHUB files in my web browser, and it displayed the full wide-length Carousel correctly, with a width of 4 images, and the NAV arrows correctly position towards either extreme of the widget.

I visually compared the GITHUB versions of the script.js and index.html files with the current TEST versions (i.e. those that came from the ZIP). There were no major differences. In the script.js version of the ZIP, there were test instructions as comments within the file, that were not included in the GITHUB version. 

While comparing the "main.css" file between its ZIP version and ONLINE version, I discovered this key difference:

ZIP:
.owl-carousel .owl-stage-outer {  
	max-width:450px; 
	
GITHUB:
.owl-carousel .owl-stage-outer {  
	max-width:1275px; 
	
The other key difference were:

ZIP:
.owl-prev {   

}

GITHUB:
.owl-prev { 
	float:left; 
} 

ZIP:
.owl-next {   

}

GITHUB:
.owl-next { 
	float:right; 
}


Without being more familiar with the overall code, I assumed that these particular parameters (.owl-prev and .owl-next) are responsible for the placement of the NAV arrows, which were previously located incorrectly in my TEST version of the files. 

I decided to check line 21 of the GITHUB version of the index.html file.

It reads:

<script src="js/script.js"></script>

Therefore, I think there is an error in the same code (line 20) in the ONLINE version (http://developer.olapic.com/articles/tutorial-apiv2-carousel-example.html):

<script src="js/api_examples.js"></script>

Please confirm and update the ONLINE version if necessary.

.......

At this point, I had determined that the GITHUB versions of the files  were functional, and had determined the key differences between the GITHUB version and the current state of my ZIP versions. I created a backup of my ZIP versions, and over-wrote my live repository version of the ZIP files with all of the GITHUB versions of the same files. Then I committed those versions to my Github repository (shjackson/Scott_Jackson_1756).

Note: I mispelled the word "functional" when uploading the corrected versions of the files. I couldn't figure out how to added a change summary, so the typo is still there. Sorry about that.

I updated this Readme.

Please let me know if you have any questions or comments about how I worked through this project.

Cheers,

Scott


