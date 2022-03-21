# *My code*

##* Description: It took me a while to figure out how to solve the problem of computers not being compatible with magic packs. I am still in the learning stage of R, and I did not make too many innovations. I just tried to combine some sentences to make the whole look more concise. I think the image editing feature of R is actually interesting and will be better next time.


```r
library(magick)
library(dplyr)

imageBackground <- image_blank(width = 500, height = 60, color = "#ffffff") %>% image_annotate(text = "Salute", color = "#000000", size = 40, font = "Impact", gravity = "center")

imageAddress <- "https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.wxcha.com%2Fm00%2F85%2F40%2Ffb33180b5fcf06463b8d1ff8a5d03f6c.jpg&refer=http%3A%2F%2Fimg.wxcha.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1650424001&t=a1a6274d402cdc4764b3fcdefc4574f5"

imageMeme <- image_read(imageAddress) %>% image_scale(500)

imageAppend <- c(imageMeme, imageBackground)

meme <- image_append(imageAppend, stack = TRUE)

image_write(meme, "my_meme.png")
```


##*The link back to stats220 page*
https://dmlcl.github.io/stats220/
