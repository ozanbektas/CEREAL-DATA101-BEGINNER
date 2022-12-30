# CEREAL-DATA101-BEGINNER
BEGINNER PROJECT ABOUT CEREAL 

# kutuphaneleri alalım

1-import pandas as pd
2-import seaborn as sns
3-import matplotlib.pyplot as plt
4-%matplotlib inline  

# okutuyorum
df = pd.read_csv('C:/Users/ozann/OneDrive/Masaüstü/databank/data101  proje/cereal.csv')

df.head() # dataları görselleştirdim

df.info() # null değer varmı bakıyorum

# her bir gevrek markasının besin değerlerini histogramlara yazdıralım
df.hist(bins=50,figsize=(20,15))
plt.show()

print(df[0:5])

df.isnull().sum() # Data setimizde null değer olup olmadığını görelim.Bu işlem veri temizleme aşaması için önemli.

# null değer olmadığını gördük,cereal markalarından ratinglere bakıp büyük bi outlier olup olmadığına bakalım

Rating = df['rating']
df['rating']

sns.set_palette("summer") #outlierı yakalamak için veriyi görselleştiriyorum.Bu yüzden grafik rengi olarak summerı seçtim.

sns.distplot(Rating).set_title('Distribution of ratings for cereal')
# Outlier veriyi görebilmek için grafiğe döktüğümüz kod buradadır.Herhangi bir null değeri olmadığı için burada bırakıyorum.
