{{- $description := .Description | default (.Summary | plainify | htmlUnescape | truncate 200) -}}
---
title: {{ .Title | jsonify }}
date: {{ .Date.Format "2006-01-02" }}
{{- with $description }}
description: {{ . | jsonify }}
{{- end }}
---

{{ .RawContent }}