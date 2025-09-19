Reflecting back on our work and the usage of AI tools, we overall tended to rely on AI for MANY elements, including almost all of the CSS that makes the website look as good as it does.
However, we also jumped in when it was necessary to improve upon key details that AIs may have missed.


# Coding the website #
For the production of the entire site, we solely used ChatGPT. We were originally planning to use the GitHub Co-pilot alongside it, however ChatGPT proved themselves far beyond proficient. When we asked it to create a home page, it produced EVERYTHING we asked it for. The caveat is that you have to be incredibly specific with what you want it to produce (you also have to know how to have concise writing).


For example, when you only give it a few sentences to work off of the website happens to turn shoddy, buggy, straining to your eyes, or becomes incredibly disorganized in hierarchical structure. Here is an example of one of our first prompts, which quickly resulted in a flat neon-green website with contrasting text (Note he attached 4 images which included the website's logo and pictures from our competitor website):

`"Generate a code for this website’s homepage. The homepage’s top ui will be similar to this ui. And have the color scheme similar to this image. The same image that is used for the color scheme is also the logo. Now make the front page’s hero image the same size as the image with the 2 people in the forest, but instead of the 2 individuals in the forest it’s this image instead. Now try to somewhat replicate the homepage from https://bens30.com/ for the website I gave you. This website is called 'Bio Shield'"`


In order to mold it more to our desires, we started a new chat and planned out this very long response (note we did revise this several times prior for more specifity) (also we attached an image of the logo):

`"I would like you to write HTML code to make a website for this company. There will be four pages: the home page, products page, about page, and contact page. I have attached Bio Shield’s logo as a basis for the color scheme and page layout. Use Open Sans for the font.
First, could you code the layout home page? Here is what I would like:`

    1. A top bar where users can navigate to the four aforementioned pages. The logo should be in the top left corner at all times in this bar.
    2. For the user to be immediately greeted with a “hero image” that spans across the screen. There will be a caption in the middle which is a short sentence about Bio Shield’s eco friendly insect repellents, and right below a button that leads to the products page
    3. As the user scrolls down there will be more banners of their insect repellent, main products being shown (with name, description, and cost), listing of benefits,
    quotes from users. Section the products, benefits, and quotes by encasing them in their own highlighted boxes.
    4. Frequently asked questions at the very bottom 
`Feel free to add anything more to the homepage beyond what has been listed if you feel it will assist with making a compelling home page."`



This input (the initial variant, but still had numbered instructions like these) attained instantaneous results: the website was very pleasing, had each section in the order described, and included every detail. To our surprise, it even codes all of the JavaScript for functions like filtering products by name. 

After refining and adding more, it produced the website you see right now. From there, we moved straight to having it produce the other pages (in the same chat so we wouldn't lose the consistency of the design) with similarly formatted prompts. Each one, on the first try, created the pages also seen on the website (that means they were *really* good). However, it did gradually lose consistency after each page: by the third page, the tertiary-black color shifted into a grassy green, hovering over the navigation links switched from changing colors into underlining the text, and the size of the navigation bar became smaller. Rather than ask GPT to fix these, we decided to manually change the CSS ourselves: we did this when we hadn't learnt CSS basics yet, so trying to figure out how to change all of those features was kinda annoying and took a bit of time!

To conclude, the AI coded basically all the website; we just jumped in to fix consistency and change some UI.

# Images #
In total, we used three AI tools for generating images: Artlist, Firefly, and ChatGPT. 
We hadn't planned to use GPT initially; we relied solely on Artlist and Firefly. However, these tools were very limited. 

Artlist only allowed five free trial uses, which derailed lots of my plans. The only time we used Artlist was to create the Bio Shield logo, which honestly looked really nice. It generated that logo on the first try, too, which was very surprising. The prompt we used for Artlist went something along the lines of, "Bio Shield is an Eco-Friendly insect repellent company. Generate a logo for their brand."

Firefly generated the "hero images" you see on the home and products page. We also planned to use it for improving the logo and making products. While Firefly was dominant over other AIs in our ability to essentialy produce unlimited images, it also had a massive flaw: it mangles text horribly, and no matter what prompts you feed it, the resulting images seem to defy what you want. But if it's not asked to create anything with text, it's alright: it makes humans quickly.

Growing desperate, we turned to ChatGPT, asking it to slap the Bio Shield logo onto an unlabelled lotion bottle. *Turns out, ChatGPT is very, very good at creating images.* We used ChatGPT to create every product seen by taking pictures of products online and telling the AI to slap the Bio Shield logo ontop instead.

The only image not created by any AI tools was the background image in the about page. We grabbed that one from Google images.

# Writing #
This section refers to the writing for the product descriptions and about us page.
Yes, we also used ChatGPT. We didn't see a reason to use any other model, as GPT's writing is already decent.

With Bio Shield, we wanted to portray the brand as a company that takes pride in their eco-friendly products. For the about page, we told GPT, "a 2-3 paragraph description of Bio Shield’s philosophy and the people behind it. Tell the tale of how Bio Shield rose as a company which idealized eco-friendly insect repellents."

This produced the description you see. We were pleased with the result, and decided to leave it be.

The product descriptions were generated as the page was created.


# Log #
Below is a document log of how we used ChatGPT to produce the website, and how we jumped in to change things

ChatGPT produces the code for the home page.
- We edit descriptions and add in images. The “Hero Image” wasn’t fitting, so we manually went into the code to change its aspect ratio.
- Colors were perfect. For the most part, they were untouched.
- We did ask GPT to better section off parts.
- Manually went into the code to make it sematic

ChatGPT produces the products page
- Descriptions were weird, so we changed those.
- Inserted AI-Produced images (special thanks to Firefly)
- Had GPT produce images for all the products

ChatGPT produces the about page
- At this point, the colors and designs began growing inconsistent. We jumped in to make sure they were congruent across the site, since we knew asking it to fix them probably wouldn’t work.
- Added an image from online as the background
- We discovered that the images scale with the size of the space they're allocated to have in the grid. This problem was most prominent when using the filter, which caused the only product shown to be super-sized and take up the entire grid, making an unpleasant singular card you'd have to scroll down to full read. To fix this, we searched how to scale HTML elements and discovered that setting max-width and max-height in the CSS to px sizes will keep the sizes consistent regardless of space.

ChatGPT produces the contact page
- Structure is perfect. We make up an email and a phone number
- We had to fix the consistency again, changing colors of text and the submit button.

Changes after everything
- Scaled up the logo in the top left corner
- Made sure nav links were equally spread out and, when hovered over, had consistent designs

# Conclusion #
Our use of AI tools throughout this project demonstrates how using several AI tools together can create a visually-appealing and cohesive website. However, solely using AI is an imperfect solution, as when coding several pages for a website, it lacks the ability to apply consistent design, and when generating images, it struggles to maintain realistic design or create comprehensible text. The times we had to intervene and change code ourselves show that creators will have to possess prior knowledge about coding and perform some manual work to create a fully functional website.