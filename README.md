※使用python3

※jupyter notebook如果視覺化中文部分出現亂碼，可參考這篇 → https://goo.gl/ZM2JHk

1.套件安裝
pip install snownlp
pip install numpy
pip install matplotlib



2.執行jupyter notebook

(1)匯入套件。zeros:創建0矩陣 、 svd:奇異值分解

(2)定義標題、不需要的值與符號

(3)建立字典與文章技術變亮

(4)object.parse:文字小寫 → 濾掉停止詞語標點符號 → 詞頻技術

SVD分解出詞與主題的矩陣，矩陣表示出頻率與重要性，另外第二個矩陣s表示前後矩陣的關聯。

(5)object.parse:建構矩陣

(6)object:printA:矩陣呈現、資料視覺化

【標題】

從視覺化觀察：T1、T3、T6為一類、T2、T7、T9為一類，T4、T5、T8相對是比較遠離的。

[T1、T3、T6]

T1:風評：柯文哲打5大案導致外資投資減少，真假?

T3:風評：柯文哲是台北市長，不是中共同路人

T6:獨家民調：柯文哲連任台北市長的法寶 就靠這群人愛他

[T2、T7、T9]

T2:獨家民調：柯文哲連任台北市長的法寶 就靠這群人愛他

T7:為何柯P上任3年，做到那麼多前人沒做的?員工一句話，讓他悟出做老闆該有的高度

T9:陳昭南專欄：到底是誰在抹紅柯P

[T4、T5、T8]

T4:觀點投書：柯文哲開始「自我內爆」之後的台北市長選舉...

T5:民進黨台北市長選戰「黑馬」鄭麗君 蔡其昌籲「黨中央務必考慮這張牌」

T8:羅智強觀點：砍柯P砍到鄭文燦，陳金德是超級豬隊友

可以看出T1跟T3開頭同時有:「風評... 」，但覺得整體上仍缺乏很好的解釋力。

【文字】

斷詞斷得太細，這裡有點難觀察關聯性。


3.總結

(1).段詞使用結巴(jieba)斷字應該表現會更優異

(2).未來可用tf-idf 對[文章內容]做計算，矩陣內容會更加龐大，但可應用的地方上相對較廣。

(3).尚未達到【丟入內容，可判斷跟'柯文哲'有關聯】，未來可以用羅吉斯回歸嘗試。

(4).分類可嘗試用k-means，比較分群與效率效果會不會更好。
