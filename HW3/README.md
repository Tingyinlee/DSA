[Binary Search Tree 流程圖、學習歷程、BST原理](https://github.com/albert0796/DSA/blob/master/HW3/Binary%20Search%20Tree%20%E6%B5%81%E7%A8%8B%E5%9C%96%E3%80%81%E5%AD%B8%E7%BF%92%E6%AD%B7%E7%A8%8B%E3%80%81BST%E5%8E%9F%E7%90%86.pdf)

BST 原理 & 流程圖  
  
A.	結構
1.	為樹狀結構，由一個或多個節點組合而成的有限集合。
2.	樹不可以為空，至少有一個特殊的節點稱為「根節點」(Root)。
3.	根節點之下的節點為 0 ≦ n ≦ 2 個互斥的子集合 T1、T2…Tn，每一個子集合本身也是一棵樹。
4.	每一個節點都會儲存一個值，稱為「鍵值」。
5.	每一個節點的鍵值大於等於左子節點的鍵值；每一個節點的鍵值小於右子節點的鍵值。
 
B.	走訪
1.	中序走訪 (In-order)
走訪順序為: 「左子樹 > 樹根 > 右子樹」
 
2.	前序走訪 (Pre-order)
走訪順序為: 「樹根 > 左子樹 > 右子樹」
 

3.	後序走訪 (Post-order)
走訪順序為: 「左子樹 > 右子樹 > 樹根」
 
C.	新增  
由於BST有每一個節點的鍵值大於等於左子樹和小於右子樹所有鍵值的特性，因此新增的節點也必須符合這樣的特性。另外，因為根節點之下的節點為 0 ≦ n ≦ 2，所以新增的節點僅能新增在子節點尚未達到二的節點之下。以下將一組資料 31, 28, 16, 40, 35, 55 依照順序新增到一顆二元搜尋樹。輸入的資料相同但順序不同會出現不同的搜尋樹。
 
i.	新增31: 先設根節點，31為其鍵值。  
ii.	新增28: 28比根節點小，所以設為左子節點。  
iii.	新增16: 16比根節點小，也比28小，所以設為左子數28的左節點。  
iv.	新增40: 40比根節點大，所以設為右子節點。  
v.	新增35: 35比根節點大，比40小，所以設為右子數40的左節點。  
vi.	新增55: 55比根節點大，也比40大，所以設為右子數40的右節點。  

D.	搜尋  
從樹根開始向下搜尋，當欲搜尋的數值小於根節點時就往根節點左方走訪；大於根節點時就往根節點右方走訪。直到找到欲搜尋的數值為止。如已走訪到最後的葉節點但仍未找到數值，則代表欲搜尋的數值並未在二原搜尋樹中。
 
E.	刪除
1.	欲刪除的節點無任何子節點:
直接將該節點刪除，將其父節點連結該節點的鍊結打斷。
 
2.	欲刪除的節點僅有一個子節點:
將該節點的子節點的數值取代該節點的數值，再將其子節點刪除，如其子節點有子節點，則將其子節點的子節點接在該節點下。
 
3.	欲刪除的節點有兩個子節點:
欲刪除的節點有兩個子節點: 先往欲刪除的節點的右邊子節點走訪一格。如果該節點沒有左節點，直接將該節點取代欲刪除的節點，結束。不然就接著不斷往左邊的子節點走訪直到走訪到的節點無左節點為止，然後將欲刪除的節點的左節點接在該節點的左邊，此時欲刪除的節點僅剩右子節點，最後將欲刪除的節點以其柚子節點取代。
