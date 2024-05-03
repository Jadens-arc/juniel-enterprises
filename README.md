# Juniel Enterprises Official Website

Designed By [Jaden Arceneaux](https://github.com/jadens-arc). Made using the [Hugo framework](https://gohugo.io/)

## How to make changes

All pages are stored in the `content` folder

### Making a new page

To create a new page simply create a new file in this folder

Example:

```
AmaVoice.md
ProactiveEd.md
TravelDRx.md
NewPage.md        + our new page
```

This will automatically generate a card on the homepage

### Customizing the homescreen card

At the top of the new page you must specify a few attributes of this page to describe how it will look as a card on the homescreen (must be surrounded by plus signs, copy and paste if necessary).

```hugo
+++
title = 'New Page'
description = 'The greatest new page this world has ever seen'
+++
```

### Adding content to a page

#### Plain Text

Beneath the bottom plus signs you can start writing content for your page

```hugo
+++
title = 'New Page'
description = 'The greatest new page this world has ever seen'
+++

Welcome to our newest addition to Juniel Enterprises, where we introduce you to a world of unparalleled innovation and excellence. We're thrilled to unveil something truly spectacular, a page that sets new benchmarks in creativity and utility. Here, we've poured our passion, expertise, and vision into creating a space that not only delights but inspires.

Thank you for visiting. Explore, enjoy, and let us know how this one-of-a-kind page sparks joy in your day!
```

This will just be simple plain text on the page

#### Rowcards (the things with images)

If you're wondering how to get those fancy cards with the images next to them this is the section for you

You declare whats called a row card

```hugo
{{< rowcard >}}
```

it follows the following format

| Attribute   | meaning                                                                                                                    |
| ----------- | -------------------------------------------------------------------------------------------------------------------------- |
| url         | The url of the image you want to use in the card. Must be in quotation marks                                               |
| reversed    | Either true or false. True puts the image on the left side of the card, false puts it on the right. Not in quotation marks |
| title       | The title (bold text) on the card. In quotation marks                                                                      |
| description | The body paragraph of the card. In quotation marks                                                                         |

Here it is, integrated into our example

```hugo
+++
title = 'New Page'
description = 'The greatest new page this world has ever seen'
+++

Welcome to our newest addition to Juniel Enterprises, where we introduce you to a world of unparalleled innovation and excellence. We're thrilled to unveil something truly spectacular, a page that sets new benchmarks in creativity and utility. Here, we've poured our passion, expertise, and vision into creating a space that not only delights but inspires.

{{< rowcard
url="https://images.pexels.com/photos/4260325/pexels-photo-4260325.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
reversed=false
title="Wowie zowie"
description="Our latest addition to the Juniel Enterprises portfolio promises to revolutionize the way you think about innovation. " >}}

Thank you for visiting. Explore, enjoy, and let us know how this one-of-a-kind page sparks joy in your day!
```

### A Note on Images

For rowcards when you're defining the url for the image. If it's an external image from a different website just put the full url like "https://jadenarceneaux/logo.png". If you'd like to upload you're own image simply upload the image to the `static` folder and set the url to forwardslash + the name of your image (e.g "/super-cool-image.png")
