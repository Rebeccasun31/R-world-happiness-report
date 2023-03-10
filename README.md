# 2022-1 R Programming Final Project

使用R語言分析世界幸福報告中的指數

組員：孫承瑞、曾家祐、戚維凌、葉家蓁

# Data Introduction

世界幸福報告是聯合國於網路每年出版的國際調查報告，從2012年開始發行，迄今已持續10年，資料來源是蓋洛普世界民意調查，目的在於衡量國家公共政策對人民幸福的影響。

用以衡量的六項指標分別是GDP、平均自然壽命、社會援助、社會自由程度、人民慷慨程度、政府腐敗程度，此外我們也利用「反烏托邦殘差」這個量值一起分析。

![R_final_15](https://user-images.githubusercontent.com/86657062/224357751-8647a6b5-701d-493d-91bd-2de7424d03de.jpg)

以下簡單介紹這次所使用的dataset，裡面包括了國家幸福指數以及各項指標，

我們以此資料為根據，進一步使用不同分類方式畫出各種圖表進行分析：

![R_final_15 (1)](https://user-images.githubusercontent.com/86657062/224357801-faa3d39d-78a9-45ab-ba20-79a049627252.jpg)

將2022年的dataset summary之後可以得到國家總數與各項指標的最高、最低和平均分數等數據：

![R_final_15 (2)](https://user-images.githubusercontent.com/86657062/224357921-4e6949f4-ae6f-43c5-aaa3-13440c5a02f1.jpg)

# Data Analysis

首先我們分析2022年的世界幸福指數，將世界地圖的dataset和幸福指數merge在一起，並以國家為區域依照幸福指數的高低進行上色，

可以發現北美及北歐國家比起其他國家有明顯的差異，顯示住在該地區的人民平均擁有較高的幸福感：

![R_final_15 (3)](https://user-images.githubusercontent.com/86657062/224358602-d27dfb9c-5a0d-47c2-aa96-3a9ea420a596.jpg)

接著是2022年幸福指數前30名的國家，可以看到前八名的國家都位在歐洲，

且從色塊中發現除了反烏托邦殘差之外主要影響幸福指數的指標是GDP：

![R_final_15 (4)](https://user-images.githubusercontent.com/86657062/224359134-5588aa63-8406-4b93-ae10-3c9e6ff8244a.jpg)

根據全球的高分、中等、低分群來分析，此圖以各挑選兩個國家為例，

發現較高分的國家多位於北歐，分數中等的位於西歐、中歐，而較低分的國家則多位於東歐和南美洲：

![R_final_15 (5)](https://user-images.githubusercontent.com/86657062/224359253-6b58551a-b696-4a6e-9ef2-cefdffb1cfe5.jpg)

以下折線圖是從2015到2022年的全球平均幸福指數走勢圖，特別的是，我們把疫情爆發的2019年標示出來，

發現在2019年後幸福指數依然大幅增加，並沒有因為疫情的原因導致幸福指數下降：

![R_final_15 (6)](https://user-images.githubusercontent.com/86657062/224359818-a49146b9-1f22-4831-a2f4-b25959b9b33c.jpg)

下圖為六種指標及反烏托邦殘差在2015至2022年間的走勢，由圖中可以發現2019年之後：

- Corruption由下降轉為上升
- GDP上升趨勢顯著提升
- Social Support下降
- Life下降
- Freedom上升
- Generosity整體持續下降

![R_final_15 (7)](https://user-images.githubusercontent.com/86657062/224360585-1b84a9f0-8329-4857-b013-0a0b87f52aef.jpg)

我們將2022年的六項指標和總分的關係畫成散點圖，並畫出擬合資料的平滑曲線，可以看出各項指標和總分的相關程度：

![R_final_15 (8)](https://user-images.githubusercontent.com/86657062/224360689-bd119696-2f84-452f-9c2a-70b9cbdbeee8.jpg)

利用散點圖來表示2015~2022年各國每項指標跟幸福指數關係的離散程度，一樣畫出平滑曲線來表現近七年來資料的相關程度：

![R_final_15 (9)](https://user-images.githubusercontent.com/86657062/224361007-b6f4b084-319c-48b0-936c-975eeb4c3cd8.jpg)

# Conclusion

- 紐澳、歐洲、北美普遍幸福指數較高
- 幸福指數前八高的國家都在歐洲
- GDP、Life、Freedom、Social Support和幸福指數呈正相關
- Generosity、Corruption和幸福指數較沒有直接關係
- 2019年COVID-19爆發之後，幸福指數不減反增

# Reference

- https://worldhappiness.report/
- https://observablehq.com/@superbooming/untitled
- https://ithelp.ithome.com.tw/articles/10276943?sc=rss.iron
- https://www.heywhale.com/mw/dataset/5caaef138408c1002b4b4e92
- https://www.kaggle.com/datasets/buszter/happiness
- https://www.kaggle.com/datasets/mathurinache/world-happiness-report
