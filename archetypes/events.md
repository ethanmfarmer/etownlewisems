
---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
---

**Insert Lead paragraph here.**

## Events

{{ range first 10 ( where .Site.RegularPages "Type" "events" ) }}
* {{ .Title }}
{{ end }}