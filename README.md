# Angular Star Rating
#### Angular 1.5 Component written in typescript, based on css only techniques.

[![Bower version](https://badge.fury.io/bo/angular1-star-rating.svg)](https://badge.fury.io/bo/angular1-star-rating)
[![npm version](https://badge.fury.io/js/angular-star-rating.svg)](https://badge.fury.io/js/angular-star-rating)  
[![Package Quality](http://npm.packagequality.com/badge/angular-star-rating.png)](http://packagequality.com/#?package=angular-star-rating)

Angular Star Rating is a >1.5 Angular component written in typescript.   
It is based on a fully customizable css only star rating component written in scss. 

## DEMOS
![alt tag](https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/star-rating-options.PNG)

## Install

**Get Angular Star Rating:**
 - clone & build this repository
 - [download as .zip](https://github.com/BioPhoton/angular-star-rating/releases)
 - or via **[npm](https://www.npmjs.org/)**: by running `$ npm install angular-star-rating` from your console
 
**Load library**
```html
<script src="bower_components/ng-drupal-7-services/dist/ng-drupal-7-services.js"></script>
```

**inject it into angular**
```javascript
angular.module('myApp', ['star-rating'])
```

**Use it**
```html
<star-rating-comp
         size="'large'"
         rating="3"
         text="'Rating:'"
         on-update="crtl.onUpdate(rating)">
 </star-rating-comp>
```

## Component Properties

### @ bindings

**id**: string (Optional)  
The html id attribute of the star rating   
Default: undefined

```html
<star-rating-comp id="'my-id'"></star-rating-comp>
```

### < bindings

**text**: string (Optional)  
The text next to the stars.  
Default: undefined  

```html
<star-rating-comp text="'My text!'"></star-rating-comp>
```
**labelPosition**: starRatingPosition (Optional)  
The position of the label  
Options: top, right, bottom, left  
Default: left  

```html
<star-rating-comp label-position="'top'"></star-rating-comp>
```

<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-label-top.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-label-bottom.PNG" width="250">  
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-label-right.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-label-left.PNG" width="250">

**spread**: boolean (Optional)  
If the start use the whole space or not.  
Default: false  

```html
<star-rating-comp spread="true"></star-rating-comp>
```
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-spread-false.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-spread-true.PNG" width="250">

**numOfStars**: number (Optional)  
The possible number of stars to choose from  
Default: 5

```html
<star-rating-comp num-of-stars="6"></star-rating-comp>
```

**rating**: number (Optional)  
The actual star rating value  
Default: undefined  

```html
<star-rating-comp rating="3"></star-rating-comp>
```
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-value.PNG" width="250">

**color**: starRatingColors (Optional)  
Possible color names for the stars.  
Options: default, negative, middle, positive  
Default: undefined  

```html
<star-rating-comp color="'positive'"></star-rating-comp>
```
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-color-default.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-color-positive.PNG" width="250">  
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-color-middle.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-color-negative.PNG" width="250">

**disabled**: boolean (Optional)  
The click callback is disabled, colors are transparent   
Default: false  

```html
<star-rating-comp disabled="true"></star-rating-comp>
```

<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-disabled-false.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-disabled-true.PNG" width="250">
  
**readOnly**: boolean (Optional)  
The click callback is disabled  
Default: false  

```html
<star-rating-comp read-only="true"></star-rating-comp>
```
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-disabled-false.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-disabled-false.PNG" width="250">

**size**: starRatingSizes (Optional)  
The height and width of the stars.    
Options: small, medium, large  
Default: middle  

```html
<star-rating-comp size="'small'"></star-rating-comp>
```
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-size-small.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-size-medium.PNG" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-size-large.PNG" width="250">

**speed**: starRatingSpeed (Optional)  
The duration of the animation in ms.   
Options: immediately, noticeable, slow  
Default: noticeable  

```html
<star-rating-comp speed="'slow'"></star-rating-comp>
```

<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-animation_speed-immediately.gif" width="250">
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-animation_speed-noticeable.gif" width="250">  
<img src="https://raw.githubusercontent.com/BioPhoton/angular-star-rating/master/resources/prop-animation_speed-slow.gif" width="250">


**starType**: starRatingStarTypes (Optional)  
The type of start resource to use.     
Options: svg, icon, image  
Default: svg  

```html
<star-rating-comp star-type="'icon'"></star-rating-comp>
```
### & bindings

**getColor**: Function (Optional)  
Calculation of the color by rating.  
Params: rating, number,numOfStars and staticColor  
Return: color name  

**onClick**: Function (Optional)  
Callback function for star click event 
Params: rating

**onUpdate**: Function (Optional)  
Callback function for rating update event 
Params: rating

## Usage 
### ES5
### ES6 
### TS 
