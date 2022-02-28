# Customization

[TOC]


## CSS-Variables

This theme is highly customizable because a lot of things are parameterized with CSS variables.

Just to give you an idea on how flexible the styling is, click this button:

<div class="alter-theme-button" onclick="toggle_alternative_theme()" onkeypress="if (event.keyCode == 13) toggle_alternative_theme()" tabindex=0>Alter theme</div>

### Setup

It is recommended to add your own `custom.css` and overwrite the variables there:
```
HTML_EXTRA_STYLESHEET  = doxygen-awesome.css custom.css
```

Make sure to override the variables in the correct spot. All variables should be customized where they have been defined, in the `html` tag selector:

```css
html {
    /* override light-mode variables here */
}
```

For dark-mode overrides you have to choose where to put them, depending on wether the dark-mode toggle extension is installed or not:

- dark-mode toggle is installed:
    ```css
    html.dark-mode {
        /* define dark-mode variable overrides here if you DO use doxygen-awesome-darkmode-toggle.js */
    }
    ```
- dark-mode toggle is **NOT** installed. The dark-mode is enabled automatically depending on the system preference:
    ```css
    @media (prefers-color-scheme: dark) {
        html:not(.light-mode) {
            /* define dark-mode variable overrides here if you DON'T use doxygen-awesome-darkmode-toggle.js */
        }
    }
    ```

### Available variables

The following list gives an overview of the variables defined in [`doxygen-awesome.css`](https://github.com/jothepro/doxygen-awesome-css/blob/main/doxygen-awesome.css).

The list is not complete. To explore all available variables, have a look at the CSS starting from [here](https://github.com/jothepro/doxygen-awesome-css/blob/main/doxygen-awesome.css#L30).
All variables are defined at the beginning of the stylesheet.

| Parameter                         | Default (Light)                                             | Default (Dark)                                              |
| :-------------------------------- | :---------------------------------------------------------- | ----------------------------------------------------------- |
| **Color Scheme**:<br>primary theme colors. This will affect the entire websites color scheme: links, arrows, labels, ...                                    |||
| `--primary-color`                 | <span style="background:#1779c4;color:white">#1779c4</span> | <span style="background:#1982d2;color:white">#1982d2</span> |
| `--primary-dark-color`            | <span style="background:#335c80;color:white">#335c80</span> | <span style="background:#5ca8e2;color:white">#5ca8e2</span> |
| `--primary-light-color`           | <span style="background:#70b1e9;color:black">#70b1e9</span> | <span style="background:#4779ac;color:white">#4779ac</span> |
| **Page Colors**:<br>background and foreground (text-color) of the documentation.                                                                            |||
| `--page-background-color`         | <span style="background:white;color:black">white</span>     | <span style="background:#1C1D1F;color:white">#1C1D1F</span> |
| `--page-foreground-color`         | <span style="background:#2f4153;color:white">#2f4153</span> | <span style="background:#d2dbde;color:black">#d2dbde</span> |
| `--page-secondary-foreground-color`| <span style="background:#637485;color:white">#637485</span>| <span style="background:#859399;color:black">#859399</span> |
| **Spacing:**<br>default spacings. Most ui components reference these values for spacing, to provide uniform spacing on the page.                            |||
| `--spacing-small`                 | `5px`                                                       |                                                             |
| `--spacing-medium`                | `10px`                                                      |                                                             |
| `--spacing-large`                 | `16px`                                                      |                                                             |
| **Border Radius**:<br>border radius for all rounded ui components. Will affect many components, like dropdowns, memitems, codeblocks, ...                   |||
| `--border-radius-small`           | `4px`                                                       |                                                             |
| `--border-radius-medium`          | `6px`                                                       |                                                             |
| `--border-radius-large`           | `8px`                                                       |                                                             |
| **Content Width**:<br>The content is centered and constrained in its width. To make the content fill the whole page, set the following variable to `auto`.  |||
| `--content-maxwidth`              | `1000px`                                                    |                                                             |
| **Code Fragment Colors**:<br>Color-Scheme of multiline codeblocks                                                                                           |||
| `--fragment-background`           | <span style="background:#F8F9FA;color:black">#F8F9FA</span> | <span style="background:#282c34;color:white">#282c34</span> |
| `--fragment-foreground`           | <span style="background:#37474F;color:white">#37474F</span> | <span style="background:#dbe4eb;color:black">#dbe4eb</span> |
| **Arrow Opacity**:<br>By default the arrows in the sidebar are only visible on hover. You can override this behaviour so they are visible all the time.     |||
| `--side-nav-arrow-opacity`        | `0`                                                         |                                                             |
| `--side-nav-arrow-hover-opacity`  | `0.9`                                                       |                                                             |
| ...and many more                                                                                                                                            |||


If you miss a configuration option or find a bug, please consider [opening an issue](https://github.com/jothepro/doxygen-awesome-css/issues)!

## Doxygen generator

The theme overrides most colors with the `--primary-color-*` variables.

But there is a few small images and graphics that the theme cannot adjust or replace. To make these blend in better with
the rest, it is recommended to adjust the [doxygen color settings](https://www.doxygen.nl/manual/customize.html#minor_tweaks_colors) 
to something that matches the chosen color-scheme.

For the default color-scheme, these values work out quite well:

```
# Doxyfile
HTML_COLORSTYLE_HUE    = 209
HTML_COLORSTYLE_SAT    = 255
HTML_COLORSTYLE_GAMMA  = 113
```

## Share your customizations

If you customized the theme with custom colors, spacings, font-sizes, etc. and you want to share your creation with others, you can to this [here](https://github.com/jothepro/doxygen-awesome-css/discussions/13).

I am always curious to learn about how you made the theme look even better!

<span class="next_section_button">

Read Next: [Example](https://jothepro.github.io/doxygen-awesome-css/class_my_library_1_1_example.html)
</span>