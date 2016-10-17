Importing.Multiple.CSV.Files.intoR
================
Lucia Liu
October 16, 2016

``` r
path <- "C:/Users/Luxia Liu/"
files <- list.files(path=path, pattern="*.csv")

for(file in files)
{
  pos <- which(strsplit(file, "")[[1]]==".")
  assign(
    gsub(" ","",substr(file, 1, pos-1)), 
    read.csv(paste(path,file,sep="")))

}
```
