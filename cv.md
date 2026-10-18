---
layout: page
categories:
  - Markup
elements:
  - content
  - css
  - formatting
  - html
  - markup  
---

<style>
/* Center the specific page title with a class */
.page-title {
    text-align: center;
    font-style: normal;
}

/* Full CV link */
.cv-link {
    text-align: center;
    margin: 0 0 1.2em;
}
.cv-link a {
    display: inline-block;
    padding: 0.5em 1.2em;
    border: 1px solid currentColor;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 600;
}
.cv-link a:hover {
    opacity: 0.75;
}
</style>

<p class="cv-link">
    <a href="../assets/CV_anglais.pdf" target="_blank" rel="noopener">
        Open the full CV (PDF)
    </a>
</p>

<div style="overflow: auto; -webkit-overflow-scrolling: touch;">
    <iframe src="../assets/CV_anglais.pdf" style="width: 100%; height: 80vh;" frameborder="0"></iframe>
</div>
