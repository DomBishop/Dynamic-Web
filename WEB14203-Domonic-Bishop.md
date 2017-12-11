# Dynamic Web
## Domonic Bishop
## [Here's the app up and running on GitHub! :running:](https://dombishop.github.io/A-Day-in-the-Future/Domonic/)

## Index
- [Presentations](#presentations)
- [Blogs](#blogs)
- [Research](#research)
- [Moodboards](#moodboards)
- [Wireframes](#wireframes)
- [Thimble Pusher](#thimble-pusher)
- [Code Wars Profile](#code-wars-profile)
- [Code Resources](#code-resources)
- [Code for App](#code-for-app)

## Presentations
- [Formative](https://docs.google.com/presentation/d/1o_ulJd2_7Ng9AxtXS-1BX0gl-PL-yXv9qvGMJ0i6xnw/edit?usp=sharing)
- [Summative]()

## Blogs
- [What can be some of the challenges when running a workshop?](https://medium.com/@domonic_bishop/what-can-be-some-of-the-challenges-when-running-a-workshop-bc105aa073fd)
- [Why is it important that we prototype our ideas and test it with users?](https://medium.com/@domonic_bishop/why-is-it-important-that-we-prototype-our-ideas-and-test-it-with-users-dc2914ca3ba6)
- [Analyse your favourite app in terms of interface, data and logic](https://medium.com/@domonic_bishop/analyse-your-favourite-app-in-terms-of-interface-data-and-logic-7166bd4a36f0)
- [What is your biggest learning so far from this project?](https://medium.com/@domonic_bishop/how-i-can-implement-the-feedback-from-the-mozilla-festival-to-improve-my-dynamic-web-project-a76284a16b85)
- [Pair up with another person (not your team mate) and give each other feedback on your peer learning mini-lessons.](https://medium.com/@domonic_bishop/give-each-other-feedback-on-your-peer-learning-mini-lesson-3619e534d449)
- [Watch: The best interface is no interface](https://medium.com/@domonic_bishop/the-best-interface-is-no-interface-4e320bdf58aa)
- [WTF is an API?](https://medium.com/@domonic_bishop/wtf-is-an-api-5915cc522d64)
- [Reflect on this project as a whole](https://medium.com/@domonic_bishop/reflect-on-this-project-as-a-whole-6f294b82e0b)

## Research

### [The Article that influenced the direction we went in for this project!](https://www.theguardian.com/technology/2017/sep/26/tinder-personal-data-dating-app-messages-hacked-sold)

### Mozilla Festival feedback

At the Mozilla Festival we gained some valuable feedback on our app concept. We showed people our app demo video, and they gave us feedback that varied from user interaction options to how the app could be made to work.

We met some members of the Mozilla club at another university, they suggested that we look at screen readers that blind people use to navigate websites. Screen readers have to inspect and decipher the elements of a page, and feed it back to a user so they understand it. We could use this technology to try and uncover how social media apps track your activity.

All the other feedback we got consisted of interface and interaction suggestions. One person suggested that a user should be able to choose when they are notified, constant notifications would get annoying quickly. This then led to the realisation that telling people after they had just lost their data, was shutting the barn doors after the horse has bolted. Instead a user could have a pop up notification saying “you are just about to tell Facebook so and so”, and then the user could decide for themselves if they wanted to continue.

## Moodboards

### [This is the moodboard for the Canary app](https://pin.it/dc2mokrwonnfop)

For Canary, I tried to look at interfaces that had good infographics because that’s integral to the apps purpose. The user needs to understand the data they’re seeing for them to really think about what it is social media apps are taking from us as users.

### [This is the moodboard for the fake Facebook user finder app](https://pin.it/tzdovi2oyvwfvr)

The fake Facebook app was designed with the intention of looking like a Facebook product, and the moodboard reflects that.

## Wireframes

These are the wireframes for the Facebook user finder:

### Home
<img src="https://i.imgur.com/XxS8YMl.png" width="350">

### Results
<img src="https://i.imgur.com/YkTFKrJ.png" width="350">

### Details
<img src="https://i.imgur.com/DQc4IS1.png" width="350">

## [Thimble Pusher](https://thimbleprojects.org/dbishop/377247)

## [Code Wars Profile](https://www.codewars.com/users/DomBishop)

## Code Resources

### These are the sources that I pulled code from to develop my app:

https://www.w3schools.com/css/tryit.asp?filename=trycss_buttons_hover

https://www.w3schools.com/cssref/css3_pr_border-radius.asp

https://www.w3schools.com/tags/att_input_checked.asp

## Code for app

<!doctype html>
<html class="no-js" lang="">
    <head>
        <meta charset="utf-8">
        <meta http-equiv="x-ua-compatible" content="ie=edge">
        <title>FB user finder</title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <link rel="apple-touch-icon" href="apple-touch-icon.png">
        <!-- Place favicon.ico in the root directory -->

        <link rel="stylesheet" href="css/normalize.css">
        <link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">
        <link rel="stylesheet" href="css/main.css">

        <script src="js/vendor/modernizr-2.8.3.min.js"></script>
    </head>
    <body>
        <!--[if lt IE 8]>
            <p class="browserupgrade">You are using an <strong>outdated</strong> browser. Please <a href="http://browsehappy.com/">upgrade your browser</a> to improve your experience.</p>
        <![endif]-->

        <!-- this is the home section-->
        <section id="home">

          <img id="logo" src="https://facebookbrand.com/wp-content/themes/fb-branding/prj-fb-branding/assets/images/fb-art.png">
            <h1>Facebook User Search</h1>
            <p>Have a go at filtering your search by selecting the users preferred device, and whether or not they have children <i id="lineThrough">(don’t worry, the user won’t know):</i></p>
            <h3>When you’re ready hit GO!</h3>
            <select id="skills">
                <option value="mobile">Mobile</option>
                <option value="tablet">Tablet</option>
                <option value="computer">Computer</option>
            </select>

            <select id="pets">

              <option value="children">With children</option>
              <option value="noChildren">Without children</option>

            </select>

            <button class="button1">Go</button>
        </section>
        <!-- this is the results section -->
        <section id="results">
            <a class="back button">Back</a>
            <ol>
                <li>
                    <img src="https://randomuser.me/api/portraits/women/53.jpg">
                    <h2>Susan</h2>
                    <p>About Susan</p>
                </li>
                <li>
                    <img src="https://randomuser.me/api/portraits/men/83.jpg">
                    <h2>Name</h2>
                    <p>About this person</p>
                </li>
                <li>
                    <img src="https://randomuser.me/api/portraits/women/63.jpg">
                    <h2>Name</h2>
                    <p>About this person</p>
                </li>
                <li>
                    <img src="https://randomuser.me/api/portraits/men/3.jpg">
                    <h2>Remy</h2>
                    <p>About this person</p>
                </li>
            </ol>
        </section>
        <!-- this is the details section -->
        <section id="details">
            <a class="back button">Back</a>
            <div id="info">
                <img src="https://randomuser.me/api/portraits/women/53.jpg">
                <h2>Susan</h2>
                <p>About Susan</p>
                <a class="contact button">Contact Susan</a>
            </div>
        </section>

        <!-- load all the JS at the end-->

        <!-- Load jQuery-->
        <script src="https://code.jquery.com/jquery-1.12.0.min.js"></script>
        <script>window.jQuery || document.write('<script src="js/vendor/jquery-1.12.0.min.js"><\/script>')</script>
        <script src="js/plugins.js"></script>


        <!-- Load the Firebase library -->
        <script src="https://www.gstatic.com/firebasejs/4.7.0/firebase.js"></script>
        <script src="js/firebase.js"></script>

        <!-- our own helper scripts -->
        <script src="js/filter.js"></script>
        <script src="js/show.js"></script>

        <!-- MAIN.JS is the script that binds them all -->
        <!-- it needs to be loaded after all the others -->
        <script src="js/main.js"></script>

        <!-- Google Analytics: change UA-XXXXX-X to be your site's ID. -->
<!--
        <script>
            (function(b,o,i,l,e,r){b.GoogleAnalyticsObject=l;b[l]||(b[l]=
            function(){(b[l].q=b[l].q||[]).push(arguments)});b[l].l=+new Date;
            e=o.createElement(i);r=o.getElementsByTagName(i)[0];
            e.src='https://www.google-analytics.com/analytics.js';
            r.parentNode.insertBefore(e,r)}(window,document,'script','ga'));
            ga('create','UA-XXXXX-X','auto');ga('send','pageview');
        </script>
-->
    </body>
</html>
