1. 請說明 Fixnum (整數) 和 Float (浮點數) 之間的差異
  無小數點, 以及底層計算機結構用來配置記憶體空間大小及數值存放方式, float實作方式應以IEEE754為準

2. 今天有兩個字串：
  ```ruby 
  str1 = "Hallo Welt!" 
  str2 = " NTU Rails 261!"
  ```
請說明以下兩個印出字串的方式的不同處：
  ```ruby
  puts str1 + str2
  puts "#{str1}#{str2}"
  ```
  第一段印出需將兩段字串做串接後放入另一段更大的記憶體後再印出, 若需要處理的字串很多很大時會造成執行速度過慢, 第二段採用字串內嵌的方式, 僅將#{}裡的變數替換掉而已

3. 請解釋 array 和 hash 的不同處
array取值的方式用index, 從0到array.length-1為可存取之索引範圍
hash取值用key值, key值可不須為有序數字, 也可用字串作為鍵值, 類似Python的Dictionary或是Javascript的JSON

4. 請寫一段 code 從 [1, "a string", 3.14, [1,2,3,4]] 這個陣列找出所有非字串的值
  ```ruby
  arr = [1, "a string", 3.14, [1,2,3,4]]
  
  for i in (0...arr.length)
    if arr[i].class != "String".class
      puts arr[i].class
    else
      next
    end
  end
  ```

5. 請列出兩種產出亂數的方法
  ```ruby
  num = rand(1..5) # 1~5
  num = [1, 2, 3, 4, 5].shuffle.last
  ```

6. 請把 lesson1 程式碼裡的 calculator.rb 裡面的使用者輸入兩個數字的方式改寫成 method，並要有防止使用者亂輸入值的功能


7. 以下這段程式碼：
  ```ruby
  ((1 > 3)&&(true == true))||(!!!false)
  ```
  會執行出什麼結果？ 請試試不用 irb 算出結果
  true

8. 請問 binding.pry 是什麼？ 要如何使用它？
  用來中斷程式, 可監控執行程式中的變數資訊以及變數型態等功能

9. 下面的一段程式碼，請嘗試用其他方法把 if...else...end 簡化成一行

  ```ruby
  var = 5

  if var >= 5
  	return "var is greater than or equal to 5"
  else
  	return "var is less than 5"
  end
  ```
  
  ```ruby
  if var >= 5 then return "var is greater than or equal to 5" else puts "var is less than 5" end
  ```
