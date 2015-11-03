#15'1102 Rnote

library("foreign")
setwd("C:/Users/user/Desktop")
gss<-read.spss("GSS.SAV",to.data.frame=T)

#1
table(gss$happy, useNA='ifany')
table(gss$hapmar, useNA="ifany")
prop.table(table(gss$happy))
prop.table(table(gss$hapmar))
#2
tab<-table(gss$happy, gss$hapmar)
tab
prop.table(tab)
sum(tab)
#find st in git for goodmann Kruskal and load it
calc.lambda(tab)
calc.gamma(tab)
#calculate some good lambda and...
#large more correlate?

#2a predict happy and the error
#2b predict happy by marriage
#2c predict marriage happy error
#2d cal lambda by hand and its diff to computer
#2e gamma tell u what
#2f other coeff could be compute?

#3 robust version of correlation? by median?

#4 
library("MASS")
bst<-read.spss("Z:/daten/BOSTONH.SAV", to.data.frame =T)
Boston
names(Boston)

#5a
mean(Boston$medv)
fivenum(Boston$medv)
#5b
miss<-read.csv2("z:/daten/bhdmiss.csv")
#mcar
medv_mcar<-Boston$medv[!miss$mcar] #grib out not MCAR data
mean(medv_mcar) #higher than above
fivenum(medv_mcar)
t.test(medv_mcar)
boxplot(Boston$medv~miss$mcar)
#mar
medv_mar<-Boston$medv[!miss$mar] #grib out not MCAR data
mean(medv_mar) #higher than above even higher
fivenum(medv_mar)
t.test(medv_mar)
boxplot(Boston$medv~miss$mar)
#mar
medv_mnar<-Boston$medv[!miss$mnar] #grib out not MCAR data
mean(medv_mnar) #lower than all above
fivenum(medv_mnar)
t.test(medv_mnar)
boxplot(Boston$medv~miss$mnar)
