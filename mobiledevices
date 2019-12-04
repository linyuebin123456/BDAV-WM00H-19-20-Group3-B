# tell R where your file is located
setwd('C:/Users/metl006/Desktop/SImOut/SImOut')

# tell R what file to use
mydata <- read.csv("mobile_devices.csv")

# convert to a R data frame
mydata <- data.frame(mydata)

# fit the K-means model to mydata
fit <- kmeans(mydata, 6) #6 cluster solution

# get cluster means
means <- aggregate(mydata, by=list(fit$cluster), FUN=mean)

# append cluster assignment
mydata <- data.frame(mydata, fit$cluster)

# write the data back out to Excel
write.csv(mydata, file="Cluster6_1.csv", row.names=FALSE) # full data file with cluster assignments
write.csv(means, file="ClusterMeans6_1.csv", row.names=FALSE) # list of means by cluster

#end

