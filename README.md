# What is

StoryBoardのようにUI一覧を表示する

# Reference

MaterialButton
https://developer.android.com/reference/com/google/android/material/button/MaterialButton

## MaterialButton

cornerやstrokeなど見た目を細かく設定できる

styleとプロパティを組合わせてデザインを柔軟に変える事ができる

ボタンの色は
FillButtonでは背景が?attr/colorAccent,テキストはwhite
UnfilledButtonでは背景が透明,テキストが?attr/colorAccent

## Styles

| Style                                                  | 効果                |
|:-------------------------------------------------------|:------------------|
| Widget.MaterialComponents.Button                       | 標準のボタン            |
| Widget.MaterialComponents.Button.Icon                  | アイコン付き標準のボタン      |
| Widget.MaterialComponents.Button.OutlinedButton        | ボーダー付きボタン         |
| Widget.MaterialComponents.Button.OutlinedButton.Icon   | アイコン付きボーダー付きボタン   |
| Widget.MaterialComponents.Button.TextButton            | 塗りつぶしなしのボタン       |
| Widget.MaterialComponents.Button.TextButton.Icon       | アイコン付き塗りつぶしなしのボタン |
| Widget.MaterialComponents.Button.UnelevatedButton      | 高さのないボタン          |
| Widget.MaterialComponents.Button.UnelevatedButton.Icon | アイコン付き高さのないボタン    |


### Stroke

| attr                       |効果|
|:------------------|:--------|
| `app:strokeColor` | ストロークの色 |
| `app:strokeWidth` | ストロークの幅 |

- strokeWidthは初期値0pdなのでストロークを有効にしたい時は値を入れること

### Icon

| attr                       |効果|
|:------------------|:--------|
|`app:icon`|ボタンにアイコンを表示する|
|`app:iconPadding`|パディング|
|`app:iconTint`|塗りつぶし色|
|`app:iconTintMode`|ブレンドモード,アイコンのベースが黒だったせいか違いがわからない|
|`app:iconGravity`|start or textStart , start:アイコンが左端テキストが中央揃えになる,textStart:アイコンとテキストが中央揃えになる(new!)|


### cornerRadius

| attr                       |効果|
|:------------------|:--------|
|`app:cornerRadius`|ボタンを角丸にする50dp以上だと変化なし|

### rippleColor

| attr                       |効果|
|:------------------|:--------|
|`app:rippleColor`|リップルカラーを設定できる,実際には透明度50%が掛かる|

### backgroundTint

| attr                       |効果|
|:------------------|:--------|
|`app:backgroundTint`|ボタンの色を設定|
|`app:backgroundTintMode`|カラーブレンドモード|

## TextFields

https://github.com/material-components/material-components-android/blob/master/docs/components/TextInputLayout.md

Style一覧  
https://github.com/material-components/material-components-android/blob/master/lib/java/com/google/android/material/textfield/res-public/values/public.xml

## OutlineBox

styleにOutlinedBoxをセットする
パスがWidgetで始まるので間違わないこと

```xml
 <com.google.android.material.textfield.TextInputLayout
            style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"

            android:id="@+id/textInput1Layout2"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"

    />
```

## CornerRadius

| attr                       |効果|
|:------------------|:--------|
|app:boxCornerRadiusTopStart|パディングの設定|
|app:boxCornerRadiusTopEnd|パディングの設定|
|app:boxCornerRadiusBottomStart|パディングの設定|
|app:boxCornerRadiusBottomEnd|パディングの設定|

まとめては設定できないみたい

## Text

| attr                       |効果|
|:------------------|:--------|
|android:hint||
|app:hintEnabled
|app:errorEnabled||
|app:helperTextEnabled|機能しない？|
|app:helperText|Layoutの下にテキストを表示できる|
|app:counterEnabled|文字をカウントしてくれる,絵文字は2でカウントされる😴|
|app:counterMaxLength|最大文字数|
|app:boxBackgroundColor|Boxの背景色|
|app:boxStrokeColor|線の色,指定なしだと黒?|
|app:boxStrokeWidth|線の太さ|
|app:hintAnimationEnabled|アニメーションの有効化| 

## 以下はalpha版で使用可能

アイコン系


| attr                | 効果                         |
|:--------------------|:---------------------------|
| app:endIconDrawable | 指定なしだと丸に囲まれたxアイコン(テキストをクリアする) |
| app:endIconContentDescription                   ||
| app:endIconMode                                 |custom,none,password_toggle,clear_text,アイコン押下時の効果が変わる|

### EndIconMode


| attr                       |効果|
|:------------------|:--------|
|custom|詳細はドキュメントにて,割愛|
|none|表示しない（デフォルト）|
|password_toggle|入力文字のマスク切り替え|
|clear_text|テキストを消去する|


# その他

## BottomAppBar

埋め込み型FABのBottomBarを実装できる

## ViewDragHelper
DragでViewを動かしたい場合、その処理を移譲できる
https://medium.com/eureka-engineering/android%E3%81%AEviewdraghelper%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6youtube-soundcloud%E3%81%AE%E3%82%88%E3%81%86%E3%81%AA%E3%82%A2%E3%83%8B%E3%83%A1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%92%E5%AE%9F%E8%A3%85%E3%81%99%E3%82%8B-8d4ea7684165

