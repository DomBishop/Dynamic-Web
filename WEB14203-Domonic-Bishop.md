# Dynamic Web
## Domonic Bishop

## Index
- [Presentations](#presentations)
- [Blogs](#blogs)
- [Research](#research)
- [Moodboards](#moodboards)
- [Wireframes](#wireframes)
- [Thimble Pusher](#thimble-pusher)
- [Code Wars Profile](#code-wars-profile)
- [Website](#website)
- [Code Resources](#code-resources)
- [Broken Code](#broken-code)
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

## Website

## [Here's the app up and running on GitHub! :running:](https://dombishop.github.io/Dynamic-Web/)

The app I decided to do was based on the fact that Facebook has tons of personal data from people, and the kind of data they have is jarring. And to express that jarring factor, I picked one mundane piece of information (what device they use for the app) and contrasted that against something more personal (whether or not they have children). By using those two factors as filters, I feel I’ve recreated that jarring feeling within my app.

[I also tried to make it look as if it’s a Facebook product by looking at their branding.](https://www.sitepoint.com/fonts-colors-used-facebook-twitter-google/) The font being used on the site is “Roboto” which is the font used on Facebook's Android app. I did try to use their Mac and Windows fonts but they were locked behind copyright that I didn’t want to mess with. The blue used with the site also aligns with Facebook's branding, its #3B5998.

## Code Resources

### These are the sources that I pulled code from to develop my app:

https://www.w3schools.com/css/tryit.asp?filename=trycss_buttons_hover

https://www.w3schools.com/cssref/css3_pr_border-radius.asp

https://www.w3schools.com/tags/att_input_checked.asp

## Broken Code

This is code I would have liked to use, but I could not find a way to get it working. It would have let me find and display a persons location on a map in the app.

```js
console.log('mapbox.js ready to roll!')

// this is our "library card" to use Mapbox
mapboxgl.accessToken = 'pk.eyJ1IjoibWF0dGVvbWVuYXBhY2UiLCJhIjoiY2l2Y2lncmJ5MDAzbjJ6bDV4ZWZ1ZWkzcSJ9.ihgOtHA6TAph5UZQyESYfA'

var map = new mapboxgl.Map(
{
  // container id specified in the HTML
  container: 'map',
  // style URL
  style: 'mapbox://styles/mapbox/light-v9',
  // initial position in [long, lat] format
  center: [0.005353, 51.501597],
  // initial zoom
  zoom: 10
})

// empty list to store all the markers
var markers = [] 

function wipeMarkers()
{
  for (var i = 0; i < markers.length; i++) 
  {
    var marker = markers[i]
    marker.remove()
  }
}

function addMarkers(dataList) 
{
  // first wipe previous markers
  wipeMarkers()
  // then add new ones
  for (var i = 0; i < dataList.length; i++) 
  {
    // store the current data item in a variable
    var dataItem = dataList[i]
    // extract the data item coordinates
    var coordinates = new mapboxgl.LngLat(dataItem.longitude, dataItem.latitude)
    // create a div element for the marker
    var div = document.createElement('div')
    // add a class called 'marker' to the div
    div.className = 'marker'
    // create the custom marker
    var marker = new mapboxgl.Marker(div)
      .setLngLat(coordinates) // set the marker position
      .addTo(map) // add the marker to map
    // add the marker to the list
    markers.push(marker)
    
    // pOOpup
    // 1. update the details section with data from the selected result
    // 2. hide the results section
    // 3. show the details section
    var clickSteps = 'showDetails(resultsList['+i+'], detailsInfo); resultsSection.hide(); detailsSection.show(); '
    var popupHTML = '<a onclick="' + clickSteps + '">' + dataItem.name + '</a>'
    var popup = new mapboxgl.Popup({closeButton:false})
    popup.setHTML(popupHTML)
    marker.setPopup(popup)
  }
}
```

```js
console.log('geolocate.js ready to roll!')

// from http://www.w3schools.com/html/html5_geolocation.asp

if (navigator.geolocation) // if Geolocation is supported by your browser
{
    // then call the watchPosition function, and when you have a position, call the showPosition function
    navigator.geolocation.watchPosition(showPosition)
    // showPosition is a "callback" function, which will be called at some point in the future
} 

var userMarker = null // here is where we'll store the marker for our user

function showPosition(position) 
{
    console.log(position)
    
    // extract the latitude and longitude
    var latitude = position.coords.latitude
    var longitude = position.coords.longitude
    
    // create new Mapbox LngLat object
    var coordinates = new mapboxgl.LngLat( longitude, latitude)
    
    // create marker if it doesn't exist (in other words, if it's null)
    if (!userMarker)
    {
        // create a div element for the marker
        var div = document.createElement('div')
        // add a class called 'marker' to the div
        div.className = 'marker user'
        // create the custom marker
        userMarker = new mapboxgl.Marker(div)
        .setLngLat(coordinates) // set the marker position
        .addTo(map) // add the marker to map
    }
    else // otherwise just update its coordinates
    {
        userMarker.setLngLat(coordinates)
    }
}
```

## Code for app

### index.html

```html
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
```
### main.css

```css
html {
    font-family: 'Roboto', sans-serif;
    background: #3B5998;
}

/* hide the results and details by default */

.button {
    text-align: center;
    text-decoration: none;
    display: inline-block;
    -webkit-transition-duration: 0.4s;
    transition-duration: 0.4s;
}

.button1:hover {
    background-color: #D4D4D4;
}


#results ol {
    list-style: none;
}

#results li {
    overflow: hidden;
    cursor: pointer;
    transition: background 0.5s;
}

#results li:hover {
    background: #ccc;
}

#results img {
    max-width: 8rem;
}

#results h2 {
    line-height: 0.5;
    font-size: 2rem;
    padding-bottom: calc(8rem - 1.5rem - 10px);
}

#results, #details {
display: none;
}

#logo {
  max-width: 10rem;
}


#lineThrough {
  text-decoration: line-through;
  word-spacing: -6px;
}

h1 {
    color: #3B5998;
    text-align: center;
    padding-top: 30px;
    padding-bottom: 15px;
}

h3 {
  font-style: italic;
  padding: 30px
}

section {
    background: #FFF;
    width: 40vw;
    padding: 50px;
    height: 100vh;
    margin: auto;
    text-align: center;
}


select, button, a {
    color: #404040;
    font-size: 175%;
    border-radius: 25px;
    cursor: pointer;
}

select {
  border: 1px solid #ccc;
  border-radius: 50px;
  font-size: 16px;
  height: 34px;
  width: 268px;


}

button {
    border: none;
    width: 5vw;
    height: 50px;
    background: #E5E5E5;
}

a {
  {
  font-style: italic;
  font-size: 1.5rem;

}
```
### main.js

```js
// different ways to name variables.. which one do you prefer?
// var homeGoButton
// var homegobutton
// var home_go_button
// var goBtn
// var g

// use jQuery to select the HTML elements we're going to manipulate
// TODO wrap all these in an object, eg: var interface = { home: ... }
var homeGoButton = $('#home button')
//var homeDropdown = $('#home select')
var skillsDropdown = $('#skills')
var petsDropdown = $('#pets')
var homeSection = $('#home')
var resultsSection = $('#results')
var resultsBackButton = $('#results .back')
var resultsToggleButton = $('#results .toggle')
var resultsOL = $('#results ol')
var detailsSection = $('#details')
var detailsBackButton = $('#details .back')
var detailsInfo = $('#details #info')

// define the resultsList outside of any function
var resultsList = []

// tell the GO button to do something when we click it
homeGoButton.click( function()
{
    // 1. capture the user chosen options
    var chosenSkill = skillsDropdown.val()
    var chosenPet = petsDropdown.val()
    console.log("You picked " + chosenSkill + chosenPet)

    var filters =
    [
        {
            // favouritePet is a string, so we need a value
            key: chosenPet
        },

        {
            // chosenSkill is a number, so no need for a value
            key: chosenSkill,
            value: chosenSkill
        }
    ]

    // 2. filter+sort people by user selections
    resultsList = filterAndSortList(peopleList, filters)
    console.log(resultsList)

    // 3. show the results in the #results section
    showList(resultsList, resultsOL)

    // 4. what happens when someone clicks on a result?
    $('#results li').click( function() {
        // grab the id from the clicked item
        var resultId = $(this).attr('id')
        // use the id to get the right data
        var resultData = resultsList[resultId]
        console.log(resultData)

        // call the function showDetails()
        showDetails(resultData, detailsInfo)

        // show the details!
        resultsSection.hide()
        detailsSection.show()
    })

    // 5. show the results!
    homeSection.hide()
    resultsSection.show()
})

// tell the Back button to do something when we click it
resultsBackButton.click( function(){
   resultsSection.hide()
   homeSection.show()
})

// tell the other Back button to do something when we click it
detailsBackButton.click( function(){
   detailsSection.hide()
   resultsSection.show()
})
```

### filter.js

```js
/**
 *
 * Usage:
 *
 * var completeList = 
 * [
 *      {
 *          name: "Hillary Clinton",
 *          bakingSkills: 5,
 *          likesPets: true,
 *          party: "Hacked"
 *      },
 *      {
 *          name: "Donald Trump",
 *          bakingSkills: 0,
 *          likesPets: false,
 *          party: "Grope"
 *      }
 * ];
 * 
 * var filters = 
 * [
 *      {
 *          key: "party", 
 *          value: "Hacked"
 *      }, 
 *      {
 *          key: "likesPets"
 *          // if the value is a boolean or number
 *          // you don't need to express it
 *       }
 * ];
 *
 * filterAndSortList(completeList, filters);
 * // will return the object for Hillary
 */

/**
 * @param  {Array} - required
 * @param  {Array} - required
 * @return {Array}
 */
function filterAndSortList(completeList, filters) 
{
    // filters must be an array
    if (filters instanceof Array == false) throw 'The filters parameter must be an array'
    
    // 1. assign the whole completeList to filteredAndSortedList
    var filteredAndSortedList = completeList
    
    // 2. loop through all filters
    filters.forEach(function(filter)
    {
        // using the native JS function Array.filter to filter the array and store the result into the filteredAndSortedList
        // see https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
        filteredAndSortedList = filteredAndSortedList.filter(function(item) 
        {
            // get the item's value for the current key
            // eg. person['bakingSkills']
            // see: http://www.w3schools.com/js/js_objects.asp
            var itemValue = item[filter.key];

            // typeof will check the type of element
            // see https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof
            // it checks if the value is either a number or a boolean (ie true or false)
            if (typeof itemValue == 'number')
            {
                // if the value is a number, it will check if the number is in between 4 and 5
                var min = 4;
                var max = 5;    			
                return itemValue >= min && itemValue <= max;
            }
            if (typeof itemValue == 'boolean') 
            {
                return itemValue;
            }
            if (typeof itemValue == 'string')
            {
                return itemValue == filter.value;
            }
        });

        // using the native JS function Array.sort to sort the array and store the result in filteredAndSortedList
        // see https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort
        filteredAndSortedList = filteredAndSortedList.sort(function(itemA, itemB) 
        {
            var valueA = itemA[filter.key];
            var valueB = itemB[filter.key];

            if (typeof valueA == 'number' && typeof valueB == 'number') 
            {
                // this will sort results in descending order if the valueB - valueA is more than 0
                // or it will sort results in ascending order if the valueB - valueA is less than 0
                return valueB - valueA;
            }
        });
        
    })
    
    // 3. return the list, filtered and sorted
    return filteredAndSortedList;
}
```

### firebase.js

```js
var config =
{
    apiKey: "AIzaSyD8H2eatEERSfJq1DaTj2PylW-ed_fR0DY",
    databaseURL: "https://dynamic-web-database.firebaseio.com/"
};
firebase.initializeApp(config);

var database = firebase.database();
var peopleDatabase = database.ref('people');
var peopleList = [];

peopleDatabase.on('child_added', function( firebaseObject )
{
	var person = firebaseObject.val();
  	peopleList.push(person);
  	// "push" is JavaScript's lingo for "add to a list"
})

console.log(peopleList);
```

### plugins.js

```js
// Avoid `console` errors in browsers that lack a console.
(function() {
    var method;
    var noop = function () {};
    var methods = [
        'assert', 'clear', 'count', 'debug', 'dir', 'dirxml', 'error',
        'exception', 'group', 'groupCollapsed', 'groupEnd', 'info', 'log',
        'markTimeline', 'profile', 'profileEnd', 'table', 'time', 'timeEnd',
        'timeline', 'timelineEnd', 'timeStamp', 'trace', 'warn'
    ];
    var length = methods.length;
    var console = (window.console = window.console || {});

    while (length--) {
        method = methods[length];

        // Only stub undefined methods.
        if (!console[method]) {
            console[method] = noop;
        }
    }
}());

// Place any jQuery/helper plugins in here.
```

### show.js

```js
function makeListItemHTML (data, index) 
{
  /*
    This function creates some nice HTML around data for the #home section

    Return something like this:

    <li>
        <img src="https://ma.tteo.me/assets/surprise.png">
        <h2>Matteo</h2>
    </li>
  */

  // li = List Item
  var li  = '<li id="' + index + '">'
  + '<img src="' + data.image + '">' 
  + '<h2>' + data.name + '</h2>' 
  + '</li>'

  return li;        
}

function makeDetailsHTML (data) 
{
  /*
    This function creates some nice HTML around data for the #details section

    Return something like this:

    <h2>Matteo</h2>
    <img src="https://ma.tteo.me/assets/surprise.png">
    <p>I teach people aged 6 to 60+ how to be creative with code.
    </p>
    <a class="contact button">Contact Matteo</a>
  */

  var html = '<h2>' + data.name  + '</h2>' 
  + '<img src="' + data.image + '">' 
  + '<p>' + data.about + '</p>'
  + '<a class="contact button">Contact ' + data.name + '</a>'

  return html;        
}

// TODO refactor to updateList
function showList (dataList, interfaceList) 
{
    // update the ul content with the result of makeListHTML(list)
    // .html() is a jQuery function
    interfaceList.html( makeListHTML(dataList) ); 
}

// TODO refactor to updateDetails
function showDetails (data, interfaceElement) 
{
  var detailsHTML = makeDetailsHTML(data)
  interfaceElement.html(detailsHTML)
}

function makeListHTML (list) 
{
  var html = ''; // empty for now, we'll add HTML as we loop through the list 
  var total = list.length;

  // loop through list
  var counter = 0;
  while (counter < total) 
  {
    var data = list[counter];
    var li = makeListItemHTML(data, counter);
    
    // add the list item to the html
    html += li;
    
    // update the counter, to avoid infinite loops!
    counter = counter + 1;
  }
  return html;
}
```
