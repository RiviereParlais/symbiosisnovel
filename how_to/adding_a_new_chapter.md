To add a new chapter (or page on the main site), copy the text in "template_chapter.md", and go to "content/chapters/" and "add_file/create_new_file", and name the file appropriately, such as "chapter_x.md" or "chapter_xstar.md".

Paste in the content from "template_chapter.md"

Add *stars* around any text that should be italicized, and find those pesky [^pesky_footnotes] (making sure to add them at the bottom under the ---), and then delete the link to the [next chapter], because it will fail if the next chapter doesn't exist.

To change the image used at the top, make an image you want to use. The current headers are 10X wider than tall, and I've been using 1365px wide by 135px tall. Upload the image to "static/img/image.(png/jpg)", and then modify the path and link to the image in the header info of the page.

Hit "Commit to master" and it will save the file.

To check if everything went OK, you can go to "Actions" and look for a Green Checkmark next to the highest Action.
If it shows a red X, something went wrong. 
To see what went wrong, you can "click" on the Action, then "deploy", and most likely "Build" will have the X.
Look for **ERROR**. For example, in [this example](https://github.com/rmflight/symbiosisnovel/runs/835999635?check_suite_focus=true#step:5:10), I tried to link to "chapter_2star.md", which doesn't exist, instead of "chapter-2star.md", which is the actual chapter.

If everything's green, then you can go to ".../symbiosysnovel" and the site should be updated.

Finally, go back to the **previous chapter**, and add the link to the **next chapter**

```
[Next Chapter]({{<ref "next_chapter-num.md" >}})
```


## What Does the Header Mean??

```
---
weight: 4  -- the order in the menu. Higher weight means further down, so increment by one
bookFlatSection: true  -- Not sure, don't change it
title: "The Displayed Title"  -- The title to display 
header_img: "/img/chapter_header.jpeg"  -- the path to the header image
img_link: "https://unsplash.com/@eberhardgross?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText" -- where you got the image
img_credit: "Photo: eberhard grossgasteiger on Unsplash" -- credit for the image
---
```

**Note**: If you don't want an image, make sure to leave out the 3 last pieces specific to the image.