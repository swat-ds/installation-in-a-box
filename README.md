# Hyper Local Jekyll Theme

This is a custom site for Swarthmore Libraries Book Arts exhibit Hyper Local with aspirations to be a template theme for future collections based Jekyll projects. Very similar to Wax in scope but a little lighterweight, for non-IIIF projects. While a little fiddly currently, the point is generating a customizable CSV/JSON to Collection Grid and Item views.

I may end up switching back to Wax, but the Rakefile workflow seems unnecessary for most of our small projects and the most ingenious part of Wax is IIF tile generator -- which we just don't need because we aren't always dealing with hi-res.

***light(ish)!***

- [Milligram](https://milligram.io/)
- [Normalize](https://necolas.github.io/normalize.css/)

There are more minimal approaches but this is the minimum for our requirements. Milligram chosen for `flexbox` column layout.

***features!***

- [Pagemaster](https://github.com/mnyrop/pagemaster) Thanks, Mari!
- [viewerjs](https://github.com/fengyuanchen/viewerjs)
- jQuery (sigh, just makes things easier)
- Minimal scrollview jQuery function

Things learned:

- Pagemaster (i.e., Ruby's CSV reader) is very sensitive to encoding issues. The Airtable export we use include BOM  (byte order mark) which must be removed before proper parsing.
- In VSCode can be done: (csv) by simply changing the encoding, select encoding bottom left status bar; (json) selecting and deleting the question mark left over by BOM when CSV transposed to JSON in OpenRefine
- Everyone is happier if image filenames don't include commas :information_desk_person: