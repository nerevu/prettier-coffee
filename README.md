# Prettier Coffeescript

Uses [prettier-plugin-coffeescript](https://github.com/helixbass/prettier-plugin-coffeescript) to prettify Coffeescript.

```
npm install -g @nerevu/prettier-coffee
prettier-coffee [options] file.coffee [file2.coffee ...]
cat file.coffee | prettier-coffee
```

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
