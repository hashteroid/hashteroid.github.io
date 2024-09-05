# [<img src="https://katex.org/img/katex-logo-black.svg" width="130" alt="KaTeX">](https://katex.org/)
[![[GitHub/wdsec23.github.io/static/katex/screens/8ed93424dc32541156488db0a612a18f_MD5.svg]]](https://www.npmjs.com/package/katex)
[![[GitHub/wdsec23.github.io/static/katex/screens/1e24665c52f8dd064e9eb7341513c31e_MD5.svg]]](https://github.com/semantic-release/semantic-release)
[![[GitHub/wdsec23.github.io/static/katex/screens/402aec8476b245150b4cbc5e49b8d688_MD5.svg]]](https://github.com/KaTeX/KaTeX/actions?query=workflow%3ACI)
[![[GitHub/wdsec23.github.io/static/katex/screens/7a0ddc58be0a1fa03911816cdf8b3814_MD5.svg]]](https://codecov.io/gh/KaTeX/KaTeX)
[![[GitHub/wdsec23.github.io/static/katex/screens/baae866799fb48318d0d0a2e61231cf3_MD5.svg]]](https://github.com/KaTeX/KaTeX/discussions)
[![[GitHub/wdsec23.github.io/static/katex/screens/ebacdfddb16b6dd25d73d2e4b246b48f_MD5.svg]]](https://www.jsdelivr.com/package/npm/katex)
![[GitHub/wdsec23.github.io/static/katex/screens/6b25994c3ad0c86cb53b48fa7d0b696a_MD5.svg]]
[![[GitHub/wdsec23.github.io/static/katex/screens/620be80269f3fde88ca0d4d06d1a4a9b_MD5.svg]]](https://gitpod.io/#https://github.com/KaTeX/KaTeX)
[![[GitHub/wdsec23.github.io/static/katex/screens/427355dff14bc771ab4d2b93e63fbff5_MD5.svg]]](https://opencollective.com/katex)

KaTeX is a fast, easy-to-use JavaScript library for TeX math rendering on the web.

 * **Fast:** KaTeX renders its math synchronously and doesn't need to reflow the page. See how it compares to a competitor in [this speed test](https://www.intmath.com/cg5/katex-mathjax-comparison.php).
 * **Print quality:** KaTeX's layout is based on Donald Knuth's TeX, the gold standard for math typesetting.
 * **Self contained:** KaTeX has no dependencies and can easily be bundled with your website resources.
 * **Server side rendering:** KaTeX produces the same output regardless of browser or environment, so you can pre-render expressions using Node.js and send them as plain HTML.

KaTeX is compatible with all major browsers, including Chrome, Safari, Firefox, Opera, Edge, and IE 11.

KaTeX supports much (but not all) of LaTeX and many LaTeX packages. See the [list of supported functions](https://katex.org/docs/supported.html).

Try out KaTeX [on the demo page](https://katex.org/#demo)!

## Getting started

### Starter template

```html
<!DOCTYPE html>
<!-- KaTeX requires the use of the HTML5 doctype. Without it, KaTeX may not render properly -->
<html>
  <head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.3/dist/katex.min.css" integrity="sha384-Juol1FqnotbkyZUT5Z7gUPjQ9gzlwCENvUZTpQBAPxtusdwFLRy382PSDx5UUJ4/" crossorigin="anonymous">

    <!-- The loading of KaTeX is deferred to speed up page rendering -->
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.3/dist/katex.min.js" integrity="sha384-97gW6UIJxnlKemYavrqDHSX3SiygeOwIZhwyOKRfSaf0JWKRVj9hLASHgFTzT+0O" crossorigin="anonymous"></script>

    <!-- To automatically render math in text elements, include the auto-render extension: -->
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.3/dist/contrib/auto-render.min.js" integrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous"
        onload="renderMathInElement(document.body);"></script>
  </head>
  ...
</html>
```

You can also [download KaTeX](https://github.com/KaTeX/KaTeX/releases) and host it yourself.

For details on how to configure auto-render extension, refer to [the documentation](https://katex.org/docs/autorender.html).

### API

Call `katex.render` to render a TeX expression directly into a DOM element.
For example:

```js
katex.render("c = \\pm\\sqrt{a^2 + b^2}", element, {
    throwOnError: false
});
```

Call `katex.renderToString` to generate an HTML string of the rendered math,
e.g., for server-side rendering.  For example:

```js
var html = katex.renderToString("c = \\pm\\sqrt{a^2 + b^2}", {
    throwOnError: false
});
// '<span class="katex">...</span>'
```

Make sure to include the CSS and font files in both cases.
If you are doing all rendering on the server, there is no need to include the
JavaScript on the client.

The examples above use the `throwOnError: false` option, which renders invalid
inputs as the TeX source code in red (by default), with the error message as
hover text.  For other available options, see the
[API documentation](https://katex.org/docs/api.html),
[options documentation](https://katex.org/docs/options.html), and
[handling errors documentation](https://katex.org/docs/error.html).

## Demo and Documentation

Learn more about using KaTeX [on the website](https://katex.org)!

## Contributors

### Code Contributors

This project exists thanks to all the people who contribute code. If you'd like to help, see [our guide to contributing code](CONTRIBUTING.md).
<a href="https://github.com/KaTeX/KaTeX/graphs/contributors"><img src="https://contributors-svg.opencollective.com/katex/contributors.svg?width=890&button=false" alt="Code contributors" /></a>

### Financial Contributors

Become a financial contributor and help us sustain our community.

#### Individuals

<a href="https://opencollective.com/katex"><img src="https://opencollective.com/katex/individuals.svg?width=890" alt="Contribute on Open Collective"></a>

#### Organizations

Support this project with your organization. Your logo will show up here with a link to your website.

<a href="https://opencollective.com/katex/organization/0/website"><img src="https://opencollective.com/katex/organization/0/avatar.svg" alt="Organization 1"></a>
<a href="https://opencollective.com/katex/organization/1/website"><img src="https://opencollective.com/katex/organization/1/avatar.svg" alt="Organization 2"></a>
<a href="https://opencollective.com/katex/organization/2/website"><img src="https://opencollective.com/katex/organization/2/avatar.svg" alt="Organization 3"></a>
<a href="https://opencollective.com/katex/organization/3/website"><img src="https://opencollective.com/katex/organization/3/avatar.svg" alt="Organization 4"></a>
<a href="https://opencollective.com/katex/organization/4/website"><img src="https://opencollective.com/katex/organization/4/avatar.svg" alt="Organization 5"></a>
<a href="https://opencollective.com/katex/organization/5/website"><img src="https://opencollective.com/katex/organization/5/avatar.svg" alt="Organization 6"></a>
<a href="https://opencollective.com/katex/organization/6/website"><img src="https://opencollective.com/katex/organization/6/avatar.svg" alt="Organization 7"></a>
<a href="https://opencollective.com/katex/organization/7/website"><img src="https://opencollective.com/katex/organization/7/avatar.svg" alt="Organization 8"></a>
<a href="https://opencollective.com/katex/organization/8/website"><img src="https://opencollective.com/katex/organization/8/avatar.svg" alt="Organization 9"></a>
<a href="https://opencollective.com/katex/organization/9/website"><img src="https://opencollective.com/katex/organization/9/avatar.svg" alt="Organization 10"></a>

## License

KaTeX is licensed under the [MIT License](https://opensource.org/licenses/MIT).
