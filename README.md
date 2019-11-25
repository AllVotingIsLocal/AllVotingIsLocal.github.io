title: Welcome to the Monkey House
description: All are welcome

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/AllVotingIsLocal/AllVotingIsLocal.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```{r, out.width = '100%', fig.height = 8}
tmap_mode("view")
tm_shape(fl.data.map) + 
  tm_polygons("per.latin.america", title = "% Born in Latin America",
                                    palette = "Purples",
                                    alpha = 0.2,
                                    border.col = "grey30",
                                    border.alpha = 0.1,
                                    style = "jenks",
                                    id = "NAME.y",
                                    popup.vars = c("% Born in Latin America" = "per.latin.america",
                                                   "# Born in Latin American" = "latin.america",
                                                   "% Spanish Speakers" = "per.spanish",
                                                   "# Spanish Speakers" = "spanish",
                                                   "# US Citizens" = "total.cit"
                                                   )) +
tm_shape(ven) + 
  tm_polygons("per.venezuela", title = "% Born in Venezuela",
                                    palette = "Oranges",
                                    alpha = 0.2,
                                    border.col = "grey30",
                                    border.alpha = 0.1,
                                    style = "jenks",
                                    id = "NAME.y",
                                    popup.vars = c("% Born in Venezuela" = "per.venezuela",
                                    "% Born in Latin America" = "per.latin.america",
                                                   "# Born in Latin American" = "latin.america",
                                                   "% Spanish Speakers" = "per.spanish",
                                                   "# Spanish Speakers" = "spanish",
                                                   "# US Citizens" = "total.cit"
                                                   ))+
tm_shape(haiti) +   
  tm_polygons("per.haiti", title = "% Born in Haiti",
                                    palette = "Greens",
                                    alpha = 0.2,
                                    border.col = "grey30",
                                    border.alpha = 0.1,
                                    style = "jenks",
                                    id = "NAME.y",
                                    popup.vars = c("% Born in Haiti" = "per.haiti",
                                                   "# Born in Haiti" = "haiti",
                                                   "% Spanish Speakers" = "per.spanish",
                                                   "# Spanish Speakers" = "spanish",
                                                   "# US Citizens" = "total.cit"
                                                   )) +
  tm_shape(counties) + tm_borders()+
  tm_shape(Section203) + tm_polygons("red", alpha = 0.2)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/AllVotingIsLocal/AllVotingIsLocal.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
