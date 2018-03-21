---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
list_title : Posts List
---

<h1>Hello</h1>
<div class="yml">
<pre class="prettyprint linenums">
language: <span class="c-str">python</span>
python:
  - "2.7"
install: 
  - <span class="c-str">bundle install</span>
  - <span class="c-str">pip install awscli</span>
script:
  - <span class="c-str">bundle exec jekyll build</span>
after_success:
  - <span class="c-str">aws s3 sync --acl public-read --sse --delete ./_site/assets  s3://blog-samples-site-assets --cache-control max-age=604800</span>
branches:
    only: 
        - <span class="c-str">master</span>
</pre>
</div>


<h1>Hello again</h1>
<pre class="prettyprint linenums">
<span class="pun">language</span>: <span class="c-str">python</span>
<span class="pun">python</span>:
  - "2.7"
<span class="pun">install</span>: 
  - <span class="c-str">bundle install</span>
  - <span class="c-str">pip install awscli</span>
<span class="pun">script</span>:
  - <span class="c-str">bundle exec jekyll build</span>
<span class="pun">after_success</span>:
  - <span class="c-str">aws s3 sync --acl public-read --sse --delete ./_site/assets  s3://blog-samples-site-assets --cache-control max-age=604800</span>
<span class="pun">branches</span>:
  <span class="pun">only</span>: 
    - <span class="c-str">master</span>
</pre>

