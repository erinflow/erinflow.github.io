# Project portfolio screenshots

These are the screenshots for the 2×2 grid under **SELECTED PROJECTS** on the
Project Portfolio (Tethys) page. Drop one image per project here, named to match
the `img:` value in that page's `projects` list (in `index.html`).

| Project                                              | Filename to use                 |
|------------------------------------------------------|---------------------------------|
| CST StudioLab Data Analysis Dashboard                | `studiolab.png`                 |
| "Spoken in Plain Science" science communication tool | `spoken-in-plain-science.png`   |
| CST Event Data Analysis Dashboard                    | `event-dashboard.png`           |
| nü — NYC restaurant + bar discovery tool             | `nu.png`                        |

Each image is cropped to a 16:10 card, anchored to the top, so a wide
webpage-screenshot crop works best. Until a file is present, the striped
`[ DROP SCREENSHOT ]` placeholder shows.

## Editing the grid

The grid is data-driven. To change a project's name, link, or image, edit the
`projects:[ … ]` array on the Tethys / Project Portfolio entry in `index.html`:

```js
projects:[
  { name:'CST StudioLab Data Analysis Dashboard', url:'#', img:'studiolab.png' },
  …
]
```

- `name` — the caption shown under the screenshot (and the text link).
- `url`  — where both the image and the name link to. Use `'#'` for a project
  that isn't live yet; the card stays in place but doesn't navigate. Set a real
  `https://…` URL to make it a working link (opens in a new tab).
- `img`  — the filename in this folder.
