getwd()

#ilk fonksiyonlar

 print("I'm code")
#÷÷÷÷÷÷÷÷÷
 2+2
#÷÷÷÷÷÷÷÷
 2*4
#÷÷÷÷÷÷÷÷
2^3
#÷÷÷÷÷÷÷÷
2+(2*3)^2
#÷÷÷÷÷÷÷÷÷
(1+3)/2+45
#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
x=2  #same as: x<-2
x
#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
x*4
#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
x+2
#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
 class(x)
#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
y="hello world!"
print(y)

class(y)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷

name="Jhon Muschelli"
name
#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
x<- c(1,4,6,8)
x

class(x)

length(x)

y


length(y)

x+2

x*3

x+c(1,2,3,4)

str(x)

str(y)
#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
küp <- function(x) {
  return(x^3)
}
print(küp(5))

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷

veri=read.csv("http://johnmuschelli.com/intro_to_r/data/Youth_Tobacco_Survey_YTS_Data.csv")

View(veri)
head(veri)

View(mtcars)
dim(veri)   
nrow(veri)    #satır sayısı
ncol(veri)    #sütun sayısı
help(dim)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#değişkenin ismini değiştirmek için kullanılan fonksiyon

install.packages("dplyr")
library(dplyr)
veri_yeniden_ad = rename(veri, year=YEAR)

names(veri_yeniden_ad)
names(veri)
#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#write ile değişkenin ismini değiştirme
install.packages("readr")
library(readr)

veri_yeniden_ad2=rename(veri_yeniden_ad, Year=year)
write_csv(veri_yeniden_ad, path="C:/Users/yeni/Downloads/......tutun.csv")
getwd()


ls()   #listeleme fonksiyonu

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#ilgili paketten ilgili fonksiyonu indirme
install.packages("tidyverse")
library(tidyverse)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#yeni bir veri tanımlamak için
#32 satır 11 sütundan oluşan mtcars verisi tuttuk
veri2=data(mtcars)
View(df)
veri2=data.frame(mtcars)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#boyutuna bakıp kontrol etmek için
dim(mtcars)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#mtcars başlıklarını görmek için
head(mtcars)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#markaları tablo şeklinde görme için
View(veri2)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#veri karakterlerini görmek için
veri2_tibble= as_tibble(veri2)

head(veri2_tibble) #6 başlığı verdi

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#dplyr dan fonksiyon kullanma, yeniden adlandırdık
veri2_yeniden_ad=dplyr::rename(veri2_tibble, MPG=mpg)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#hepsini büyük harf yapmak için;
veri2_yeniden_ad2= dplyr::rename_all(veri2_yeniden_ad, toupper)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#veri2 deki değişkenlerin isimlerini vermesi için
names(veri2)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#veri değişkenlerini filtrelemek için $ işaretini kullanırız
veri2_gear = veri2$gear

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#veri2 den mpg filtrelesin select, pull kullanarak
veri2_mpg = select(veri2, mpg)

veri2_mpg = pull(select(veri2, mpg))

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#filter kullanarak "veya |" bağlama
filter(veri2, mpg > 19 | mpg < 17)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#bu filtreyi isimle çağırmak için
veri_mpg_aralık = filter(veri2, mpg > 19 | mpg < 17)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#% işareti ile içerisinden seç filtre çalıştır, 
#iki koşulu aynı anda sağlayan & yani or
#cyl 4 olsun ve mpg ler de 22 den büyük olsun koşulu için
#en son bunların içinden select ile disp ve qsec leri bas yani 2 koşul sağladık
veri2_piped= veri2 %>% filter(mpg >22 & cyl==4) %>% select(disp, qsec)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#yeni sütun oluşturmak için
veri2$yenisütun =veri2$wt*3
veri2_12
View=(veri2)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#tekrar veriyi geri çağırmak için
veri2=mtcars
View(veri2)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#ayrı 12. sütun eklemek için
veri2_12$yenisütun =veri2$wt3

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#newcol tanımlama   
veri2_mut = mutate(veri2, newcol=wt*3)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#disp değişkeninin yeni sütunda kategorize edilmişini oluşturmak için
veri2_mut2 = mutate(veri2, disp_kateg = ifelse(
                           disp <=200,
                           "düşük",
                           ifelse(disp <=400,
                                  "orta",
                                  "yüksek")
                           ))
View(veri2_mut2)

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#disp i azalan sırasına göre sıralamak için
arrange(veri2, desc(disp))

#÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷÷
#veri2 de yeni değişken oluşturmak için yeni data.frame oluşturma
transmute(veri2, newcol=disp*5, mpg, gear)


