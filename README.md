# SlaveryStories

### Project goals

**The goal of SlaveryStories is to make it easy for people to experience primary sources about slavery in the US**. We're accomplishing this goal by making these narratives available at [http://www.slaverystories.org](http://www.slaverystories.org), where anyone can read/listen at a site that is optimized for desktop, tablet, and mobile. We think that by having better presented narratives people will find it easier to read and listen to this content.

Every narrative in this repository is also displayed at SlaveryStories.org. Any narrative that's submitted as a pull request will be added to the site. Even if you have no interest in the site feel free to pull the markup for these narratives and do with them as you wish.

### How to contribute

#### You only need to know basic HTML

Contributing is easy – all it takes is a little HTML. If you don't know HTML, don't worry – not only is it the lingua franca of the web, it's super-easy. Here's a great [resource](http://teamtreehouse.com/library/html) to get you started with it.

#### Pull the repository to your computer

To get the code, just clone the repository! And if you're new to GitHub, rest assured – it's a fantastic resource that helps people across the globe collaborate on text-based documents together! You can find a great overview on how to use GitHub [here](http://readwrite.com/2013/09/30/understanding-GitHub-a-journey-for-beginners-part-1#awesm=~ou6bN5iv8eauNX).

#### Use the template file as your guide

There's a template file located in the **narrative-template** folder that has an example of what submitted HTML files need to look like.

##### First section: *top level details*

This parts easy, it's just title, subtitle (if present), and author. If your narrative doesn't have a subtitle, just delete it that bit.


      <h1 id="title">
        TITLE GOES HERE
      </h1>

      <h2 id="subtitle">
        SUBTITLE GOES HERE
      </h2>

      <h2 id="author">
        AUTHOR GOES HERE
      </h2>

##### First section: *narrative body*

All of the body, minus footnotes goes in the "narrative" section (we'll discuss footnote markup in the next section). In the template you'll know the narrative section because it looks like this:

      <section id="narrative">
        ...
      </section>

If you're adding an audio narrative, you'll add a class of "audio."

      <section id="narrative" class="audio">
        ...
      </section>


###### Chapters

Chapters are always made with "h3" tags.

      <h3>Chapter 1: Early life in my hometown</h3>

##### Blockquotes

Use this for correpondence, letters, bills of sale, etc. Only use "h3" tags if you put a header tag in a blockquote. Make sure to wrap it in paragraph tags as seen below:

    <p>
      <blockquote>
        <p>
          Collaboratively administrate empowered markets via plug-and-play networks. Dynamically procrastinate B2C users after installed base benefits. Dramatically visualize customer directed convergence without revolutionary ROI.

          Efficiently unleash cross-media information without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar solutions without functional solutions.

          Completely synergize resource sucking relationships via premier niche markets. Professionally cultivate one-to-one customer service with robust ideas. Dynamically innovate resource-leveling customer service for state of the art customer service.
        </p>
      </blockquote>
    </p>

##### Written Songs

These are very similar to blockquotes but have sections of "stanza" included:


    <p>
      <blockquote>
        <h3>A PARODY</h3>

        <section class="stanza">
          <p>"Come, saints and sinners, hear me tell</p>
          <p>How pious priests whip Jack and Nell,</p>
          <p>And women buy and children sell,</p>
          <p>And preach all sinners down to hell,</p>
          <p>And sing of heavenly union.</p>
        </section>

        <section class="stanza">
          <p>"They'll bleat and baa, dona like goats,</p>
          <p>Gorge down black sheep, and strain at motes,</p>
          <p>Array their backs in fine black coats,</p>
          <p>Then seize their negroes by their throats,</p>
          <p>And choke, for heavenly union.</p>
        </section>

        <section class="stanza">
          <p>"They'll church you if you sip a dram,
          <p>And damn you if you steal a lamb;
          <p>Yet rob old Tony, Doll, and Sam,
          <p>Of human rights, and bread and ham;
          <p>Kidnapper's heavenly union.
        </section>
      </blockquote>
    </p>

</section>


##### Declaring Footnotes

Footnotes are pretty simple to make. See instructions below for how they are declared

    <!---
      It's an anchor link that wraps a superscript (<sup></sup>) tag. Your first footnote link will have an href of "#f1" and you'll continue adding footnotes in that sequence ("#f2", "#f3", "etc"). Make sure to add the classes "footnote-asterisk" and "link".

      You'll add the number of the footnote in the body of your superscript tag ("<sup>1</sup>", "<sup>2</sup>", etc.")
    --->

      <p>
        Efficiently unleash cross-media information <a href="#f1" class="footnote-asterisk link"><sup>1</sup></a> without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar solutions without functional solutions.
      </p>

##### Footnote body

Footnotes occupy their own "section" of the narrative file.

      <section id="footnotes">
        ...
      </section>

The body of the footnote is similar to the declaring of a footnote with a couple of differences: First, each one is wrapped in a "div." The "id" matches the "href" value used when you set the footnote in the "narrative" section. Unlike before, it doesn't involve a "#" sign.

Make sure that you use match the number between the "sup" tag with what you used in the "narrative" section

    <div>
        <p>
          <a id="f1" class="footnote-asterisk"><sup>1</sup></a>
          Collaboratively administrate empowered markets via plug-and-play networks. Dynamically procrastinate B2C users after installed base benefits. Dramatically visualize customer directed convergence without revolutionary ROI.
        </p>
    </div>

    <div>
        <p>
          <a id="f2" class="footnote-asterisk"><sup>2</sup></a>
          Proactively envisioned multimedia based expertise and cross-media growth strategies. Seamlessly visualize quality intellectual capital without superior collaboration and idea-sharing. Holistically pontificate installed base portals after maintainable products.
        </p>
    </div>


##### Attribution

Like the other sections, this one is demarcated with what you'd probably expect:

    <section id="attribution">
      ...
    </section>

Use this section to give yourself some credit as well as providing the links back to any of the original sources you may have adapted your file from.

    <p>
      This narrative was transcripted by Lorraine Mitchell. You can find the original work <a href="#">here</a>.
    </p>


### Don't:

* include page numbers – no one wants that to get in the way of their reading experience.

* use tags like:

            <b> or <i>, use <strong> and <em> instead

* submit a narrative with any attributes on elements. They just end up making the markup inconsistent.

* use try to emulate styling with tags like:

            &nbsp;

* forget to include attribution info!

### Do:

* follow the instructions in the Readme and template.

* have fun!





