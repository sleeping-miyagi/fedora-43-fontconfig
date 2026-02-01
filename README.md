# fedora-43-fontconfig

## Broken CJK

Fedora 43 KDE has [some issues with Noto Sans CJK not rendering properly](https://ani.social/post/26202606). Replacing the font with something else was the easiest and cleanest way for me to "fix" it.

For Japanese --> [BIZ UDP](https://fonts.google.com/specimen/BIZ+UDPGothic)

```
sudo dnf install mrsw-biz-*
```

For Korean --> [Naver Nanum](https://hangeul.naver.com/font)

```
sudo dnf install naver-nanum-*
```

Then copy `00-preferred-fonts.conf` to `~/.config/fontconfig/conf.d/`.

## MS Fonts

This script builder makes installing MS Fonts easy: https://github.com/k-mktr/fedora-things-to-do

Then copy `01-disable-embedded-bitmap-for-msfonts.conf` to fix MS fonts with no antialiasing (see [ArchWiki Disabling embedded bitmap fonts](https://wiki.archlinux.org/title/Microsoft_fonts#Disable_embedded_bitmap_fonts)).
