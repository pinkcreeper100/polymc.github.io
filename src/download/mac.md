---
title: Download macOS
eleventyNavigation:
  key: <i class="fa fa-apple" aria-hidden="true"></i> macOS 
  order: 2
---

<div class="download-content">
    <div class="row">
    <div class="column">
      <div>
        <h1>macOS Download</h1>
        <br>
        <a class="button is-big" href="https://github.com/PolyMC/PolyMC/releases/download/{{ version.current }}/PolyMC-macOS-{{ version.current }}.tar.gz">Download (x86)</a>
        <a class="button-disabled is-big" disabled>Coming Soon (ARM)</a>
      </div>
    </div>
    <div class="column">
      {% image "Modpack Installer", "./src/img/screenshots/mac/LauncherLight.png", "./src/img/screenshots/mac/LauncherDark.png" %}
    </div>
  </div>
</div>

<div class="infobox top">

## Advanced MacOS install options

### Homebrew Package (community-maintained)

#### Installation instructions

```
brew install --cask polymc
```
</div>
