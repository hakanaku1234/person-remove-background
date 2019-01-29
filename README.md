![image](https://github.com/03053020ITE/person-remove-background/blob/master/topic.PNG)

### 本專題擬發展一套基於深度學習平台自動人像去背系統，將輸入的一張照片的人像取出，並保有邊緣(如髮絲、頭髮等)成分，並將圖像背景呈現黑色
### 本專題使用了JPPNet、Mask-RCNN、DilatedNet共三種演算法實現了三種不同的人像分割技術，分別利用LIP 、COCO、PASCAL VOC三種數據集訓練，最後利用23張相同圖像進行測試及評估
### 製作一GUI人性化界面，讓使用者可以容易的放入照片去除背景
### 提供了動漫效果，讓使用者可以輕鬆透過此平台製作漫畫

## 人像去背漫畫平台

![image](https://github.com/03053020ITE/person-remove-background/blob/master/5.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/jpp1.PNG)
### 利用人類部位(human parsing)和姿勢(pose)的連貫表示來促進每項任務，提出了一種聯合人體部位和姿勢估計網絡
### 首先我們使用GitHub上開源專案LIP_JPPNet下載預先訓練的模型並保存，接著在大陸中山大學人類網路物理智能集成實驗室下載LIP數據集，並對數據集標籤(label)進行數據增強的左右翻轉，最後訓練了40個epoch並保存最好的模型
## JPP Network
### Parsing And Pose Subnet
部位子網路(Parsing subnet) 在Res-5之後有兩個卷積來生成parsing maps
姿勢子網路(Pose subnet)在Res-4之後添加幾個3×3、1×1卷積層來生成pose maps
### Refinement Network
將前面pose maps和parsing maps重新集成到特徵空間中，方法是將它們映射到更多的通道，然後用四個卷積層(𝟑×𝟑、𝟓×𝟓、𝟕×𝟕、𝟗×𝟗)，來捕獲足夠的局部上下文(local context)並增加field size
##Look Into Person Dataset
共50462張圖片，19081張全身圖片，13672張上身圖片，403張下身圖片，3386張無頭部圖片，2788張後視圖片，21028張遮瑕圖片，並把每張圖片跟分隔為19種人體部位、一種背景


![image](https://github.com/03053020ITE/person-remove-background/blob/master/jpp%2Blip.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/jpp%2Blip2.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/jpp%2Blip3.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/mask1.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/mask%2Bcoco.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/mask%2Bcoco1.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/mask%2Bcoco2.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/dilated1.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/dilated2.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/dilated3.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/dilated4.PNG)
                                                
```
Evaluation
```

![image](https://github.com/03053020ITE/person-remove-background/blob/master/precision.PNG)

![image](https://github.com/03053020ITE/person-remove-background/blob/master/abstract.PNG
)







