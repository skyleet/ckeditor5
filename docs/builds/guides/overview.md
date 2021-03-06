---
# Scope:
# * What is it?
# * What are the use cases?
# * What is the difference with CKEditor 5 Framework?
# * What is the difference with CKEditor 4?

title: Overview
category: builds-guides
order: 10
---

CKEditor 5 Builds are a set of ready to use rich-text editors. Every "build" provides a single type of editor with a set of features and a default configuration. Our goal is to provide easy to use solutions that can satisfy a good part of the editing use cases out there.

## Builds

### Classic editor

Classic editor is what most users traditionally learnt to associate with a rich text editor — a toolbar with an editing area placed in a specific position on the page, usually as a part of a form that you use to submit some content to the server.

In CKEditor 5 the concept of the "boxed" editor was reinvented:

 * The toolbar is now always visible when user scrolls the page down.
 * The editor content is now placed inline in the page (without surrounding `<iframe>` element) — it is now much easier to style it.
 * The editor now grows automatically with the content by default.

{@img assets/img/editor-classic.png 772 Screenshot of a classic editor.}

To try it out, check the {@link examples/builds/classic-editor classic editor example}.

### Inline editor

The edited content remains a part of the page, with a floating toolbar attached:

{@img assets/img/editor-inline.png 774 Screenshot of an inline editor.}

To try it out, check the {@link examples/builds/inline-editor inline editor example}.

### Editor with balloon toolbar

The edited content remains a part of the page (like in the inline editor). The toolbar appears in a balloon next to the selection (when the selection is not empty):

{@img assets/img/editor-balloon-toolbar.png 779 Screenshot of a baloon toolbar editor.}

To try it out, check the {@link examples/builds/balloon-toolbar-editor balloon toolbar editor example}.

## How builds are designed

Each build was designed to satisfy as many use cases as possible. They differ in their UI, UX and features, and are based on the following approach:

* Include the set of features proposed by the [Editor Recommendations project](https://ckeditor.github.io/editor-recommendations/).
* Include features that contribute to creating quality content.
* Provide setups as generic as possible, based on research and community feedback.

<info-box>
	Features like fonts, colors and alignment will be introduced in the future, when the new types of builds will be introduced with the purpose of satisfying document editing scenarios.
</info-box>

### Build customization

Every build comes with a default set of features and a default configuration of them. Although the builds try to fit many cases, they may still need to be adjusted in some integrations. The following modifications are possible:

 * You can override the default **configuration of features** (e.g. define different image styles or heading levels).
 * You can change the default **toolbar configuration** (e.g. remove undo/redo buttons).
 * You can also **remove features** (plugins).

Read more in the {@link builds/guides/integration/configuration Configuration guide}.

If a build doesn't provide all the necessary features or you want create a highly optimized build of editor which will contain only the necessary features, then you need to customize the build or create a brand new one. Check {@link builds/guides/development/custom-builds Custom builds} for details on how to change the default builds to match your preferences.

## Use cases

Each of the builds fits several different use cases. Just think about any possible use for writing rich-text in applications.

The following are **some** common use cases:

* In content management systems:
	* Forms for writing articles or website content.
	* Inline writing in a front-end-like editing page.
	* In comments.
* In marketing and sales automation applications:
	* Composing e-mail campaigns.
	* Creating templates.
* In forum applications:
	* Creation of topics and their replies.
* In team collaboration applications:
	* Creation of shared documents.
* Other uses:
	* User profile editing pages.
	* Book writing applications.
	* Social messaging and content sharing.
	* Creation of ads in recruitment software.

### When NOT to use CKEditor 5 builds?

The {@link framework/index CKEditor 5 Framework} should be used, instead of builds, in the following cases:

* When you want to create your own text editor and have full control over every aspect of it, from UI to features.
* When the solution proposed by the builds does not fit your specific use case.

In the following cases [CKEditor 4](https://ckeditor.com/ckeditor-4/) should be used instead:

* When compatibility with old browsers is a requirement.
* If CKEditor 4 contains features that are essential for you, which are not available in CKEditor 5 yet.
* If CKEditor 4 is already in use in you application and you are still not ready to replace it with CKEditor 5.

<!-- TODO 1 -->
