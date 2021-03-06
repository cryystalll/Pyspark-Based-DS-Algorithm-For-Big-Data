# Big Data Analysis Based on Pyspark
```
Massive Data Analysis for 500000+ data using pyspark api
```

## 1. Google Page Rank Algorithm
<div align=center><img src="/pyspark_img/googlepagerank.jpeg" alt="Cover" width="40%"/></div>

## Method
```
iteration 10 times
```
<div align=center><img src="/pyspark_img/pagerankkkk.jpeg" alt="Cover" width="40%"/></div>

## 2. Kmeans Clustering Algorithm 
## Method
```
iteration 10 times
```
```
Initially build clusters
c1:randomly choose centers pair 
c2:choose long-distance pair 
```
<div align=center><img src="/pyspark_img/kmeans_algo.png" alt="Cover" width="40%"/></div>
<div align=center><img src="/pyspark_img/kmeanss.png" alt="Cover" width="40%"/></div>


## Result And Discussion
* i.Euclidean distance
<div align=center><img src="/pyspark_img/Euclidean.png" alt="Cover" width="40%"/></div>

```
以cost來看，c2選擇「互相距離遠」的點為中心點的⽅式比c1隨機選擇中心點的⽅法好。
因為 Euclidean distance是受平方影響，在多維的資料中若有某一維離中心點偏差值特別大，容易造成 distance與cost值特別大，
因此對c1方法來來說，若沒有盡量選互相距離大的點座為中心點，在圖中會很容易易有些點附近都沒有中心點(中心都距離他們很遠)，偏差值會太大而主導距離跟cost值 ; 
c2的⽅法較不會有極端值的出現，因此cost會較小。 
還有如果⼀一開始使用c1⽅法選擇的中⼼點之間距離較近，在分類時容易把離他們較近、本該在同⼀群的點分散到這些距離較近的中⼼點之中。
若一開始就選擇互相距離遠的中⼼點，能確保他們周圍較近的點⼀開始可分進同⼀類，
這影響到了後續分類表現以及percentage improvement，由此可觀察到c2的表現較好。
```
## ii.Manhattan distance
<div align=center><img src="/pyspark_img/manhattan.png" alt="Cover" width="40%"/></div>

```
以cost來看，c1隨機選擇中⼼心點的⽅法比c2選擇「互相距離遠」的點為中心點的⽅式好。
c1⽅法⼀開始的cost就比c2⽅法⼩，因為在多維資料中，Manhattan distance是受各維度影響，
不會有偏差值被特別放大的問題，算出的是各維度差的總和，離中心近的點跟遠的點的影響力是同等的。 
比起c1周圍有可能有許多距離和較小的點，⽤用c2可能會導致中心點太過分散，雖然可能沒有偏差特別大的點，
導致c2⽅方法的distance跟cost比較大。
```
## 3.matrix product
<div align=center><img src="/pyspark_img/matrix-multiplication.png" alt="Cover" width="30%"/></div>

