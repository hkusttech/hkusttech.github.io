---
title: Media Folder
headless: true
---



{{ $page := . }}
{{ with .Site.GetPage "section" "images" }}
  {{ with .Resources.GetByPrefix $page.Params.imagename }}
    {{ $image200x := (.Resize "200x") }}
    {{ $image400x := (.Resize "400x") }}
    <img src="{{ $image200x.RelPermalink }}">
    <img src="{{ $image400x.RelPermalink }}">
    <br />
  {{ end }}
{{ end }}
