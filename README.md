# SlaveryStories.org

### Project goals

**The goal of SlaveryStories.org is to make it easy for people to discover and read true stories about slavery in the US from the perspective of the slaves themselves**.

We're accomplishing this goal by making these stories available at [slaverystories.org](http://www.slaverystories.org), where anyone can read/listen to stories on a site that is optimized for desktop, tablet, and mobile. We think that by providing a better online experience people will find it easier to read and listen to this content.

Every narrative in this repository is displayed on SlaveryStories.org. We also encourage others to submit narratives that will be added to the site as well. To contribute a narrative follow the instructions below.

### How to contribute

#### Contributing takes only 3 steps:

1. Fork this repository
2. Create a narrative using our HTML template included in the repository
2. Submit the narrative back to this repository via a pull request

#### ** Prerequisites to contribute **

 1. **Have git installed**:   [You an use this easy guide to get set up.](https://github.com/scholastica/slave-narratives/wiki/Installing-Git-and-or-Github-Apps)
 2. **Understand Basic HTML**: If you don't know HTML, don't worry – not only is it the lingua franca of the web, it's super-easy. There's a great resource to get you started [here](http://teamtreehouse.com/library/html).

### Step 1: Fork this repository

To get started, begin by [forking this repository](https://help.github.com/articles/fork-a-repo). This will create a **copy** of all files in the repository and allow you to add additional narratives.  Simply click the "Fork" button in top right corner of this repository to make your own clone of the repository:

![](https://github-images.s3.amazonaws.com/help/bootcamp/Bootcamp-Fork.png)

Once you've forked the repository, you should now have a new repository listed under your own github account  **(e.g. github.com/your-username/slave-narratives )**.

Next, simply clone your forked repository to your computer using github's "Clone to Desktop" link.

![](https://github-images.s3.amazonaws.com/windows/repository/windows-clone-in-desktop.png)

**Next, you can begin adding a new narrative**

### Step 2:  Creating a narrative using our HTML Template.

Inside your cloned repo  you'll see a template file located in the **narrative-template** folder that has an example of what submitted HTML files need to look like.

**Let's walk through the template so you can understand whats required:**

####  Title, Subtitle, & Author

This parts easy, it's just title, subtitle (if present), and author. If your narrative doesn't have a subtitle, just delete that bit.
  ```html
      <h1 id="title">
        TITLE GOES HERE
      </h1>

      <h2 id="subtitle">
        SUBTITLE GOES HERE
      </h2>

      <h2 id="author">
        AUTHOR GOES HERE
      </h2>
  ```

#### Narrative body

All of the body text, minus footnotes goes in the "narrative" section (we'll discuss footnote markup in the next section). In the template you'll know the narrative section because it looks like this:
  ```html
      <section id="narrative">
        ...
      </section>
  ```

If you're adding an audio narrative,  be sure to add a class of "audio" to the narrative html section
  ```html
      <section id="narrative" class="audio">
        ...
      </section>
  ```

####  Declaring Chapters

Chapters are always made with "h3" tags.
  ```html
      <h3>Chapter 1: Early life in my hometown</h3>
  ```

#### Blockquotes

Use this for correpondence, letters, bills of sale, etc. Only use "h3" tags if you put a header tag in a blockquote. Make sure to wrap it in paragraph tags as seen below:
  ```html
    <p>
      <blockquote>
        <p>
          Collaboratively administrate empowered markets via plug-and-play networks. Dynamically procrastinate B2C users after installed base benefits. Dramatically visualize customer directed convergence without revolutionary ROI.

          Efficiently unleash cross-media information without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar solutions without functional solutions.

          Completely synergize resource sucking relationships via premier niche markets. Professionally cultivate one-to-one customer service with robust ideas. Dynamically innovate resource-leveling customer service for state of the art customer service.
        </p>
      </blockquote>
    </p>
  ```

#### Written Songs

These are very similar to blockquotes but have sections of "stanza" included:

  ```html
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
 ```

#### Declaring Footnotes

**Footnote Links**
Footnotes are pretty simple to make. Within the body text, a footnote is an anchor link that wraps a superscript (<sup></sup>) tag. Like this:

    ```html
     <a href="#f1" class="footnote-asterisk link"><sup>1</sup></a>
    ```
 Your first footnote link will have an href of "#f1" (like the example above) and you'll continue adding footnotes in that sequence ("#f2", "#f3", "etc"). Make sure to add the classes "footnote-asterisk" and "link".

  ```html
      <p>
        Efficiently unleash cross-media information <a href="#f1" class="footnote-asterisk link"><sup>1</sup></a> without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar solutions without functional solutions.
      </p>
  ```
**Footnote Content**

The text of each footnotes are declared within their own "section" within the template:
  ```html
      <section id="footnotes">
        ...
      </section>
  ````

The body of the footnote is similar to the declaration of a footnote with a couple of differences:  First, each one is wrapped in a "div" and the "id" must match the "href" value used when you set the footnote in the "narrative" section.

Make sure that you match the number between the "sup" tag with what you used in the "narrative" section. Here's an example:

  ```html
     <section id="footnotes">
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
    </section>
  ```


#### Attribution

Like the other sections, this one is demarcated with what you'd probably expect:
  ```html
    <section id="attribution">
      ...
    </section>
  ```

Use this section to give yourself some credit as well as providing the links back to any of the original sources you may have adapted your file from.

 ```html
    <p>
      This narrative was transcripted by Lorraine Mitchell. You can find the original work <a href="#">here</a>.
    </p>
 ```

### Step 3:  Submit a Pull Request

![](https://github-images.s3.amazonaws.com/help/pull_requests/pullrequest-send.png)

Once you've created a narrative using the above template you're now ready to make a Pull Request. There are two steps:

 1.  [Follow these instructions to commit your changes to your forked repository](https://help.github.com/articles/fork-a-repo#push-commits).

 2.  [Follow these instructions to create pull request from your forked repository](https://help.github.com/articles/creating-a-pull-request)

** Once your pull request has been sent we'll review it and see that it's added to SlaveryStories.org!**


### Some Do's and Dont's

#### Don't:

* include page numbers – no one wants that to get in the way of their reading experience.

* use tags like:
  ```html
      <b> or <i>, use <strong> and <em> instead
  ```

* submit a narrative with any attributes on elements. They just end up making the markup inconsistent. For example don't do:

  ```html
     <p class="make-bigger"></p>
  ```

* try to emulate styling with tags like:  `&nbsp;`

* forget to include attribution info!

#### Do:

* keep your markup as simple as possible – it should mostly just consist of "paragraph" elements and "h3" chapter headings

* follow the instructions in the Readme and template.

* have fun & thank you! 

# License

This repository is licensed under the
[Creative Commons Attribution 3.0 license](http://creativecommons.org/licenses/by/3.0/us/deed.en_US),
and the underlying source code used to format and display content on SlaveNarratives.org
is licensed under the [MIT license](http://opensource.org/licenses/mit-license.php).
