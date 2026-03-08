# 資料結構 · 課堂 5　Linked List 鏈結串列　測驗


## 一、選擇題　（每題 5 分，共 25 分）

**1.** Linked List 的每個節點包含哪兩個部分？

&emsp;（　　）　A. 鍵值（key）與雜湊碼（hash）

&emsp;（　　）　B. 資料（data）與指向下一個節點的指標（next）

&emsp;（　　）　C. 索引（index）與資料（data）

&emsp;（　　）　D. 前後兩個指標（prev 與 next）

---

**2.** 對 Singly Linked List 的**頭部**插入一個新節點，時間複雜度是？

&emsp;（　　）　A. O(n)　　B. O(log n)　　C. O(n²)　　D. O(1)

---

**3.** 下列哪個操作，Linked List 比 Array **更有效率**？

&emsp;（　　）　A. 用索引隨機存取 arr[i]

&emsp;（　　）　B. 在**已知位置**的節點後插入新節點

&emsp;（　　）　C. 搜尋某個特定值

&emsp;（　　）　D. 利用 CPU Cache 加速存取

---

**4.** Doubly Linked List 相較於 Singly Linked List 的主要優勢是？

&emsp;（　　）　A. 佔用更少記憶體

&emsp;（　　）　B. 可以雙向遍歷，且尾部刪除達到 O(1)

&emsp;（　　）　C. 搜尋速度更快

&emsp;（　　）　D. 不需要使用指標

---

**5.** 何時**最適合**選擇 Linked List 而非 Array？

&emsp;（　　）　A. 需要頻繁用索引讀取資料

&emsp;（　　）　B. 需要盡量減少記憶體使用

&emsp;（　　）　C. 資料大小無法預測，且頻繁在頭部或中間插入/刪除

&emsp;（　　）　D. 需要 Cache-Friendly 的存取模式

---

## 二、繪圖題　（共 24 分）

**6.（12 分）** 請畫出以下程式碼建立的 Singly Linked List 結構圖，標示 `head` 指向、各節點的 `data` 值、`next` 方向，以及最後的 `NULL`。

```cpp
Node* n1 = new Node(); n1->data = 10;
Node* n2 = new Node(); n2->data = 30;
Node* n3 = new Node(); n3->data = 20;
n1->next = n2;
n2->next = n3;
n3->next = nullptr;
Node* head = n1;
```

&emsp;（在下方空白處作圖）

&emsp;

&emsp;

&emsp;

&emsp;

&emsp;

---

**7.（12 分）** 在下圖 Linked List 中，在節點 `20` 後面插入新節點 `99`。請畫出插入後的結構，並標示哪些指標發生改變。

原始：

```
head → [10] → [20] → [30] → NULL
```

插入後（請畫出）：

&emsp;

&emsp;

&emsp;

指標變化說明：

&emsp;① 節點 ＿＿＿ 的 next 從指向 ＿＿＿ 改為指向 ＿＿＿

&emsp;② 新節點 [99] 的 next 指向 ＿＿＿

---

## 三、複雜度表格　（每格 3 分，共 27 分）

請填寫各操作的時間複雜度，並在「誰贏？」欄填入 Array / Linked List / 平手。

| 操作 | Array | Singly LL | 誰贏？ |
|------|:-----:|:---------:|:------:|
| 隨機存取 arr[i] | O(1) | | |
| 搜尋（未排序） | O(n) | | |
| 頭部插入 | O(n) | | |
| 尾部插入（有 tail 指標） | O(1) | | |
| 中間插入（已知位置） | O(n) | | |
| 中間插入（需先搜尋） | O(n) | | |
| 頭部刪除 | O(n) | | |
| 尾部刪除（Singly 無 prev） | O(1) | | |
| Cache 效能 | 優秀 | | |

---

## 四、簡答與分析題　（共 24 分）

**8.（12 分）** 說明 Singly、Doubly、Circular 三種 Linked List 的差異，各舉一個應用場景。

Singly Linked List（單向）：

&emsp;特徵：每個節點有 ＿＿＿ 個指標（next）

&emsp;應用場景：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

Doubly Linked List（雙向）：

&emsp;特徵：每個節點有 ＿＿＿ 個指標（prev + next）

&emsp;應用場景：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

Circular Linked List（環狀）：

&emsp;特徵：最後一個節點的 next 指向 ＿＿＿＿＿＿＿＿＿＿

&emsp;應用場景：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

---

**9.（12 分）** 給定 Linked List：`head → [5] → [3] → [8] → [1] → NULL`

請描述**刪除值為 3 的節點**的完整步驟，說明需要修改哪個指標，以及操作後的結構。

步驟①：

&emsp;＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

步驟②：

&emsp;＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

步驟③：

&emsp;＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

刪除後的結構：`head → [＿＿] → [＿＿] → [＿＿] → NULL`

此操作的時間複雜度：O(＿＿)　理由：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

---

<div style="page-break-before: always;"></div>

# ✦ 答案參考　（教師批改用，請勿發給學生）

---

**一、選擇題**

1. **B**　　2. **D**　　3. **B**　　4. **B**　　5. **C**

---

**二、繪圖題**

**6.** head 指向 n1（data=10），串接順序為：

```
head → [10 | ●]──→ [30 | ●]──→ [20 | ×] → NULL
```

（注意：順序是 10 → 30 → 20，不是 10 → 20 → 30）

**7.** 插入後結構：

```
head → [10] → [20] → [99] → [30] → NULL
```

① 節點 **[20]** 的 next 從指向 **[30]** 改為指向 **[99]**

② 新節點 [99] 的 next 指向 **[30]**

---

**三、複雜度表格**

| 操作 | Array | Singly LL | 誰贏？ |
|------|:-----:|:---------:|:------:|
| 隨機存取 | O(1) | **O(n)** | Array |
| 搜尋 | O(n) | **O(n)** | 平手 |
| 頭部插入 | O(n) | **O(1)** | Linked List |
| 尾部插入（有 tail） | O(1) | **O(1)** | 平手 |
| 中間插入（已知位置） | O(n) | **O(1)** | Linked List |
| 中間插入（需先搜尋） | O(n) | **O(n)** | 平手 |
| 頭部刪除 | O(n) | **O(1)** | Linked List |
| 尾部刪除 | O(1) | **O(n)** | Array |
| Cache 效能 | 優秀 | **差** | Array |

---

**四、簡答與分析**

**8.**
- Singly：1 個指標，記憶體最省，應用：Stack、簡單清單
- Doubly：2 個指標（prev+next），可雙向遍歷，應用：Browser History、LRU Cache
- Circular：最後節點 next 指回**第一個節點（head）**，應用：Round Robin 排程、音樂循環播放

**9.**
- 步驟①：從 head 開始遍歷，找到值為 3 的節點的**前一個節點**（即 [5]）
- 步驟②：將節點 [5] 的 next 指向節點 [3] 的 next（即節點 [8]）
- 步驟③：釋放節點 [3] 的記憶體（`delete`）

刪除後：`head → [5] → [8] → [1] → NULL`

時間複雜度：**O(n)**，因為需要從頭遍歷直到找到目標節點的前一個節點
