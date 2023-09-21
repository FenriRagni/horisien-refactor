# Horiseon-Refactor

## Technology Used 

| Technology Used         | Resource URL           | 
| ------------- |:-------------:| 
| HTML    | [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) | 
| CSS     | [https://developer.mozilla.org/en-US/docs/Web/CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)      |   
| Git | [https://git-scm.com/](https://git-scm.com/)     |    

## Description 
This project involved research into accessibility standards in HTML in order to meet those standards without changing the look of the website itself. This was done through the use of semantic elements available in HTML. I also consolidated the classes and element stylings in the CSS file.

[Visit the Deployed Site](https://fenriragni.github.io/horisien-refactor/)
![Site Langing Page](./assets/images/fenriragni.github.io_horisien-refactor_.png)


## Table of Contents

* [Code Refactor Example](#code-refactor-example)
* [Usage](#usage)
* [Learning Points](#learning-points)
* [Author Info](#author-info)
* [Credits](#credits)
* [License](#license)


## Code Refactor Example

```html
  <div class="benefits">
        <div class="benefit-lead">
            <h3>Lead Generation</h3>
            <img src="./assets/images/lead-generation.png" />
            <p>
                Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
            </p>
        </div>
        <div class="benefit-brand">
            <h3>Brand Awareness</h3>
            <img src="./assets/images/brand-awareness.png" />
            <p>
                Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.
            </p>
        </div>
        <div class="benefit-cost">
            <h3>Cost Management</h3>
            <img src="./assets/images/cost-management.png" />
            <p>
                As the search ranking for your business increases, your advertising costs decrease, and you no longer need to advertise your page.
            </p>
        </div>
    </div>
```

Converting the above non-semantic div with the class of 'benefits' to an appropriate [semantic element](https://www.w3schools.com/html/html5_semantic_elements.asp). 

```html
<aside class="benefits">
        <section>
            <h3>Lead Generation</h3>
                <img src="./assets/images/lead-generation.png" alt="image of half a gear pointing to money"/>
                    <p>
                        Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
                    </p>
        </section>

        <section>
            <h3>Brand Awareness</h3>
                <img src="./assets/images/brand-awareness.png" alt="image of a lightbulb wearing a suit"/>
                    <p>
                        Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.
                    </p>
        </section>
        <section>
            <h3>Cost Management</h3>
                    <img src="./assets/images/cost-management.png" alt="image of a gear surrounded by money"/>
                        <p>
                            As the search ranking for your business increases, your advertising costs decrease, and you no longer need to advertise your page.
                        </p>
        </section>
    </aside>
```

This change require some additional modification to the CSS selector: 

```css
.benefits {
    margin-right: 20px;
    padding: 20px;
    clear: both;
    float: right;
    width: 20%;
    height: 100%;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #2589bd;
}

.benefit-lead {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-brand {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-cost {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-lead h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-brand h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-cost h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-lead img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-brand img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}

.benefit-cost img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}
```

No longer targeting the element on the page with the three different classes but instead the css selector targeting a single 'benefits' class and consolidating similar attributes

```css
.benefits {
    margin-right: 20px;
    padding: 20px;
    clear: both;
    float: right;
    width: 20%;
    height: 100%;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #2589bd;
    margin-bottom: 32px;
    color: #ffffff;

}

.benefits h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefits p {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefits img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}
```

## Usage 
Provide instructions and examples for use. Include screenshots as needed. 

To add a screenshot, create an `assets/images` folder in your repository and upload your screenshot to it. Then, using the relative filepath, add it to your README using the following syntax:

```md
![alt text](assets/images/screenshot.png)
```


## Learning Points 


This is a good place to Explain what you Learned by creating this application.
This is a great way to remind about all of the Complex Skills you now have.
If the user is less experienced than you:
They will be impressed by what you can do!

If the user is more experienced than you:
They will be impressed by what you can do!

Remember, it is easy to forget exactly how Valuable and Impressive your skills are, as well as How Much You’ve Learned!
So quantify that here!


## Author Info

```md
### Farley Wittles 


* [Portfolio](https://youtu.be/bHX54GCrDB4)
* [LinkedIn](https://youtu.be/bHX54GCrDB4)
* [Github](https://youtu.be/bHX54GCrDB4)
```

The user has looked through your whole README, and gotten familiar with your application. 
This is where you take credit, and make it easy for them to learn more about you!
Direct them to the following:
- Your GitHub Profile
- Your LinkedIn
- Your Portfolio Website
- And Anything Else You Want!

Give credit where credit is due! 

If you Pseudocode or Pair Program with someone else, give them kudos in your Contributors section!


## Credits

List your collaborators, if any, with links to their GitHub profiles.

If you used any third-party assets that require attribution, list the creators with links to their primary web presence in this section.

If you followed tutorials, include links to those here as well.


## License

The last section of a good README is a license. This lets other developers know what they can and cannot do with your project. If you need help choosing a license, use [https://choosealicense.com/](https://choosealicense.com/)


---

🏆 The sections listed above are the minimum for a good README, but your project will ultimately determine the content of this document. You might also want to consider adding the following sections.

## Badges

![badmath](https://img.shields.io/github/languages/top/nielsenjared/badmath)

Badges aren't _necessary_, per se, but they demonstrate street cred. Badges let other developers know that you know what you're doing. Check out the badges hosted by [shields.io](https://shields.io/). You may not understand what they all represent now, but you will in time.

## Features

If your project has a lot of features, consider adding a heading called "Features" and listing them there.

## Contributing

If you created an application or package and would like other developers to contribute it, you will want to add guidelines for how to do so. The [Contributor Covenant](https://www.contributor-covenant.org/) is an industry standard, but you can always write your own.

## Tests

Go the extra mile and write tests for your application. Then provide examples on how to run them.

---

© 2023 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.