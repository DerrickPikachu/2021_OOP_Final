---
title: Final Homework
tags: 2021_OOP_Final
---

# Final Homework of course OOP

github connection: https://github.com/DerrickPikachu/2021_OOP_Final

hackmd connection: https://hackmd.io/XVq1FmLfSMqc44O8sj-sMg?both

[TOC]

## 題目說明

在現代生活中，網路上有著大量便利的應用程式。這些應用程式使得我們的生活得到了捷徑，變得更加便利且輕鬆簡單。其中一項廣為使用的應用程式即是購物平台，現代人購物常常不再真的到賣場或者百貨公司，而是上網逛購物平台來購買所需。

==今天需要各位藉由打造一個簡易的購物平台來因應時代的變化，並同時展現你們在OOP這門課上學到的知識和coding skill。==

在這份作業中，你需要交出兩個cpp檔。
第一份作業較為簡單，第二份作業延伸第一份作業。
兩份作業要求的執行效果會有點不同，還請各位注意。

### 作業一

我們的購物平台需要兩個模式跟介面:
1. User Mode
2. Manager Mode

程式一開始會如此詢問:
![](https://i.imgur.com/EpMPUuq.png)


接下來將從Manager Mode開始說明。

#### Manager Mode

Manager Mode的基本畫面:
![](https://i.imgur.com/aP331kN.png)

==在基本畫面中，除了以上三個選擇外，按下0可以退回選擇使用者模式的畫面。==
購物平台剛開始開業的時候，**商店內將不具備任何商品**，必須先透過manager mode來加入新的商品。以下依序說明三個功能的效果:
1. **Add new commodity**
    - 加入一個新的商品進入商店當中
    - ![](https://i.imgur.com/S8e0GNC.png)
    - 按照如上圖一樣的順序輸入商品資訊
    - 輸入完成後跳回基本畫面
    - **當輸入相同的commodity的時候應輸出這行錯誤訊息**
    - ![](https://i.imgur.com/IWAcbIH.png)
2. **Delete the commodity from the commodity list**
    - 從已加入的商品中刪除一個商品
    - ![](https://i.imgur.com/J8QlW2B.png)
    - 如上圖將存在的商品列出(**只列出名稱**)，並請使用者輸入
    - 使用者輸入編號即可刪除商品
    - 刪除完成後跳回manager mode的基本畫面
    - ***如果無商品存在，則輸出如下圖***
    - ![](https://i.imgur.com/WhiOGZk.png)
3. **Show all existing commodity**
    - 輸出所有存在的商品，包含他們的詳細內容
    - ![](https://i.imgur.com/aAz6mzU.png)
    - 輸出完成後跳回基本畫面
    - ***如果無商品存在，則輸出如下圖***
    - ![](https://i.imgur.com/WhiOGZk.png)


#### User Mode

User Mode的基本畫面:
![](https://i.imgur.com/iwXbSFh.png)

==一樣在基本畫面只要按下0就可以跳回使用者模式選擇介面。==
接下來將介紹此三種功能的效果:
1. **Buy the commodity you want**
    - 可以從已存在的商品中挑選一樣你想要的商品***放入購物車中***
    - ![](https://i.imgur.com/jfeJJAx.png)
    - 使用者可以輸入商品編號來購買物品
    - 也可以輸入0來結束購物，跳回基本介面
    - ***輸入一次商品即購買該物品一件***
2. **Check your shipping cart**
    - 輸出目前購物車內所含有的內容，並且詢問使用者是否有需要從購物車刪除的商品
    - ![](https://i.imgur.com/aAuU1VA.png)
    - 如果選擇1則詢問要刪除的商品
    - ![](https://i.imgur.com/3wF9LJD.png)
    - 一樣選擇購物車內的商品編號來刪除，刪除直接將該商品刪除(不論有幾個)
    - 最後再向使用者詢問是否要結帳
    - ![](https://i.imgur.com/aGBOFUD.png)
    - 如果要的話就進行與功能3一模一樣的流程，不要的話就跳回基本介面
    - ***如果購物車是空的，則輸出如下圖***
    - ![](https://i.imgur.com/DAj8t4m.png)
3. **Checkout**
    - 替使用者根據目前購物車內含有的內容結帳
    - ![](https://i.imgur.com/sY5m6wC.png)
    - 按下2的話跳回基本介面
    - 按下1的話幫助結算總金額，並且清空購物車
    - ![](https://i.imgur.com/4On5w0i.png)
    - ***如果購物車是空的，則輸出如下圖***
    - ![](https://i.imgur.com/T4cfEt6.png)

### 作業二

==作業二基本上延伸自作業一，大部分的介面及功能都與作業一相同。==

不同的是，作業二中你必須設計三種商品類型，每種類型的商品會對應不同的屬性。舉例來說，一個叫做電腦的類型，這類商品的基礎屬性，可能就會有CPU的屬性、RAM的屬性...等。
以及你必須在關閉程式之前將資料保存起來，下一次開啟程式時，必須要能夠顯示你上次輸入的商品資訊。

:::info
**不可以再使用這篇README上面舉例的類型**(除非你的聯想力真的這麼薄弱想不到，那勉強讓你用這上面提到的***一種***類型)
:::

接下來將細說作業二中應有的功能。
選擇使用者模式的畫面不變，與作業一相同。較多改變的是Manager Mode。

#### Manager Mode

Manager Mode中的基本介面與作業一相同，但內部的三個功能會有些微不同:
1. **Add new commodity**
    - 在開始輸入前，必須先詢問使用者要新增的商品是哪個類型的
    - ![](https://i.imgur.com/jolb0gT.png)
    - 選擇類型以後，必須輸出該類型需要的商品內容
    - ex:![](https://i.imgur.com/ILCFbTx.png)
    - ex:![](https://i.imgur.com/1gNJRR8.png)
2. **Delete the commodity from the commodity list**
    - 這個區塊一樣必須列出所有商品的名稱，但列出時需要按照類型分類，如下圖
    - ![](https://i.imgur.com/clFDgva.png)
3. **Show all existing commodity**
    - 展示目前有的所有商品，一樣必須按照類型分類，如下圖
    - ![](https://i.imgur.com/HczJAmQ.png)

此外，在manager完成商品登陸以後，在關閉程式之前，必須要先將目前所有的商品資料保存起來。而下次打開程式時，必須能夠將資料通通讀進程式裡，並且不必等manager輸入就保有那些資料。

#### User Mode

User Mode的基本介面與作業一相同，功能2與3基本上與作業一相同，不過在展示購物車內容時，必須根據該商品的類型輸出所有的屬性。==(輸出順序可以任意，不必一定要同類型放一起)==
而功能1的部分，必須按照商品類型，同類型的放在一起輸出才行。

1. **Buy the commodity you want**
    - ![](https://i.imgur.com/6CTnwiG.png)
3. **Check your shipping cart**
    - ![](https://i.imgur.com/Vwt7sLa.png)
5. **Checkout**
    - ![](https://i.imgur.com/wuv0jLH.png)

## 作答說明

由於作業一與作業二的題目要求稍微有些不同，所以會分開解釋詳細內容。

### 作業一

在作業一中，***你只需要完成兩個class***:
- CommodityList
- ShoppingCart

將這個兩class裡所有的method都按照method該有的效果定義完成，那麼程式就會順利運作。你們必須定義的method已經寫在上面了。

==這裡你只需要思考如何達成這兩個class的效果，你應該怎麼儲存資料，請盡可能地想出有效率的儲存方法。你可以使用任何你會的資料儲存方法。==

### 作業二

在作業二中，你除了要完成作業一裡面的那兩個class以外，==你還需要自己設計三種商品類型==，並且完成這三種商品類型。此外，在CommodityList與ShoppingCart裡面method的要求都與作業一有一些不同，因此你可能會需要修改你的資料儲存方法。

第二份作業比較需要注意的是將CommodityList資料存入file裡面的部分。由於商品是需要分類的，根據你設計CommodityList的資料儲存方法，存入file的方式會有所不同。

:::info
**Hint**: ShoppingCart不需要將資料存到file裡，只要處理CommodityList的file I/O即可。
:::

## 配分

作業一: 40%

作業二: 60%

:::info
不會改得太嚴格，能寫盡量寫，請注意一定要可以執行
:::

## Store Mechanism

在class Store中，決定當下要顯示給使用者看的介面。Store透過控制其attribute storeStatus來決定要顯示的介面。

storeStatus是一個enumerator，宣告如下:
```c++
enum SMode {OPENING, DECIDING, SHOPPING, CART_CHECKING, CHECK_OUT, MANAGING, CLOSE} storeStatus;
```

屬於User Mode的status有:
1. DECIDING
2. SHOPPING
3. CART_CHECKING
4. CHECK_OUT

屬於Manager Mode的status有:
1. MANAGING

決定使用者模式的status為:
- OPENING

結束應用程式的status為:
- CLOSE

:::info
一旦進入CLOSE的status應用程式就會結束
:::

在Store中，有一個method叫做userInterface><，這個method會根據目前Store的狀態來選定要執行的其他method><:
```c++
void userInterface() {
    if (storeStatus == SMode::OPENING) {
        askMode();
    } else if (storeStatus == SMode::DECIDING) {
        decideService();
    } else if (storeStatus == SMode::SHOPPING) {
        chooseCommodity();
    } else if (storeStatus == SMode::CART_CHECKING) {
        showCart();
    } else if (storeStatus == SMode::CHECK_OUT) {
        checkOut();
    } else if (storeStatus == SMode::MANAGING) {
        managerInterface();
    } else if (storeStatus == SMode::CLOSE) {
        return;
    }
}
```

### SMode::OPENING -> askMode()

這個method會詢問使用者要進行的操作模式，如下:
![](https://i.imgur.com/EpMPUuq.png)

在使用者選定模式以後會接換storeStatus的狀態


| user choice | storeStatus |
| ----------- | ----------- |
| choose 1    | DECIDING    |
| choose 2    | MANAGING    |


### SMode::DECIDING -> decideService()

這個階段為user mode，會詢問使用者想要的服務
![](https://i.imgur.com/h9UOYla.png)


| user choice |  storeStatus  |
| ----------- | ------------- |
| choose 1    | SHOPPING      |
| choose 2    | CART_CHECKING |
| chooce 3    | CHECK_OUT     |
| choose 0    | OPENING       |

### SMode::CART_CHECKING -> showCart()

此為user mode的功能2，展示購物車的內容，效果如題目所述。唯有最後詢問是否要結帳時，才會根據user的選擇去切換storeStatus的狀態

| user choice | storeStatus |
| ----------- | ----------- |
| choose 1    | CHECK_OUT   |
| choose 2    | DECIDING    |

### SMode::CHECK_OUT -> checkOut()

此為user mode的功能3，替user結帳，不論是否決定結帳，最後storeStatus的狀態都會改回DECIDING。

### SMode::MANAGING -> managerInterface()
    
這個method會輸出manager的基本介面
![](https://i.imgur.com/aP331kN.png)

選擇的選項會執行對應的method。
commodityInput -> 新增一個commodity
deleteCommodity -> 刪除一個commodity
showCommodity -> 列出所有commodity
除了選擇0會將storeStatus修改回OPENING。

## Project Doc

這個區塊將介紹一些你們需要完成的以及可能會使用到的class以及method。請一定要了解了定義再去使用，否則建議自己寫一個類似的功能。

### Class InputHandler

這個class主要是包含一些utility function。因此實際上是不會真的宣告一個instance出來的，而是直接透過InputHandler::method()這樣的方式來使用。class裡面包含的全都是static method。

#### ==readWholeLine==

Parameter: None, or fstream
Return: string

讀取user的一行輸入。這個method主要是要解決getline會讀到input buffer裡面會殘留'\n'的問題，會先藉由cin.get()來將這個'\n'讀走，之後再進行getline()，如果有這種需求的輸入可以使用者個function。
此外，此function有一個overloading的版本，可以傳入一個fstream object，針對這個data stream來處理讀取一整行的問題。

:::info
**Hint**: 殘留'\n'的問題在file I/O裡面也非常麻煩且難以處理，一個簡單的方法是每一次都使用getline每一次都讀一整行，這是一個解決辦法，不過需要額外再去轉換讀進來的資料的型態。
:::

#### ==isNum==

Parameter: string
Return: boolean

判斷輸入進來的string是不是一串連續的數字，如:"12345678"，是的話return true，否則為false。

#### ==isValidNum==

Parameter: string
Return: boolean

valid number在這份作業中我給他的意義是(是數字 && 數字>0)。只要符合valid number的定義這個method就會return true。

#### ==numberInput==

Parameter: none
Return: int

這個method讓user輸入一個數字進來，如果輸入的不是數字，則會讓使用者再輸入一遍。如果是數字，則將這個輸入從string轉成integer再return。

#### ==getInput==

Parameter: int, bool(option)
Return: int

讀取user的輸入，只接受[0, maxChoiceLen]的數字，只要不是數字或者超出範圍，就會要求user重新輸入。其中parameter noZero如果是true的話就會讓範圍改成[1, maxChoiceLen]。

### Class Commodity

#### ==Attribute==

- price(protected)
    - 商品價格
- description(protected)
    - 商品描述
- commodityName(protected)
    - 商品名稱

#### ==Constructor==

有兩種overloading的介面，一種為沒有任何parameter的版本，一種為有三個parameter分別對應三個attribute的版本。

#### ==detail==

Parameter: none, or int
Return: none

這個method主要負責將Commodity的詳細內容輸出，有一個overloading的版本加入了一個parameter amount，這個是當購買了數個這個commodity object時，要輸出數量時使用。
輸出範例如下:
![](https://i.imgur.com/Xs3c6Hb.png)

#### ==userSpecifiedCommodity==

Parameter: none
Return: none

這個method主要是用來initialize Commodity object。會在Store裡面被呼叫，主要是用在讓user來完整輸入Commodity需要的資訊，而不會在Contructor的時候對object initialize。

:::info
這個method在作業一不會用到
:::

#### ==save==

Parameter: fstream
Return: none

根據傳入的fstream data flow來將Commodity的資訊傳入這個stream中。用在file I/O要將Commodity存進file裡時。

#### ==load==

Parameter: fstream
Return: none

根據傳入的fstream data flow來讀取Commodity的資訊，並對這個object進行initialize。用在讀取file時。

:::info
**Hint**: 這兩個method根據你的作答方式有可能會用不到，不過我覺得如果沒用到有可能程式會寫得很亂。此外，它們在Commodity裡面都是空的，尚未被定義。因為這兩個method需要被override。
:::

#### ==getName==

Parameter: none
Return: string

commodityName的getter function

#### ==getPrice==

Parameter: none
Return: string

price的getter function

### Class CommodityList

:::info
**Hint**: 這個Class必須要由你來完成它。包含Attribute在內，都必須由你來定義，有一些method是你一定要完成的(否則程式跑不起來)。你可以使用任何你所學過的data structure。
:::

這個class用來管理Store擁有的商品。當manager新加入一個Commodity到Store中時，就是必須將commodity object加入到這個class裡面。換句話說，manager mode裡所有的操作，其實都是在對這個class的object操作。

CommodityList的object本身就是Store的attribute，因此它的method會在Store裡面被呼叫，一定要去完成它的定義。

#### ==showCommoditiesDetail==

Parameter: none
Return: none

這個method負責將當前所有可以被購買的商品輸出到螢幕上。這個method影響到的範圍廣泛，不論user mode或者manager mode都會使用到。最簡單的例子就是manager mode的功能3，範例輸出如下:
1. 作業一
![](https://i.imgur.com/aAz6mzU.png)
2. 作業二
![](https://i.imgur.com/HczJAmQ.png)

#### ==showCommoditiesName==

Parameter: none
Return: none

這個method只輸出商品的名稱到螢幕中。範例輸出:
1. 作業一:
![](https://i.imgur.com/J8QlW2B.png)
2. 作業二:
![](https://i.imgur.com/clFDgva.png)

它將在manager的功能2中被呼叫。

#### ==empty==

Parameter: none
Return: boolean

如果CommodityList是空的，就會回傳true，否則回傳false

#### ==size==

Parameter: none
Return: int

回傳CommodityList中含有的Commodity數量

#### ==get==

Parameter: int
Return: Commodity*

藉由傳入的int來找出要回傳的Commodity。這個int是輸出在畫面中的Commodity編號 - 1。
ex:
![](https://i.imgur.com/J8QlW2B.png)
上圖中，pikachu doll的編號就是2 - 1 = 1。

:::info
**Hint**: 會傳入編號 - 1的原因是CommodityList裡的商品編號是zero-based
:::

#### ==add==

Parameter: Commodity*, string
Return: none

將傳入的Commodity根據傳入的string指定的Commodity類型存到CommodityList中。

#### ==isExist==

Parameter: Commodity*
Return: boolean

判斷傳入的Commodity是不是已經存在於CommodityList中，判斷的依據是根據有沒有同名的Commodity。

#### ==remove==

Parameter: int
Return: none

將指定編號的Commodity刪掉。這裡的編號一樣是zero-based

#### ==save==

Parameter: none
Return: none

將整個CommodityList的資料存到file中。

:::info
這個class根據作答的方法有可能不會被implement，不過當然將存檔的程式寫在這裡會是比較好的。
:::

### class ShoppingCart

:::info
**Hint**: 這個Class必須要由你來完成它。包含Attribute在內，都必須由你來定義，有一些method是你一定要完成的(否則程式跑不起來)。你可以使用任何你所學過的data structure。
:::

這個class主要在儲存購物車內的Commodity。與CommodityList不同的地方是，它不一定每個Commodity只存一個，有可能會有復數個相同的Commodity。必須記錄相同Commodity的數量有幾個。

同CommodityList，ShoppingCart的object同樣也是Store的attribute。因此有一些重要的method一定要被implement。

#### ==push==

Parameter: Commodity*
Return: none

將傳入的Commodity放入購物車中。

:::info
**Hint**: ShoppingCart可以不必根據Commodity的類型分類。
:::

#### ==showCart==

Parameter: none
Return: none

將整個購物車內的Commodity都輸出至螢幕中，範例輸出如下:
1. 作業一:
![](https://i.imgur.com/aAuU1VA.png)
2. 作業二:
![](https://i.imgur.com/Vwt7sLa.png)

#### ==size==

Parameter: none
Return: int

根據ShoppingCart內含有的Commodity數量回傳。
:::info
同一個Commodity視為同一個entry。舉例來說，有一個叫做phone的商品以及ball的商品，如果購物車內phone有4個，ball有2個。則回傳的size為兩個商品的2。
:::

#### ==remove==

Parameter: int
Return: none

根據傳入的int找出要刪除的Commodity，不論這個Commodity在購物車內有幾個都直接刪掉。
:::info
**Hint**: 這裡傳入的指定編號一樣是zero_based，一樣是根據showCart輸出的編號 - 1來刪除Commodity
:::

#### ==checkOut==

Parameter: none
Return: int

計算整個購物車內含有的Commodity的總金額並回傳，同時將ShoppingCart內含的Commodity清空。

#### ==empty==

Parameter: none
Return: boolean

判斷購物車內不有沒有任何商品，沒有的話回傳true，否則為false。
