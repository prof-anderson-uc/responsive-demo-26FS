# Introduction to Responsive Design

**Web Design I · Coding Exercise**

In this exercise, you’ll use CSS to change how a page is arranged as the browser window gets narrower. You’ll start with three content boxes and a four-image gallery. Then you’ll use Flexbox, Grid, and media queries to adapt the layout for tablet and phone widths.

The same HTML is used at every width. As you work, ask yourself: **What needs to change when there’s less room?**

## What You’ll Practice

- Using **Flexbox** to arrange content boxes in a row or a column.
- Using **CSS Grid** to change how many columns a gallery has.
- Writing **media queries** that apply styles at different viewport widths.
- Testing your layout in **Live Preview** and publishing it with **GitHub Pages**.

## Get Started

1. Open the [Responsive Design template](https://github.com/prof-anderson-uc/responsive) on GitHub.
2. Click **Use this template → Create a new repository**.
3. Select your own GitHub account as the owner. Name the repository `responsive`, choose **Public**, and click **Create repository**.
4. On **your new repository**, click **Code → Open with GitHub Desktop**. Clone it into your class folder.
5. In GitHub Desktop, choose **Repository → Open in Visual Studio Code**.
6. Open `index.html` in **Live Preview** and open `styles.css` for editing. Start with the preview wide enough to see the desktop layout.

## Starter Files

| File or folder | What it contains |
| --- | --- |
| `index.html` | The page structure, including the heading, three content boxes, four gallery images, and the viewport meta tag. |
| `styles.css` | The starting styles and labeled sections for the desktop, tablet, and phone layouts. **Make your changes here.** |
| `reset.css` | The reset stylesheet, which gives the page a consistent starting point across browsers. |
| `images/` | The four images used in the gallery. |

## What You’ll Do

Follow along with the class demonstration or the videos in Canvas. Save and resize your preview as you go so you can see what each change does.

### 1. Build the Desktop Layout

Start in the **DESKTOP Layout** section of `styles.css`. Set a maximum width for the page wrapper, use Flexbox to arrange the three content boxes in a row, and use Grid to give the gallery four columns. Make sure the images can shrink to fit their columns.

### 2. Add the Media Queries

Use these two queries in `styles.css`. Try a different page background color in each one so you can see exactly when it takes effect.

```css
/* Tablet styles apply when the viewport is narrower than 768px. */
@media (width < 768px) {
   body {
      background-color: darkslategray;
   }
}

/* Phone styles go last so they can override tablet styles. */
@media (width < 480px) {
   body {
      background-color: tan;
   }
}
```

The `<` means **less than**. At exactly `768px`, the desktop layout applies. At exactly `480px`, the tablet layout applies. Below `480px`, **both queries match**, so keep the phone query after the tablet query. When both set the same property on the same selector, the later declaration wins.

**Following the videos?** The videos use the older `max-width` syntax and slightly different breakpoint numbers. Use the query lines above for this version of the exercise and follow the demonstrations for the layout changes.

### 3. Build the Tablet Layout

Inside the tablet query, change `main` from Flexbox to Grid. Put the first two boxes side by side and make the third box span both columns on the next row. Change the gallery to two columns.

### 4. Build the Phone Layout

Inside the phone query, switch `main` back to Flexbox and use `flex-direction: column` to stack the boxes. Set the gallery to one column. Follow the demonstration to adjust the margins, padding, colors, and borders for the narrower layout.

## Check Your Work

Resize the Live Preview pane or open the preview in a browser and resize the window.

| Try this width | Content boxes | Gallery |
| --- | --- | --- |
| **900px** | Three boxes in one row | Four columns |
| **650px** | Two boxes on the first row, with the third spanning the next row | Two columns |
| **400px** | Three boxes stacked vertically | One column |

- [ ] All four images load and fit within the gallery.
- [ ] The page fits at each test width without horizontal scrolling.
- [ ] The layout switches as you resize the preview in both directions.

If a style shows up at the wrong width, check the braces around your media query. Each layout rule belongs inside the query’s outer pair of braces.

## Publish and Submit

1. Save your changes in VS Code.
2. In GitHub Desktop, enter a short commit summary such as `Complete responsive layouts`. Click **Commit to main**, then **Push origin**.
3. Open your repository on GitHub and go to **Settings → Pages**. Choose **Deploy from a branch**, select **main** and **/(root)**, and click **Save**.
4. Once the site is published, open it and check the desktop, tablet, and phone layouts again.
5. Submit your **live GitHub Pages URL** in Canvas. If you named your repository `responsive`, your link will look like `https://your-username.github.io/responsive/`.

---

**Professor Eric Anderson**  
Media Communications & Technology · University of Cincinnati Blue Ash College
