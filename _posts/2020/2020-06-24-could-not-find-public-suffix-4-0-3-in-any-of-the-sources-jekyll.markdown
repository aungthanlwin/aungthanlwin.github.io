---
layout: "post"
title: "How to fix 'Could not find public_suffix-4.0.3 in any of the sources - Jekyll' "
date: "2020-06-24 13:34"
img: "/images/2020/06/public_suffix not found.png"
thumbnail: "/images/2020/06/public_suffix not found.png"
categories: "Jekyll blogging"

---

I was trying to build the Jekyll blog with command "bundle exec jekyll serve". But I received the errror "Could not find public_suffix-4.0.3 in any of the sources". I fixed by by running the command below ...
"bundle install".

That will install all missing packages.

![Error]({{site.baseurl}}/images/2020/06/public_suffix not found.png)
