---
layout: post
comments: true
title:  "RICOH THETA and WebVR - Quick HowTo"
date:   2016-09-14
author: "Craig"
categories: WebVR
---
![](/blog/img/2016-09/aframe-mobile.png)

The future of virtual reality and augmented reality is [WebVR](http://venturebeat.com/2016/09/17/how-webvr-will-make-virtual-reality-massively-available/).
It's open source JavaScript, works with browsers and mobile phones today.
THETA media works great with it. Support for Occulus Rift and HTC Vive
headsets is available today in development builds and will be available
to the general public by the end of 2016.

![](/blog/img/2016-09/occulus-rift.png)

It's easy to get started and powerful enough to build amazing applications.

![](/blog/img/2016-09/web-vr-menu.png)

Let's get started with a simple THETA VR site using
[A-Frame](https://aframe.io/).

Using your mobile phone, go to this sample link:

[https://codetricity.github.io/aframe-demo/scene1.html](https://codetricity.github.io/aframe-demo/scene1.html)

Put the mobile phone in Cardboard and you'll be able to navigate the image by moving your phone.

The image will look like this. Press the goggle icon to split the image.

![](/blog/img/2016-09/meetup-image.png)

There's nothing unusual here except that the main code is one line.

![](/blog/img/2016-09/code-sample.png)

[Fork the sample code](https://github.com/theta360developers/aframe-demo) on GitHub.

![](/blog/img/2016-09/github.png)

Copy your THETA pictures into the image sub-directory.

![](/blog/img/2016-09/image-directory.png)

Open the file `scene1.html`

    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="utf-8">
        <title>RICOH THETA MeetUp Test Scene 1</title>
        <meta name="description" content="Panorama — A-Frame">
        <script src="dist/aframe.js"></script>
      </head>
      <body>
        <a-scene>
          <a-sky src="image/1.jpg" rotation="0 -130 0"></a-sky>
        </a-scene>
      </body>
    </html>

Change `src/1.jpg` to the name of your file.

Push the file back up to GitHub Pages and view the URL in your browser. That's
it. You can now refer to the [A-Frame](https://aframe.io/)
site to come up with ideas to build
your interface.

---

## Troubleshooting

If you open the file on your local computer without uploading to
GitHub Pages, you may see this:

![](/blog/img/2016-09/console-error.png)

The error message in your JavaScript console will be:

>Image from origin 'file://' has been blocked from loading by Cross-Origin
Resource Sharing policy: Invalid response.
Origin 'null' is therefore not allowed access.


The fastest way to sort this out is to simply to push to gh-pages.
I'm assuming that you're familiar with gh-pages or can figure it out
with a quick web search. The super short version: `git add *`, which will
add all your files `git commit -a`, `git push`. Make sure you push to
the `gh-pages` branch. Your site will be up at
username.github.io/aframe-demo/scene1.html

`chrome://flags`
![](/blog/img/2016-09/chrome-flags.jpg)


## Resources

* [A-Frame](https://aframe.io/)
* [WebVR](https://webvr.info/)
* [MozVR](https://mozvr.com/)
* [RICOH THETA Community Forum](http://lists.theta360.guide/)
