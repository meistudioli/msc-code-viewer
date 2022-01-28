# msc-code-viewer

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/msc-web-push) [![DeepScan grade](https://deepscan.io/api/teams/16372/projects/20025/branches/532018/badge/grade.svg)](https://deepscan.io/dashboard#view=project&tid=16372&pid=20025&bid=532018)

As a web developer, show some demo code is a very common stuff. There are so many syntax highlighting libraries for the Web. highlight.js is one of the popular library. It is easy to use and there are so many themes for it. To make it more suitable for me, I wrap highlight.js and GitHub light / dark themes as a web component and named it &lt;msc-code-viewer />. With &lt;msc-code-viewer /> syntax highlighting is a piece of cake. It will switch light / dark mode as user preference. Of course「COPY」feature has already built-in.

![<msc-web-push />](https://blog.lalacube.com/mei/img/preview/msc-code-viewer.png)

## Basic Usage

&lt;msc-code-viewer /> is a web component. All we need to do is put the required script into your HTML document. Then follow &lt;msc-code-viewer />'s html structure and everything will be all set.

- Required Script

```html
<script
  type="module"
  src="https://your-domain/wc-msc-code-viewer.js">        
</script>
```

- Structure

Put the content inside &lt;msc-code-viewer /> as its child. It will have highlighting content.

```html
<msc-code-viewer>
  <!-- Syntax highlighting content -->
  <style>
  body, .usertext {
    color: #F0F0F0; background: #600;
    font-family: Chunkfive, sans;
    --heading-1: 30px/32px Helvetica, sans-serif;
  }
  </style>
</msc-code-viewer>
```

## JavaScript Instantiation

&lt;msc-code-viewer /> could also use JavaScript to create DOM element. Here comes some examples.

```html
<script type="module">
import { MscCodeViewer } from 'https://your-domain/wc-msc-code-viewer.js';

// use DOM api
const nodeA = document.createElement('msc-code-viewer');
document.body.appendChild(nodeA);
nodeA.textContent = `
Show me the money
`;

// new instance with Class
const nodeB = new MscCodeViewer();
document.body.appendChild(nodeB);
nodeB.textContent = `
Show me the money
`;
</script>
```

## Style Customization

&lt;msc-code-viewer /> uses CSS variables to style its interface. That means developer could easy change them into the lookup you like.

```html
<style>
msc-code-viewer {
  --msc-code-viewer-border-radius: 16px;
}
</style>
```

## Property

| Property Name | Type | Description |
| ----------- | ----------- | ----------- |
| value | String | Getter / Setter for value. Developers could use this property to setup syntax highlighting. |


## Event

| Event Signature | Description |
| ----------- | ----------- |
| msc-code-viewer-mutate | Fired when <msc-code-viewer-mutate /> mutated. |

## Reference
- [&lt;msc-code-viewer /&gt;](https://blog.lalacube.com/mei/webComponent_msc-code-viewer.html)
