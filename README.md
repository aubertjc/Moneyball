# Moneyball
Least Square
http://rpubs.com/jaubert148/132502
1.- https://rstudio-pubs-static.s3.amazonaws.com/23247_8af1a386e4184c95bb36ba7a6ea0f699.html

2.- Data.Scientist.QUI dans Complément

load(url('http://s3.amazonaws.com/assets.datacamp.com/course/dasi/mlb11.RData'))
plot(mlb11$runs ~ mlb11$at_bats)
correlation = cor(mlb11$runs, mlb11$at_bats)
correlation
x1 = 5400
y1 = 750

x2 = 5700
y2 = 650

plot_ss(x = mlb11$at_bats, y = mlb11$runs, x1, y1, x2, y2, showSquares = TRUE)
plot_ss(x = mlb11$at_bats, y = mlb11$runs, showSquares = TRUE, leastSquares=T)

ggplot(mlb11,aes(x=mlb11$at_bats,y=mlb11$runs))+geom_point()+geom_smooth(method="lm")+labs(x="mlb11$at_bats", y="mlb11$runs") + theme(panel.background = element_rect(fill = "blue"))
