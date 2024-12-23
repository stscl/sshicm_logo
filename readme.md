
``` r
library(showtext)
showtext_auto(enable = TRUE)
font_add("ShineTypewriter", regular = "./ShineTypewriter-lgwzd.ttf")
library(hexSticker)
library(magick)

sticker(
  subplot = "./sshicm.png",
  s_x = 1.015,
  s_y = 1.000,
  s_width = .985,
  s_height = .985,
  package = "",
  # p_family = "ShineTypewriter",
  # p_size = 18.5,
  # p_x = 1.00,
  # p_y = 1.525,
  # p_color = "#a9fdff",
  dpi = 300,
  asp = 1,
  h_size = 2.75,
  h_color = "#404040",
  h_fill = "#404040",
  white_around_sticker = T,
  # url = "https://stscl.github.io/sshicm",
  # u_color = "#a9fdff",
  # u_size = 5.25,
  filename = "sshicm_logo.png"
)

# finally make sshicm logo background transparent
# https://uutool.cn/img-matting/

image_read('./sshicm_logo.png') |> 
  image_resize("240x278")|> 
  image_write('./sshicm_logo.png')
```

![](./sshicm_logo.png)

**Many thanks to [my friend](https://github.com/dflemore) for her
invaluable assistance in creating the core sshicm figure.**
