#  setwd("C:/Users/?ick/Desktop/Comunity ecology research")
library("csv")
library("ggplot2")
library("car")
#work directory is set and packages loaded

d<- read.csv("dataset.csv", header= TRUE, sep= ";", dec= ".", stringsAsFactors = F) 
# dataset is assigned

d$Absolute_Latitude <- abs(d$Latitude)
#column made for absolute latitude

d[d==0]<- 0
# takes 0 data and tells R not to use this data in the plot

for (i in 23:73) {

  abund_plot <-  ggplot(d, aes(x=d[,"Absolute_Latitude"], y=d[,i])) + 
                  geom_point() 
  pic=file.path("C:", "Users", "?ick", "Desktop", "Comunity ecology research", "Tempo", paste("myplot_", colnames(d)[i], ".jpeg", sep=" "))
  jpeg(file=pic)
   print(abund_plot)
  dev.off()
  
  }
# for loop for crearting and saving plots for absolute abundance of the 
# different species


ssp_columns <- 23:73
count <- 0



for (i in 1:length(all_comb[1,])) { 
  # columns of d to compare: all_comb[,i]
  print(names(d[,all_comb[,i]]))
  for (j in 1:nrow(d)){
    
  }
}


    x <- if (j >0) 
          1 else 0
    y <- if (ssp_columns[ssp_columns != i] > 0) 
          1 else 0
    if (x && y != 0) 
  }
    
    
  
}


g <- 23:72


all_comb <- combn(g, 2)
View(all_comb)
print(i)









