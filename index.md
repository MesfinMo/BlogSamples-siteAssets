---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
list_title : Posts List
---



<div class="yml">
<pre class="prettyprint linenums">
language:<span class="c-str"> python</span>
python:
  - "2.7"
install: 
  - <span class="c-str">bundle install</span>
  - <span class="c-str">pip install awscli</span>
script:
  - <span class="c-str">bundle exec jekyll build</span>
after_success:
  - <span class="c-str">aws s3 sync --delete ./_site/assets  s3://blog-samples-site-assets --cache-control max-age=604800</span>
branches:
  only: 
    - <span class="c-str">master</span>
</pre>
</div>

<div class="cmd">
<pre class="prettyprint">
$ <span class="c-str">git init</span>
$ <span class="c-str">git add .</span>
$ <span class="c-str">git commit -m "First commit"</span>
$ <span class="c-str">git remote add origin remote git@github.com:MesfinMo/BlogSamples-siteAssets.git</span>
$ <span class="c-str">git push -u origin master</span>
</pre>
</div>