# SEC-Ligitation-Release-Crawler

 - 說明：爬取美國證管會發佈的訴訟新聞稿，製成excel後作為後續text mining的材料
 - 使用工具：BeautifulSoup、Selenium、re
 - 遭遇問題：每段時期的articles html都不太相同，年份越早，資料越是以不規律方式存放，導致爬取失敗率居高不下，後續進行調整
 - 針對不同時期去撰寫程式碼
    - 2018 ~ => 2018以後的articles，存放位置固定，透過bs4即可抓取到所需資料
    - 2004 ~ 2017 => 這段期間的articles分成兩個部分取得，標題、編號等基本資料存放在h標籤裡，內文存放在p標籤裡，利用規律性以re分別抓取，失敗率大幅下降
    - ~ 2004 => 2004以前只能用string的方式去取得，尚待開發
