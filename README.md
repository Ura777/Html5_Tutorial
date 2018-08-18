# Html5_Project
## 目錄
* [環境設置](https://github.com/Ura777/Html5_Tutorial#%E7%92%B0%E5%A2%83%E8%A8%AD%E7%BD%AE)
* [Java環境變數設置](https://github.com/Ura777/Html5_Tutorial#java%E7%92%B0%E5%A2%83%E8%AE%8A%E6%95%B8%E8%A8%AD%E7%BD%AE)
* [Visual Studio Code相關設定](https://github.com/Ura777/Html5_Tutorial#visual-studio-code%E7%9B%B8%E9%97%9C%E8%A8%AD%E5%AE%9A)
* [課程介紹](https://github.com/Ura777/Html5_Tutorial#%E8%AA%B2%E7%A8%8B%E4%BB%8B%E7%B4%B9)
  * [Ch01 - Tomcat的管理](https://github.com/Ura777/Html5_Tutorial#ch01---tomcat%E7%9A%84%E7%AE%A1%E7%90%86)
  * [Ch02 - 基本的Html5](https://github.com/Ura777/Html5_Tutorial#ch02---%E5%9F%BA%E6%9C%AC%E7%9A%84html5)
  * [Ch03 - 文字與排版](https://github.com/Ura777/Html5_Tutorial#ch03---%E6%96%87%E5%AD%97%E8%88%87%E6%8E%92%E7%89%88)
  * [Ch04 - 表格](https://github.com/Ura777/Html5_Tutorial#ch04---%E8%A1%A8%E6%A0%BC)
  * [Ch05 - 表單](https://github.com/Ura777/Html5_Tutorial#ch05---%E8%A1%A8%E5%96%AE)
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
## Ch04 - 表格
* table、tr、td、th
  * table為最外層的表格
  * tr為列
  * td為行
  * th為行標題
* caption
  * caption為表格標題
  * 通常放在table標籤上方
* colspan屬性
  * 水平方向的合併
  * 行的合併
* rowspan屬性
  * 垂直方向的合併
  * 列的合併
* thead、tbody、tfoot
  * thead為表首
  * thead為表身
  * tfood為表尾
* colgroup、col
  * colgroup內的子標籤為col
  * col可以決定行的外觀樣式
  * col可以使用的屬性
    * span
    * style
* 表格通常會搭配CSS進行修飾，使表格更加地美觀好看。
* * *
## Ch05 - 表單
* form
  * form為表單的最外層
  * 常用的屬性
    * method
    * action
  * 子標籤通常為input
* input
  * 輸入標籤
  * 常用的屬性
    * name
    * type
* button
  * 按鈕
  * 按鈕的種類
    * submit
    * reset
    * button
* text
  * 文字方塊
* textarea
  * 文字區域欄位
* radio
  * 單選核取元件
  * name屬性為同樣的名稱時，代表示在同一個群組。
* checkbox
  * 複選核取元件
  * name屬性為同樣的名稱時，代表示在同一個群組。
* select
  * 下拉式選單
  * 加上multiple屬性就可以複選
* password
  * 密碼欄位
* email
  * 電子信箱地址欄位
  * 送出表單時，會自動檢查是否符合電子郵件地址的格式。
* url
  * 超連結欄位
* search
  * 輸入列
* tel
  * 電話號碼欄位
* 與日期或是時間有關的欄位
  * date
  * time
  * month
  * week
  * datetime-local
  * 瀏覽器已經不支援datetime
* color
  * 色彩欄位
* range
  * 範圍欄位
* datalist
  * 資料清單
  * datalist的id要與input標籤的list屬性名稱相同
* number
  * 數字欄位
* label
  * 標籤
* fieldset
  * 表單分組
  * 子標籤為legend
  * legend為分組標題
* output
  * 顯示計算或是處理的結果
* progress
  * 進度條
* meter
  * 顯示某個範圍內的比例或量標
* optgroup
  * 替一群option加上共同的標籤
* * *


