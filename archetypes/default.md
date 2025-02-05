+++
date = '{{ .Date }}'
draft = true
title = '{{ replace .File.ContentBaseName "-" " " | title }}'
image = ""
github = ""
live = ""
+++

[[.Params.image | default "Image is required"]]

{{- with .Params.github }}

- [Source Code]({{ . }})
  {{- end }}

{{- with .Params.live }}

- [Live Demo]({{ . }})
  {{- end }}
