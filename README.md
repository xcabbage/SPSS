# SPSS

plusz node-ok:

C:\ProgramData\IBM\SPSS\Modeler\17.0\CDB
konyvtarat letrehozni


-- R node ----------------------------------
# csak egyszer kell install package
#install.packages("Imap")
library(Imap)

distance<-gdist(modelerData$Longitude1,modelerData$Latitude1, modelerData$Longitude2,modelerData$Latitude2, units = "km", verbose = FALSE)

# ez mindig kell az R mezomanipulalo nod kod vegere
modelerData<-data.frame(modelerData,distance)
var1<-c(fieldName="Distance",fieldLabel="",fieldStorage="real",fieldMeasure="",fieldFormat="",fieldRole="")
modelerDataModel<-data.frame(modelerDataModel,var1)
