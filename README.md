## Hugo
A Go Language Static Site Generator
[Hugo](http://gohugo.io)

By default, Go Templates remove HTML comments from output. This has the unfortunate side effect of removing Internet Explorer conditional comments. As a workaround, use something like this:
```
{{ "<!--[if lt IE 9]>" | safeHTML }}
  <script src="html5shiv.js"></script>
{{ "<![endif]-->" | safeHTML }}
```

##Middleman
A Ruby on Rails Static Site Generator
[middlemanapp](https://middlemanapp.com)

By default, Middleman uses the template engine [Erubis](http://www.kuwata-lab.com/erubis/). Erubis uses `<% statement %>` by default, which conflicts with Kenscio `<% user.attribute[’name’] %>`. Either the template engine needs to be switched, or each Kenscio reference needs to be escaped.