# Introduction
This is a task from Google Code-In.
Here you learn how to make interactive data visualization.

# Requirements
- R
- RStudio
- animint2 
- servr
- gistr

# Code Description
```
#Task 5

#Create an interactive data visualization using animint2
library("animint2")
library("servr")
library("gistr")
#Load World Bank Data
data(WorldBank, package="animint2")
tail(WorldBank)
WorldBank1975 <- subset(WorldBank, year==1975)
head(WorldBank1975)
#Make a scatter plot
scatter <- ggplot()+
  geom_point(
    mapping=aes(x=life.expectancy, y=fertility.rate, color=region),
    data=WorldBank1975)
scatter
animint(scatter)
#Create a bl.ocks link
servr::httd("/private/var/folders/0y/h0r16nbn5vbgc154pt0pgbzh0000gn/T/RtmpQln7eg/filea7e63df00e0e")
animint2gist(animint(scatter))
```
# Screen Cast
![Record](http://g.recordit.co/R2A48Zu1vn.gif)

# Authors
- Mridul

# Website
http://bl.ocks.org/krishnakalyan3/raw/7792acba973e5efb7fbe9c373c6422ad/
