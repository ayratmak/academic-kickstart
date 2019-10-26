+++
title = "Global Happiness report visualisation"
date = 2019-03-24T11:48:42+01:00
draft = true

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["global happiness","R","data visualisation"]

# Project summary to display on homepage.
summary = ""

# Slides (optional).
#   Associate this page with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references
#   `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides = ""

# Optional external URL for project (replaces project detail page).
external_link = ""

# Links (optional).
url_pdf = ""
url_code = ""
url_dataset = ""
url_slides = ""
url_video = ""
url_poster = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# links = [{icon_pack = "fab", icon="twitter", name="Follow", url = "https://twitter.com"}]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""

  ## {{< figure library="1" src="happiness.jpg" >}}
+++



## Happiness scores in Europe

Below is a visualisation for happiness levels within the region with points scaled by GDP per capita.


{{< figure src="Rplot17.png" title="" >}}

## Europe breakdown

## Happiness scores in Asia & Pacific

Let's now turn to Asia and review where individual countries stand with regards to happiness levels within the region.

{{< figure src="Rplot18.png" title="" >}}

## Happiness scores in Africa

{{< figure src="Rplot16.png" title="" >}}

## All countries

The highest happiness levels are found in Western Europe.

{{< figure src="Rplot15.png" title="" >}}

## R code

```R
mydata3 %>%  
  filter(Region2 %in% 'Asia & Pacific') %>%
  ggplot(aes(x=Happiness.Score, y=reorder(Country,Happiness.Rank), size=Economy..GDP.per.Capita.))+  
    geom_point(alpha=0.5,col="steelBlue") +
##    geom_text(aes(label=Country),nudge_x=3,label.size = 0.25) +
##    geom_label(aes(label=Country),nudge_x=3,label.size = 0.25) +
    labs(
      x = "Happiness Score",
      y = "Country",
      title = "Asia: Happiness Score by Country",
      subtitle = "Australia has the highest happiness levels",
      caption = "The World Happiness Report , 2017"
    ) +
    theme_gray() +
    theme(
      axis.ticks = element_blank(),
##      panel.grid = element_blank(),
      plot.title = element_text(size = 11),
      plot.subtitle = element_text(size = 9),
      axis.text.x=element_text(size=10,vjust=0.5),
      legend.position="none"
    ) +
    scale_colour_discrete(name="Region")
```
