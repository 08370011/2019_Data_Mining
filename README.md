# My learning note

Data Mining

- Fri 12:00-15:00


## HW0 Tidy Data

- [HW0 Tidy data](https://github.com/smile22091/2019_Data_Mining/blob/master/HW0_Tidy_Data/notebooks/HW0_Tidy_Data.ipynb)



## HW1 Decision Tree

- [HW1 Decision Tree](https://github.com/smile22091/2019_Data_Mining/blob/master/HW1_Decision_Tree/notebook/Adult.ipynb)

- [HW1 Decision Tree Nbviewer](https://nbviewer.jupyter.org/github/smile22091/2019_Data_Mining/blob/master/HW1_Decision_Tree/notebook/Adult.ipynb)


## HW2 Apriori

- [HW2 Apriori](https://github.com/smile22091/2019_Data_Mining/blob/master/HW2_Apriori_Algorithm/notebook/Apriori.ipynb)

- [HW2 Apriori Nbviewer](https://nbviewer.jupyter.org/github/smile22091/2019_Data_Mining/blob/master/HW2_Apriori_Algorithm/notebook/Apriori.ipynb)

### Note

#### 關聯規則
在資料探勘的演講或是課程上，講者一定會提到「啤酒尿布」這樣的案例。估且不論這是不是江湖謠傳，這的確是一個經典的資料探勘算法 - **關聯規則**（Association rule）。因為常用在商品資料上，所以也被稱為**購物籃分析**（Basket data analysis）。

關聯分析是一種在大規模資料集中尋找相互關係的任務，透過資料間的關係，**目標去找出怎樣的組合是比較常出現的**。與傳統統計的相關性差異在於關聯法則更重視的是關聯性。這些關係可以有兩種形式:

1. 頻繁項集（frequent item sets）: 經常出現在一塊的物品的集合。
2. 關聯規則（associational rules）: 暗示兩種物品之間可能存在很強的關係。


#### Apriori Algorithm 量化標準
1. Support (支持度) : 意思是某特定種類在所有種類的比重
	- 例如我有100名會員，其中有20名購買過雨具，則support(雨具) = 20% 。

2. Confidence (信賴度) : 意思是某A種類中，含有某B種類的比重
	- 例如我有100名會員，其中40人買過涼鞋，而這40買過涼鞋者當中，又另有10人買過雨具，則confidence(涼鞋->雨具) = 10/40 = 25% 。

3. Lift (提升度) : 意思為某兩者關係的比值，如果小於1代表兩者是負相關，等於1表示兩者獨立，大於1表示兩者正相關
	- 公式為confidence(A->B) / support(B) ，帶入上述例子可表示成 lift(涼鞋->雨具) = 25/20 = 1.25 。

#### Apriori 演算法優缺點
- 優點：易編碼實現
- 缺點：在大資料集上可能較慢
- 適用資料型別：數值型 或者 標稱型資料。

#### Apriori 演算法流程步驟：
1. 收集資料：使用任意方法。
2. 準備資料：任何資料型別都可以，因為我們只儲存集合。
3. 分析資料：使用任意方法。
4. 訓練資料：使用Apiori演算法來找到頻繁項集。
5. 測試演算法：不需要測試過程。
6. 使用演算法：用於發現頻繁項集以及物品之間的關聯規則。

#### 應用場景
Apriori 演算法廣泛應用於各種領域，通過對資料的關聯性進行了分析和挖掘，挖掘出的這些資訊在決策制定過程中具有重要的參考價值。

1. 應用於消費市場價格分析中

2. 應用於網路安全領域，比如網路入侵檢測技術中

3. 應用於行動通訊領域


#### Reference
- [資料探勘演算法 - 關聯規則](https://ithelp.ithome.com.tw/articles/10187244)

- [一步步教你輕鬆學關聯規則Apriori演算法](https://www.itread01.com/content/1544958735.html)

- [【10】當老闆問說：嗯...你只不過是改變資料結構而已，說好的分析呢？](https://ithelp.ithome.com.tw/articles/10194134)