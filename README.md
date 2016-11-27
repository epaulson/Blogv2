# Blog V2

Some rough development notes for BlogV2. Goal: be more #indieweb

Tech involved:
* Pelican
* github
* Medium
* Camlistore
* Jupyter 
* Pinboard
* Facebook?

## Phase 1
- Upgrade Pelican to latest release
- Consolidate posts into private repo so can have drafts etc
- Fix URL maps 
- turn on ipython/jupyter plugin
- move from github pages to S3? be nice to see 404 logs

## Phase 2
- Pelican plugin to create camli permanode for each posts
- Embed camli permanode id in html head? As text in footer with some type of rel annotation [http://microformats.org/wiki/existing-rel-values](http://microformats.org/wiki/existing-rel-values)
- Shove markdown into Camlistore
- optionally cross post to Medium
- stand up a public camli somewhere to serve as backup
- useful background:
  - http://bezdelev.com/post/hugo-aws-lambda-static-website/
  - https://aws.amazon.com/blogs/compute/dynamic-github-actions-with-aws-lambda/
  - https://github.com/danielfrg/pelican-ipynb
  - http://danielfrg.com/blog/2015/09/28/crawling-python-selenium-docker/ - a nice example of notebooks in pelican

## Phase 3
- Create link notebooks in jupyter
- Enable js preview of links - [https://groups.google.com/forum/#!topic/jupyter/ut6rDwsb_Jw](https://groups.google.com/forum/#!topic/jupyter/ut6rDwsb_Jw) or else do it in the jupyter kernel
- post links to pinboard to get related links and tags
- optionally drop in Facebook to get FB graph id
- Questions
  - link per cell?
  - how to fetch links when rerendering notebook

## Phase 4
- archive content of pages from the links 
- push links through a bounce/Interstitial page that has a pointer to the archived version as well in case the link is broken?
- or, periodically crawl links and replace anything that 404s with a static snapshot from my archive?
  - maybe keep a minhash of original and compare value of current link too? 
- see: 
  - [http://www.acuriousmix.com/2014/09/05/trying-to-scratch-a-collective-itch-a-personal-knowledgbase-part-2/](http://www.acuriousmix.com/2014/09/05/trying-to-scratch-a-collective-itch-a-personal-knowledgbase-part-2/)
  - [http://a16z.com/2015/04/15/benchling/](http://a16z.com/2015/04/15/benchling/)
  - [https://news.ycombinator.com/item?id=11009996](https://news.ycombinator.com/item?id=11009996) - Quiver, a programmers notebook

## Phase 5
- Additional content - mostly dumped into camlistore. Use schema.org in json-ld where possible
  - scanner with OCR
  - ebooks, so I remember what the hell I own
  - research papers / PDFs
  - hand-written notes
  - media (well, really just keep a list of movies)
