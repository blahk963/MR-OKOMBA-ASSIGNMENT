# 3D CSS Animations: Car, Moon and Bouncing Ball

Three 3D animations built with pure HTML and CSS, all in a single page. A small switcher at the top lets you flip between them. The only JavaScript is a few lines that handle the switcher.

**Live demo:** https://blahk963.github.io/MR-OKOMBA-ASSIGNMENT/
NAME: OLANIPEKUN TAYE TOBI
MATRIC NO: CPE/2021/1050

## The scenes

| Scene | What it shows |
| --- | --- |
| **Car** | A 3D red car (built from CSS boxes) driving along a road, with spinning wheels. |
| **Moon** | A shaded moon with rotating craters, travelling in an arc that moves it toward and away from the viewer. |
| **Ball** | A ball bouncing on a perspective checkered floor, with squash on impact and a shadow that shrinks as the ball rises. |

You can link straight to a scene by adding its name to the URL:

- `.../#car`
- `.../#moon`
- `.../#ball`

## Run it locally

No install or build step is needed.

1. Download or clone this repo.
2. Open `index.html` in any modern browser.

In VS Code you can also use the **Live Server** extension and click "Go Live".

## Deploy on GitHub Pages

1. Push this repo to GitHub, with `index.html` in the root folder.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, set the source to **Deploy from a branch**.
4. Choose your main branch and the `/ (root)` folder, then save.
5. After a minute or two, your site is live at the link GitHub shows.

If you still see an old version after pushing, hard refresh with `Ctrl+Shift+R` (`Cmd+Shift+R` on Mac).

## Project structure

```
.
├── index.html   # all three scenes, their CSS and the switcher script
└── README.md
```

Each scene lives in its own `<section>` (`#car`, `#moon`, `#ball`), and its CSS is scoped to that section so the styles don't clash. Only the visible scene is rendered, so hidden scenes don't run their animations.

## Customise

Look for these in the CSS inside `index.html`:

| What to change | Where |
| --- | --- |
| Car speed | `animation: car-drive 8s` in `#car .vehicle` |
| Car colour | the reds (`#d62828`, `#b01f1f`, `#c1121f`, `#ef4b4b`) in `#car .hull` |
| Moon travel speed | `animation: moon-travel 14s` in `#moon .orbit` |
| Moon size | `width` and `height` in `#moon .moon` |
| Ball bounce speed | `1.2s` in `#ball .bounce`, `#ball .sphere` and `#ball .shadow` (keep all three the same) |
| Ball bounce height | `-36vh` in `@keyframes ball-bounce` |
| Ball colour | the gradient colours in `#ball .sphere` |

## Browser support

Works in current versions of Chrome, Edge, Firefox and Safari. It uses CSS 3D transforms, `perspective`, `conic-gradient` and `@keyframes`.

If your system is set to reduce motion, the animations run much slower.

## Licence

Free to use, copy and modify.
