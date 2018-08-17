# Html5_Project
## 目錄
* [環境設置](https://github.com/Ura777/Html5_Tutorial#%E7%92%B0%E5%A2%83%E8%A8%AD%E7%BD%AE)
* [Java環境變數設置](https://github.com/Ura777/Html5_Tutorial#java%E7%92%B0%E5%A2%83%E8%AE%8A%E6%95%B8%E8%A8%AD%E7%BD%AE)
* [Visual Studio Code相關設定](https://github.com/Ura777/Html5_Tutorial#visual-studio-code%E7%9B%B8%E9%97%9C%E8%A8%AD%E5%AE%9A)
* [課程介紹](https://github.com/Ura777/Html5_Tutorial#%E8%AA%B2%E7%A8%8B%E4%BB%8B%E7%B4%B9)
  * [Ch01 - Tomcat的管理](https://github.com/Ura777/Html5_Tutorial#ch01---tomcat%E7%9A%84%E7%AE%A1%E7%90%86)
  * [Ch02 - 基本的Html5](https://github.com/Ura777/Html5_Tutorial#ch02---%E5%9F%BA%E6%9C%AC%E7%9A%84html5)
  * [Ch03 - 文字與排版](https://github.com/Ura777/Html5_Tutorial#ch03---%E6%96%87%E5%AD%97%E8%88%87%E6%8E%92%E7%89%88)
* * *
## 環境設置
* 作業系統 = Windows 7
* JDK版本 = [1.8.0_171](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Apache Tomcat版本 = [9.0.8](https://tomcat.apache.org/download-90.cgi)
* Visual Studio Code版本 = [Windows x64 User Installer Stable Build](https://aka.ms/win32-x64-user-stable)
* * *
## Java環境變數設置
* 取得並複製JDK安裝路徑  
 
        路徑通常為：  
		C:\Program Files\Java\jdk1.8.0_162
 
* 控制台 &gt; 所有控制台項目 &gt; 系統 &gt; 點選右邊的進階系統設定 &gt; 點選上方的進階標籤 &gt; 環境變數
* 在Administrator的使用者變數(U)區塊中點選新增按鈕，根據對應的欄位輸入以下的資料：  
 
    | 欄位名稱      | 輸入內容                            |
    |:-------------:|:-----------------------------------:|
    | 變數名稱(N)   | JAVA_HOME                           |
    | 變數值(V)     | C:\Program Files\Java\jdk1.8.0_162  |
 
* 在系統變數(S)的區塊中點選變數名稱為Path的選項 &gt; 點選編輯按鈕
* 按下鍵盤的右方向鍵 &gt; 輸入分號 &gt; 輸入以下內容：  
 
        %JAVA_HOME%\bin;
 
* 輸入完之後，一直按下確定按鈕。
* 打開命令提示字元視窗，輸入以下指令後按下Enter：  
 
        java
 
* 出現列表Java的功能列表，代表環境變數設置成功。
* * *
## Visual Studio Code相關設定
* 更改字體大小
  * 上方選單點選檔案 &gt; 喜好設定 &gt; 設定
  * 點選右邊視窗的使用者設定標籤，在下方輸入以下程式碼：
 
        {  
            "editor.fontSize": 22
        }
 
  * 按下快捷鍵Ctrl+S儲存
* * *
## 課程介紹
## Ch01 - Tomcat的管理
* 更改通訊埠
  * 去安裝Tomcat的路徑中尋找server.xml
 
        路徑通常為：  
		C:\Program Files\Apache Software Foundation\Tomcat 9.0\conf\server.xml
 
  * 使用文字編輯器開啟server.xml &gt; 尋找以下的程式碼：
 
        <Connector port="8080" protocol="HTTP/1.1"  
               connectionTimeout="20000"  
               redirectPort="8443" /> 
 
  * 將8080改成想要設定的數字
 
        例如：
		80
 
  * 修改完成後儲存檔案 &gt; 重新啟動Tomcat
* 虛擬資料夾與真實資料夾的對應
  * 去安裝Tomcat的路徑中尋找server.xml
 
        路徑通常為：  
		C:\Program Files\Apache Software Foundation\Tomcat 9.0\conf\server.xml
 
  * 使用文字編輯器開啟server.xml &gt; 尋找以下的程式碼：
 
        <Host name="localhost"  appBase="webapps"  
            unpackWARs="true" autoDeploy="true">
 
  * 在上述的程式碼下方新增以下的程式碼：
 
        <Context path="/虛擬資料夾名稱" docBase = "實體資料夾位置" debug="0" />  
		  
		例如：  
		<Context path="/test" docBase = "C:\Html5_Tutorial" debug="0" />
 
  * 修改完成後儲存檔案 &gt; 重新啟動Tomcat
  * 虛擬資料夾與實體資料夾的名稱都不能有中文字
* * *
## Ch02 - 基本的Html5
* 第1個Html5
  * Hello World!!!
* section
  * 區段結構
  * 不要把section拿來當作div的替代標籤使用
* nav
  * 導引
* header與footer
  * header為頁首
  * footer為頁尾
* aside
  * 側邊欄
* address
  * 可以放置聯絡資訊
  * 文字樣式為斜體
* time
  * pubdate屬性為發布日期
* * *
## Ch03 - 文字與排版
* p
  * 段落
* blockquote
  * 引用
* annotation
  * 註解
* hr
  * 水平線
* pre
  * 定義格式
  * 可以保留空格與換行符號，通常用來顯示程式碼。
* h1~h6
  * 標題樣式
  * 1的字體最大，6的字體最小。
* div
  * 區塊
  * 可以與CSS搭配使用
* font
  * Html5不支援，請使用CSS代替。
* sup與sub
  * sup為上標效果
  * sub為下標下果
* ruby、rt與rp
  * 可以顯示注音或是拼音
  * 如果瀏覽器不支援ruby標籤，將會顯示rp標籤內的內容。
* br
  * 換行
* span
  * 同一行的區塊
  * 可以與CSS搭配使用
* ul、li
  * 沒有排序的項目清單
* ol、li
  * 有排序的項目清單
* dl、dt、dd
  * 可以製造出縮排的效果
* ins與del
  * ins為插入
  * del為刪除
* 特殊符號
  * &copy;
  * &lt;
  * &gt;
  * &quot;
  * &amp;
  * 半形空白
* * *


