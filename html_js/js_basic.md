js_basic.md

JavaScript基本語法


# 標識符命名規則

1. 第一個字符必須是一個字母、下劃線（_）或美元符號（$）；
2. 剩下的其他字符可以是字母、下劃線、美元符號或數字。


# 註釋

// 單行註釋

/* 多行
註釋 */


# 嚴格模式

"use script";
略


# 分號與代碼塊

語句以分號結尾，可以省略，但是建議不省略
代碼塊使用{}標識，有些情況下可以省略，但是建議不省略


# 變量

## var 關鍵字

使用 var 操作符定義的變量會成為包含它的函數的局部變量。
如過省略 var，會被定義為全局變量，但不推薦。

## let 關鍵字

let 聲明的範圍是塊作用域，var 聲明的範圍是函數作用域。

## const 關鍵字

const 的行為與 let 基本相同，區別是聲明變量的時候，必須同時初始化變量，並且嘗試修改 const 聲明的變量會導致運行時錯誤。

## 不使用 var，const 優先， let 次之


# 數據類型

- Undefined     表示值未定義，是假值，唯一值 undefined，與 null 表面上相等
- Null          對空對象的引用，空對象指針，是假值，唯一值 null，與 undefined 表面上相等
- Boolean       表示值為布爾值，轉換函數 Boolean()
- Number        表示值為數值，特殊的數值 NaN，意思是 Not a Number，isNaN()函數判斷是否為NaN，轉換函數 Number()、parseInt()、parseFloat()
- String        表示值為字符串，字符串的長度通過 length 屬性獲取，轉換 toString() 方法、String() 函數、加上一個空字符串""
- Symbol        表示值為符號，使用 Symbol() 函數初始化。
- Object        對象通過 new 操作符後跟對象類型的名稱來創建。

## typeof 操作符（返回數據類型）

## 模板字面量 ``
## 字符串插值 ${} ，類似於Python的f字符串
## 標籤函數：略
## 原始字符串：標籤函數 String.raw、屬性 .raw


# 操作符

1. 遞增/遞減操作符  ++  --
2. 一元加和減  +  -
3. 位操作符（略）
4. 布爾操作符  邏輯非 !  邏輯與 &&  邏輯或 ||
5. 乘性操作符  乘法 *  除法  /  取模（餘數） %
6. 指數操作符  Math.pow()  **  **=
7. 加性操作符  +  -
8. 關係操作符  小於 <  大於 >  小於等於 <=  大於等於 >=
9. 相等操作符  等於 ==  不等於 !=  全等 ===  不全等 !== （推薦使用全等和不全等）
10. 條件操作符  variable = boolean_expression ? true_value : false_value
11. 賦值操作符  =  *=  /=  %=  +=  -=  <<=  >>=  >>>=
12. 逗號操作符  逗號操作符可以用來在一條語句中執行多個操作。


# 流控制語句

1. if 語句  if (condition1) {statement1} else if (condition2) {statement2} else {statement3}
2. do-while 語句  do {statement} while {expression}
3. while 語句  while (expression) {statement}
4. for 語句  for (initialization; expression; post-loop-expression) {statement}
5. for-in 語句  嚴格的迭代語句，用於枚舉對象中的非符號鍵屬性 for (property in expression) {statement}
6. for-of 語句  嚴格的迭代語句，用於遍歷可迭代對象的元素 for (property of expression) {statement}
7. label 語句  label: statement  可通過 break 或 continue 語句引用
8. break 和 continue 語句  break 退出循環；continue 退出當前循環
9. with 語句  將代碼作用域設置為特定的對象  with (expressiom) {statement}
10. switch 語句

switch (expression) {
    case value1:
        statement
        break;
    case value2:
        statement
        break;
    case value3:
        statement
        break;
    case value4:
        statement
        break;
    default:
        statement
}


# 函數

function functionName(arg0, arg1,...argN) {
    statements
}


# instanceof 操作符

result = variable instanceof constructor

檢測任何引用值和Object構造函數的類型


# 新對象通過使用 new 操作符後跟一個構造函數（constructor）來創建。

let  now = new Date();

要創建日期對象，就使用 new 操作符來調用 Date 構造函數。


# ECMAScript 通過 RegExp 類型支持正則表達式。正則表達式使用類型 Perl 的簡潔語法來創建：

let expression = /pattern/flags;
或
使用 RegExp 構造函數來創建

略


# trim()方法

創建一個字符串的副本，刪除前、後所有空格符，再返回結果。


# split()方法

返回的數組前後包含兩個空字符串。