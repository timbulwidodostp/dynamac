# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Dynamic simulation and testing for single-equation ARDL models Use dynamac (dynardl) With (In) R Software
install.packages("readxl")
install.packages("httr")
install.packages("dynamac")
library("httr")
library("readxl")
library("dynamac")
# Import Data Excel Into R From Github Olah Data Semarang (timbulwidodostp)
github_link <- "https://github.com/timbulwidodostp/dynamac/raw/main/dynamac/dynamac.xlsx"
temp_file <- tempfile(fileext = ".xlsx")
req <- GET(github_link, 
# authenticate using GITHUB_PAT
authenticate(Sys.getenv("GITHUB_PAT"), ""),
# write result to disk
write_disk(path = temp_file))
dynamac <- readxl::read_excel(temp_file)
# Estimate Dynamic simulation and testing for single-equation ARDL models Use dynamac (dynardl) With (In) R Software
dynamac<-dynardl(concern~incshare10+urate,data=dynamac,lags=list("concern"=1,"incshare10"=1),diffs=c("incshare10","urate"),ec=TRUE,simulate=FALSE)
summary(dynamac)
dynamac_2<-dynardl(concern~incshare10+ urate,data=dynamac,lags=list("concern"= 1,"incshare10"=1),diffs=c("incshare10","urate"),lagdiffs=list("concern"=1),
ec=TRUE,simulate=FALSE)
summary(dynamac_2)
# Dynamic simulation and testing for single-equation ARDL models Use dynamac (dynardl) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished