# Assignment 3, part 1 1st attampt 
download.file("https://raw.githubusercontent.com/markziemann/SLE712_files/master/bioinfo_asst3_part1_files/gene_expression.tsv",destfile="gene_expression.tsv")
x<-read.table("gene_expression.tsv")
typeof(x)
head(x)
str(x)

x <- read.table("gene_expression.tsv", header = TRUE)
head(x)
str(x)
x <- read.table("gene_expression.tsv", header = TRUE , stringsAsFactors = FALSE )
head(x)
str(x)
x <- read.table("gene_expression.tsv", header = TRUE , stringsAsFactors = FALSE , row.names = 1)
head(x)
str(x)

x <- read.csv("gene_expression.tsv", sep="\t" ,stringsAsFactors = FALSE, row.names = 1 )
head(x)
str(x)

x$A <- colMeans(x)
x
colnames(x)[3]<-"Mean"
head(x)
str(x)
