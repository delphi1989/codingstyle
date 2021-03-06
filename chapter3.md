# 三、原始碼結構

原始碼由以下幾個結構依序組成：

1. 著作權或版權資訊（有必要的話）
2. Package敘述
3. Import敘述
4. 一個頂層類別(**top-level class**)

結構間以一列空白行分隔

#### **3.1 著作權或版權資訊**

若檔案內需要有著作權或版權資訊時，必須呈現在原始碼檔案的最上方





---

#### **3.2 Package 敘述**

package敘述不進行***line-wrapper***，也就是不換行的意思。字元數限制不適用於package敘述。
>line-wrapper：原本只會有一行的程式敘述，為了不超過字元數的限制而分隔成很多行。通常一行程式敘述應介於80 ~ 100個字元數間。



---
#### **3.3 Import 敘述**

>3.3.1 不使用通用符號import (No wildcard imports)

不使用通用符號(```*```)或static import。

>3.3.2 不進行line-wrapper (No line-wrapping)

import敘述不進行***line-wrapper***，也就是不換行的意思。字元數限制不適用於import敘述。

>3.3.3 排序與間隔 (Ordering and spacing)

所有的import敘述會組合成不同的群組，群組間以一空白行做為分隔，依序為：

1. 所有的```static``` import
2. com.google開頭的 import(只有當原始碼檔案在com.goolge的package內時)
3. 所有第三方資源的import，例如：```android, com, junit, org, sun```，依ASCII順序排列
4. ```java``` imports
5. ```javax``` imports

import群組內以原始碼檔案名稱依照ASCII的順序進行排列，且群組內不會有空白列，以分號包裹敘述。

#### **3.4 類別宣告**

>3.4.1 只有一個頂層類別( Exactly one top-level class declaration)

一個頂層類別依附在自己的原始碼檔案內。

>3.4.2 類別成員排序(Class member ordering)

類別成員的順序對於學習有很大的益處，但並不存在一個一致的標準。不同的類別的類別成員擁有不同的順序。

重要的是讓類別以一個**有邏輯的方式**排序類別內的成員，使維護人員有辦法解釋、理解相關的問題。像是新建立的方法不能總是習慣性地放在類別原始碼的最底部，這雖然是依照時間排序，但並不是種有邏輯的方式，對於理解程式碼沒有幫助。

>>3.4.2.1 方法重載： 不要分割(Overloads: never split)

當一個類別擁有多個相同名稱宣告的建構子及方法時，應連續的排列，不被其他的類別成員隔開。








