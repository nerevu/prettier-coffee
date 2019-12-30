[![Build Status](https://travis-ci.org/nerevu/html2hs.svg?branch=master)](https://travis-ci.org/unframework/html2hs)

# Convert Legacy HTML to Hyperscript

Automatically translate old HTML markup into the new Hyperscript markup embeddable directly inside your component Javascript code.

Use this for hand-converting legacy project source code (e.g. AngularJS templates): care is taken to preserve original whitespace and even comments. For dynamic serving and CI builds check out https://github.com/alexmingoia/jsx-transform instead.

```
npm install -g @nerevu/prettier-coffee
prettier-coffee [options] file.coffee [file2.coffee ...]
cat file.coffee | prettier-coffee
```

See [prettier-plugin-coffeescript](https://github.com/helixbass/prettier-plugin-coffeescript#configuration) for available options

Coffeescript goes in:

```coffee
m 'table.sample-html', [
  m('tr', [
    m('th', 'Pandas')
    m('th', 'Kittens')
    m('th', 'Hedgehogs')
  ])
  m('tr', [
    m('td', 'foo')
    m('td', 'bar')
    m('td', 'baz')
  ])
  m('tr', [
    m('td', '32')
    m('td', '45')
    m('td', '83')
  ])
  m('tr', [
    m('td', 'onomatopoeia')
    m('td', 'schadenfreude')
    m('td', 'antidisestablishmentarianism')
  ])
]
```

prettified Coffeescript comes out:

```coffee
m "table.sample-html", [
  m "tr", [m("th", "Pandas"), m("th", "Kittens"), m "th", "Hedgehogs"]
  m "tr", [m("td", "foo"), m("td", "bar"), m "td", "baz"]
  m "tr", [m("td", "32"), m("td", "45"), m "td", "83"]
  m "tr", [
    m "td", "onomatopoeia"
    m "td", "schadenfreude"
    m "td", "antidisestablishmentarianism"
  ]
]
```
