## Technology

1. The source of the blog is on a [this repository](https://github.com/Mgccl/blog). 
2. html files are hosted on [site44](http://http://www.site44.com/). 
3. Using site44's rewrite system to direct all `/files` request to [amazon s3](http://aws.amazon.com/s3/), see `redirects.site44.txt` file.
4. The blog source is compiled by [hakyll](http://jaspervdj.be/hakyll/).
5. The content is written use my variation of [Pandoc's Markdown](http://johnmacfarlane.net/pandoc/README.html#pandocs-markdown), I call it [Xu's MathDoc](https://github.com/Mgccl/blog/blob/master/mathdoc.hs).
6. A simple rsync to sync compiled data to the blog.

## Todo

- Maybe add a CDN? (well... seriously it's not like I have 5 milion views).
- Tags (man I really don't want to spend so much time on this site)
- Compress the HTML. (Not easy, since there are math formats that doesn't allow compression.)

## Notes

- Under mac, MathDoc require you to `export LANG=C` for it to work, I have no idea why.
- Remember to set cache to amazon s3 . Say `Cache-Control` to `public, max-age=31536000`
- site44 doesn't support top level domains, you can use [wwwizer](http://wwwizer.com/naked-domain-redirect) to emulate the effect.