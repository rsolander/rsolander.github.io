## Welcome to Rsolander's Project Page

You can use the [editor on GitHub](https://github.com/rsolander/rsolander.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/rsolander/rsolander.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

---

## Making sense of 2020
_No Repo Available | 12/22/2020_

Can the collective mindset of a group of people be detrimental to preventing the spread of coronavirus?

I collected US county population data, US county confirmed covid case data, and US county voting data (in the 20202 election) to see if anti-mask idiosyncrasies demonstrated by a group of people results in the amplified spread of coronavirus.
While to most this may seem obvious, there are still people who doubt the effectiveness of mask-wearing and other recommended precautions, and I'm hoping that my study can help further reinforce the science behind these measures.

I represented the "groups of people" with the ~3000 counties in the united states, and I used voting results in the 2020 election as an indicator for how these counties approached coronavirus.

> "From the moment President Trump announced recommendations from the Centers for Disease Control and Prevention to wear a face covering, he made clear that he did not personally like the idea. Early on, he made negative comments about masks and criticized people who wore them, and he has routinely refused to don one himself, even in places where mask use is required (though he did allow himself to be photographed in a mask for the first time last week, when he visited the Walter Reed National Military Medical Center). He is not alone among Republican officials in eschewing masks or downplaying their benefits, behavior that political scientists believe has encouraged a partisan split in who wears masks."

_From <https://www.nytimes.com/interactive/2020/07/17/upshot/coronavirus-face-mask-map.html>_

I don't believe that everyone who voted republican is anti-mask and anti-science, but there is significant evidence that it's an indicator for that sentiment:

> In general, Republicans are more likely to live in states with less population density, and in places that have had laxer rules about masks and lower rates of coronavirus infections, at least early in the pandemic. But research from a team that includes Shana Gadarian, an associate professor of political science at Syracuse University, has found that your political party is a better predictor of mask use than any other factor they measured. Her team compared people of the same age and living in the same ZIP code, and found partisan differences in mask behavior.

Quote from somewhere.
![Covid Vs Voting](rsolander.github.io/cov_vote_12_22.PNG)

---

## HotJar Feedback App
_[rsolander/PyRepo](github.com/rsolander/PyRepo) | 12/22/2020_

I built this app to integrate with the feedback tool installed on our externally-facing sites in an effort to collect and process feedback data and responses.
Our marketing team and website owners use the app to discover patterns in the types of feedback being recieved (good vs bad) as well as where various types of feedback are coming from (are users from certain countries having a worse / better experience than others?).
The app highlights particular pages or sites that are recieving high frequencies of bad feedback, which has often led to the team discovering UX errors faster than before.

![My helpful screenshot](rsolander.github.io/hjapp_demo.gif)

Feedback responses over a certain period of time are included, along with information about the user submitting it (email, location, browser type).
These responses are grouped by the particular site or country page that they were submitted for, and these buckets are sent to site owners or managers that can act upon any action items identitfied through these responses.
I added code that utilizes SMTP to send these buckets in a weekly email, and I included a static web page interface for the marketing team where they can configure which emails recieve which site feedback.

Coded in Python and features popular libraries such as Pandas, Plotly, and Requests. Front-end is constructed by the wonderful Streamlit.io.
The app, email service, and email configuration UI are all deployed on an Amazon Web Services EC2 instance.
