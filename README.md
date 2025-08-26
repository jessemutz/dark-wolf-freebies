# Dark Wolf Freebies - Technical Deep Dive on UI/UX

## Links and resources
### Accessibility

- [Color Contrast Grid](https://contrast-grid.eightshapes.com/?version=1.1.0&background-colors=&foreground-colors=%23FFFFFF%2C%20White%0D%0A%23F2F2F2%0D%0A%23DDDDDD%0D%0A%23CCCCCC%0D%0A%23888888%0D%0A%23404040%2C%20Charcoal%0D%0A%23000000%2C%20Black%0D%0A%232F78C5%2C%20Effective%20on%20Extremes%0D%0A%230F60B6%2C%20Effective%20on%20Lights%0D%0A%23398EEA%2C%20Ineffective%0D%0A&es-color-form__tile-size=compact&es-color-form__show-contrast=aaa&es-color-form__show-contrast=aa&es-color-form__show-contrast=aa18&es-color-form__show-contrast=dnp) - Check your entire color palette for WCAG compliance and readability
- [a11y-automation](https://a11y-automation.dev/) - An open-source project to track the potential accessibility violations and document the automated checks available for each.
- [A11y Project](https://www.a11yproject.com/) - Tons of great accessibility resources and guides
- [Mozilla Accessibility Guides](https://developer.mozilla.org/en-US/docs/Web/Accessibility) - Great guides on ARIA (Accessible Rich Internet Applications)
- [Access Lint](https://accesslint.com/) - GitHub App for accessibility linting
- [CanIUse](caniuse.com) - Browser support checker
- [PA11Y CI](https://github.com/pa11y/pa11y-ci) - Accessibility tool for CI/CD
  - More simple to integrate into pipelines.
- [Axe-core DevTools](https://www.deque.com/axe/devtools/) - More comprehensive testing. Looks like mostly paid services.
  - [Axe-core repo](https://github.com/dequelabs/axe-core)
  - [Axe-core docs](https://docs.deque.com/)
- [SA11Y CI](https://sa11y.netlify.app/overview/) - Another framework-agnostic testing tool (adds component on your front end)

With CI/CD and automated testing, the tools here [don't find all a11y issues](https://github.com/abbott567/axe-core-vs-pa11y), but it's better than nothing.

### Usability
- [Nielson Norman Group](https://www.nngroup.com/) - great usability research library
- [Never write click here](https://newvistadigital.com/blog/never-say-click-here-how-write-online-improve-seo-and-user-experience) - article on writing better links

### CSS
- [Open Props](https://open-props.style/) - Amazing a-la-carte CSS variables built by one of the senior Chrome CSS devs.
  - e.g. [normalize](https://github.com/argyleink/open-props/blob/main/src/extra/normalize.src.css)
- [Color Gradients](https://codepen.io/newvistadigital/pen/qYpYwJ)
- [OKLCH Explorer](https://oklch.com/#0.761,0.1736,129.58,100)

## Fun snippets and resources

### CSS Helpers
- [accordion-transition](./snippets/accordion-transition.css) - Better accordion to transition from height 0 to auto
- [better missing image](./snippets/better-missing-image.scss) - This is a progressive enhancement for when images are missing. It grabs the `alt` text and provides an explanation of what's going on.
- [debugger](./snippets/debugger.css) - This is WAY better than the standard `border: 1px solid red;`` method. The border adds size, which could shift items in your layout. Better to use outline so layout isn't altered.
- [insecure links](./snippets/insecure-links.css) - Any link with `target="_blank"` should have a `rel="nofollow noreferrer` for performance and security. This will highlight any external link that doesn't have these.
- [emoji cursor](./snippets/emoji-cursor.css) - you think `cursor: pointer;` is cool? What about cursor: :wolf:
- [hover (scss)](./snippets/hover.scss) - lil mixin that accounts for `:focus` and `:active` states
- [logo reel](./snippets/logo-reel.css) - make all images the same size (like in that logo reel)
- [responsive video](./snippets/responsive-video.scss) - embedding video can be wonky. No longer with this.

#### Examples of Debugger and Missing Image 

![Screenshot of debugger in action](./assets/debugger.png)
![Screenshot of missing image](./assets/image-missing.png)

