# operator-mono-atom
Free [Operator Mono](http://www.typography.com/blog/introducing-operator) clone for Atom

A stylish way to code!

Check out the [screenshots](#screenshots).

## Installation

1. [Install fonts](#install-fonts)
1. [Configure Atom](#configure-atom)
1. [Troubleshooting](#troubleshooting)
1. [Screenshots](#screenshots)
  1. [JSX](#screenshot-jsx)
  1. [Ruby](#screenshot-ruby)
  1. [Elixir](#screenshot-elixir)
  1. [Python](#screenshot-python)

### <a name="install-fonts"></a> Install fonts

Download and install [Fira Code](https://github.com/tonsky/FiraCode) font into your system. [Installation instructions](https://github.com/tonsky/FiraCode/wiki)

Download and install [Script12 BT](https://www.myfontsfree.com/134618/script12pitchbt.htm) font into your system in the same manner. Thanks to @kencrocken for finding this font :)

The current version (last checked September 2017) of the fonts can also be found in this repository.

### <a name="configure-atom"></a> Configure Atom

#### Enable Ligatures

To use Fira Code properly you need to enable ligatures. There are two ways to do this, see below:

##### Ligatures - Quick install

Bring up Atom and go to Settings > Themes. Search for [Operator Mono](https://atom.io/themes/operator-mono) and install.

This syntax theme has been built to support this Fira Code, it is built from scratch using the Oceanic Next Italic palette and it will enable ligatures, and make certain attributes italic. It will also be your theme.

##### Ligatures - Manual install

If you prefer to use your own syntax theme, you have to edit your styles.less and insert these lines:

```
atom-text-editor {
  text-rendering: optimizeLegibility;

  &.editor .syntax--string.syntax--quoted,
  &.editor .syntax--string.syntax--regexp {
    -webkit-font-feature-settings: "liga" off, "calt" off;
  }
}
```

#### Enable "Operator Mono" font

In order to enable the alternative font for italic, which is probably what you came for, you have to manually edit your styles.less file and merge the code snippet found in `styles.less` in this repository with your own.

If you have any personal preferences, such as applying "Operator Mono" for comments as well, just add `.syntax--comment` in the css selector list.

### <a name="troubleshooting"></a> Troubleshooting

Atom version

The instructions / code works for the latest versions of Atom (1.20.x) and Atom Beta (1.21.x). Please make sure your editor is updated.

Are your ligatures not being applied correctly?

1. In Editor Settings, you might need to enter "Fira Code" in "Font Family"
1. Hunt down and disable interfering packages that modifies fonts, such as "fonts"

![Screenshot of example bad package fonts](img/fonts.png)

### <a name="screenshots"></a> Screenshots

The screenshots below are taken with the [Operator Mono](https://github.com/klippx/operator-mono) theme.

#### <a name="screenshot-jsx"></a> JSX

![Screenshot of JSX](img/JSX.png)

#### <a name="screenshot-ruby"></a> Ruby

![Screenshot of Ruby](img/ruby.png)

#### <a name="screenshot-elixir"></a> Elixir

![Screenshot of Elixir](img/elixir.png)
