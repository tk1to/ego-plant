**Mandragora-Rails API Document**
----
### **Root URL**
https://mandragora-rails.herokuapp.com

----
#### **`GET`** `/api/weather`
* #### 概要<br />
  現在時間の東京の気象情報を取得する。
* #### Parameters<br />
  なし
* #### Response
  - weather
    - Clear
    - Clouds
    - Rain
  - temp
    - 気温を華氏(°Ｆ)で表示。(そのうち摂氏(℃)に直します)
  - humidity
    - 湿度を(%)で表示。
```ruby
{
  "weather": "Clouds",
  "temp": 297.44,
  "humidity": 94
}
```
<br />

----

#### **`GET`** `/api/slack`
* #### 概要<br />
  Slackへのテスト通知。
* #### Parameters<br />
  なし
* #### Response
  - status
    - 固定。
```ruby
{
  "status": "alerted!"
}
```
<br />

---

#### **`GET`** `/moistures/create?value=***`
* #### 概要<br />
  湿り気データを作成
* #### Parameters<br />
  value [integer]
* #### Response
  - status
    - 固定。
```ruby
成功時
{
  "status": true,
  "msg":    "success!"
}
```
```ruby
失敗時
{
  "status": false,
  "msg":    "failed..."
}
```
