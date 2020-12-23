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

## HotJar Feedback App
[github/PyRepo](github.com/rsolander/PyRepo) | 12/22/2020

I built this app to integrate with the feedback tool installed on our externally-facing sites in an effort to collect and process feedback data and responses.
Our marketing team and website owners use the app to discover patterns in the types of feedback being recieved (good vs bad) as well as where various types of feedback are coming from (are users from certain countries having a worse / better experience than others?).
The app highlights particular pages or sites that are recieving high frequencies of bad feedback, which has often led to the team discovering UX errors faster than before.

![My helpful screenshot](rsolander.github.io/hjapp_demo.gif)

Feedback responses over a certain period of time are included, along with information about the user submitting it (email, location, browser type).
These responses are grouped by the particular site or country page that they were submitted for, and these buckets are sent to site owners or managers that can act upon any action items identitfied through these responses.
I added code that utilizes SMTP to send these buckets in a weekly email, and I included a static web page interface for the marketing team where they can configure which emails recieve which site feedback.

Coded in Python and features popular libraries such as Pandas, Plotly, and Requests. Front-end is constructed by the wonderful Streamlit.io.
The app, email service, and email configuration UI are all deployed on an Amazon Web Services EC2 instance.
