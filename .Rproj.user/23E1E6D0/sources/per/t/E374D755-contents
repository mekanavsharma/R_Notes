
"
In following topic (R basic) we rely on 'US murder rates by state' data set
access the dataset by loading the dslabs library and loading the murders dataset using the data
function
"

library(dslabs)
data(murders)
class(murders)
str(murders)
rm(list = ls())
colnames(murders)

# levels do the same as unique function
unique(murders$region)
levels(murders$region)

#Suppose we want the levels of the region by the total number of murders rather than alphabetical order.
# we can use reorder , and use sum.
region <- murders$region
value <- murders$total
region <- reorder(region, value, FUN = sum)
levels(region)

temp <- c(35, 88, 42, 84, 81,30)
city <- c('Beijing', 'Lagos', 'Paris', 'Rio de Janeiro', 'San Juan', 'Toronto')
names(temp) <- city

# Check muder rate for one state ; we can use which
murders$murder_rate <- murders$total / murders$population * 100000
ind <- which(murders$state == "California")
ind
murders$total[ind]


# what if we want to do it for multiple states; use match
ind <- match(c("New York", "Florida", "Texas"), murders$state)
ind
murders$total[ind]


#logical statement to check whether element exist or not
c("Arkansas","Boston", "Dakota", "Washington") %in% murders$state

#Advanced: There is a connection between match and %in% through which. 
match(c("New York", "Florida", "Texas"), murders$state)

# same output but different order
which(murders$state%in%c("New York", "Florida", "Texas"))

murders[murders$murder_rate < 1 & murders$region == 'Northeast',]