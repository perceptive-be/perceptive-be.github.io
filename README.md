# perceptive.be

The website of Perceptive SRL: plain HTML and one stylesheet, served by GitHub Pages from the root of `main`, at the custom domain in `CNAME`.

- No scripts, cookies, analytics or web fonts; nothing loaded from other sites.
- Links are relative, so the pages also work from a local folder. `404.html` uses root links, since GitHub serves it at any missing path.
- English is at the root, French under `fr/` and Dutch under `nl/`, with the same page names; each page links to its versions in the other two languages (the picker and the `hreflang` links). A change to the text goes in all three.
- The company details are in every page's footer and on `company/`; a change goes in all of them. The Dutch pages give the address in Dutch (Arthur Andréstraat, Sint-Pieters-Woluwe) and RPM Bruxelles.
- To preview: open `index.html` in a browser, or run `python3 -m http.server` here and open http://localhost:8000.
- To publish: commit here as usual, then send the current files as one new commit, which replaces what GitHub holds:

  ```bash
  git push --force origin "$(git commit-tree "HEAD^{tree}" -m Website):refs/heads/main"
  ```

  The full history stays in this local copy only; GitHub shows one commit. A plain `git push` is refused, since the public `main` is not part of this history. The site's Git name is set for this repository only: Perceptive SRL, mail@perceptive.be.

© 2026 Perceptive SRL. All rights reserved.
