# Video-Games-Sales
title: "Video Games Sales"
author: "Shreya Sajeev"
date: "4/15/2022"
```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```


```{r libraries}
suppressPackageStartupMessages(library(tidyverse))
```
```{r input}
vgsales <- readxl::excel_format ("D:/My Desktop/vgsales.xlsx")
```


--Across the several years, what was the total global sales made in the gaming industry?
```{r error=FALSE}
library(ggplot2)
ggplot(data = vgsales, aes(x = Year, y = Global_Sales,)) +
  geom_line() +
  labs(x = "Year",
    y = "Global_Sales",
title = "Trend of Sales made by Nintendo")
```
![R 1](https://user-images.githubusercontent.com/100975522/163599231-bc9628f7-4f68-40c4-958a-24a5e06e047d.jpeg)


--Which game made the most amount of global sales?
```{r}
vgsales <- readxl::excel_format ("D:/My Desktop/vgsales.xlsx")
val <- max(na.rm = FALSE)
cat("The most purchased game:", max(vgsales))
```
The maximum value of the vector is: 82.74
This value corresponds with the global sales made by Wii Sports.


--Which platform earned the most amount of sales in the North American Region?
```{r}
library(ggplot2)
ggplot(data = vgsales, aes(x = Platform, y = NA_Sales,)) +
  geom_line() +
    labs(x = "Platform",
    y = "NA_Sales",
title = "Trend of Sales in North American region")
```
![R2](https://user-images.githubusercontent.com/100975522/163601820-8cc7dd25-258b-4725-b6dd-4feaef7dc2b8.jpeg)
The graph shows that Wii has been the platform that has made most sales in the North American region.



--Which game genre was the most popular in the European region?
```{r}
library(ggplot2)
ggplot(data = vgsales, aes(x = Genre, y = EU_Sales,)) +
  geom_line() +
    labs(x = "Genre",
    y = "EU_Sales",
title = "Popular Game Genres in European region")
```
![R3](https://user-images.githubusercontent.com/100975522/163602601-60d959da-ab66-4a17-932e-bc33a13a3d1a.png)
From the graph we can see that the genre of 'sports' gained the most traction amongst gamers in the European region.
