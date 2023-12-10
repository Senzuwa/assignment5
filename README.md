# URLとは

URLは「Uniform Resouce Locater」の略称で、インターネット上に存在する情報資源（文書や画像など）の場所を指し示す技術方式.   

- 「プロトコル://ドメイン名/ディレクトリパス名/ファイル名」という形式で構成されているホームページのページの住所（アドレス）   

- 「http://」が一般的に用いられており、一方で「https://」は情報を暗号化して安全なやり取りができるような仕組みになっている.


# クエリ文字列
サーバに情報を送るためにURLの末尾に付け足す文字列（変数）のこと.   

- 「？」をURLの末尾につけ、その次に「パラメータ = 値」をつける.複数のパラメータを付ける場合は「＆」を用いる.

### クエリ文字列には2種類あり、用途が異なる

1.パッシブパラメータ   
 - パッシブパラメータはアクセス解析のためのパラメータで、表示されるコンテンツに影響はない.
 - ユーザがどこから自分のWebサイトへ辿り着いたのかを知るために、固有パラメータをつけて計測する.
  
  ↪︎一般的に、集客のためにWebサイトへの流出元を分析したいときや、リスティング広告から流入情報を知りたい時に使用される.





2.アクティブパラメータ   

 - アクティブパラメータは動的なページ結果の表示に用いられ、表示されるコンテンツに影響がある.
 - パラメータを付け加えることで、Webサイトの表示内容を変更する.

   ↪︎アクティブパラメータを用いることにより、商品一覧をサイズごとにフィルタリングしたり、価格順に並べたりすることができる.


⚠︎注意点   

「＝」の代わりに「:」や「,」を使用したり、「&」の代わりに「[]」を使用したりする非標準パラメータを使用すると検索エンジンに読み取れない可能性があるため、「?」、「=」、「&」を用いる必要がある.   

# パス変数   

パス変数(パスパラメータ)は、URLパスの一部を変数として利用するパラメータになり、URLでリソースを特定するのに使われている.   

例）`http://example.com/users/12345`   
- 12345の部分がユーザーIDなどを表す変数となっている.
- ユーザーIDとか記事IDなどがよく使われる.   
- 世の中の様々なサービスでパス変数を指定することで特定のユーザーの情報や記事の情報などを表示するために活用されている.


# クエリ文字列とパス変数の違いとは   

- 類似点:   
 - どちらもURLに用いられている.

- 相違点:
  - パス変数は特定のもの（画面など）を表示したいときに用いられる.
  - クエリ文字列は特定のものに条件を加える場合に用いられる.

# HTTPメソッドとは   

クライアントから発信されるHTTPリクエストは、どのリソースに対して何をしたいかを指示する.
「どの」リソースかは、URLで決定されるが、「何をしたいか」は別に指示する必要があり、そのためにHTTPメソッドが使用される.   

HTTPメソッドの例
| HTTPメソッド    | メソッドのはたらき    | 
| :-- | --- | 
| GET| リソース情報を取得する    | 
| POST    | 新しいリソース情報を送り込む    | 
| PUT    |  リソース情報を新しい情報で置き換える   | 
| PATCH    | リソース情報の一部を新しい情報で置き換える   | 
| DELETE    | リソース情報を削除する    |    

※ ブラウザの制約上、実際に用いられるのは「GET」,「POST」の2種類   

# リクエストヘッダ
HTTPヘッダーは、HTTPリクエストおよびHTTPレスポンスのフィールドで、メッセージや本文の意味や意図、内容のことを変更したり、より詳細に説明したりするための追加情報を渡すためのもの.

![image](https://github.com/Senzuwa/assignment5/assets/151819109/cfffe8aa-191c-4d38-b923-08f17680859d)   

[参考](https://wa3.i-3-i.info/word1844.html)   

# HTTPステータスコードとは   

HTTPステータスコードは、特定のHTTPリクエストが正常に完了したかどうかを示す3桁のコード.

HTTPステータスコードの例   
| HTTPステータスコード    | 説明  | 
| :-- | --- | 
|  200（OK）   | リクエストは正常に処理することができた    | 
|  201（Created）  | リクエストが成功してリソースの作成が完了    | 
|  400 (Bad Request)  | 一般的なクライアントエラー　| 
|  404 (Not Found)  | Webページが見つからない    | 
|  500 (Internal Server Error)  | 何らかのサーバー内で起きたエラー　|    

# レスポンスヘッダとは   

HTTPレスポンスとはWebブラウザからホームページのファイルが置いてあるWebサーバに対して出される「このページを閲覧したい」などのお願いに対するWebサーバからの返事のこと.   

このHTTPレスポンスは「ステータスライン」、「レスポンスヘッダ」、「レスポンスボディ」の三つの要素で構成されている.   

「HTTPレスポンスヘッダ」は上記の通り「HTTPレスポンス」を構成する部品のひとつであり、「HTTPステータスラインに書ききれないレスポンスの情報」が書かれている場所のこと.

# レスポンスボディとは

「HTTPレスポンスボディ」は「レスポンスヘッダ」同様、「HTTPレスポンス」を構成する部品のひとつであり、「相手が欲しがってたファイルの中身」が書かれている場所のこと.   


# JSONとは   

- JSONとは「JavaScript Object Notation」の略で、JavaScriptにおけるオブジェクトの書き方を参考に作られたデータフォーマット(データの記述形式)のこと.   
- JSONのもっとも基本的な形式は、データのキーと値を{ }の中にコロンで区切って記載するもの.

JSONの一例   


```
{
'name' = '仲林'
'age'  = '38'
'affiliation' = 'パイレーツ'
}
```

# 参照
[「分かりそう」で「分からない」でも「分かった」気になれるIT用語辞典](https://wa3.i-3-i.info/word1847.html)   
[Qiita](https://qiita.com/tbpgr/items/989c6badefff69377da7)    
[Notepm](https://notepm.jp/markdown-table-tool)    
[Mdn](https://developer.mozilla.org/ja/docs/Web/HTTP/Status)






