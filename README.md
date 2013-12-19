# 【jQuery】チェックボックスを「全て選択」ボタンの設置方法

複数のチェックボックスを一度に全選択・全解除できるボタンを設置する方法です。
チェックボックスのグループが複数ある場合にも対応しています。

## デモ

<a href="http://klutche.github.io/checkAll/" class="link" target="_blank">デモ</a>

## Javascript

jQuery 依存のスクリプトなので、まず jQuery を読み込んでおきます。

  <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>

その下に以下のスクリプトを記載します。

  <script type="text/javascript">
  $(function(){
    $('.checkAll').on('change', function() {
      $('.' + this.id).prop('checked', this.checked);
    });
  });
  </script>

## HTML

  <input type="checkbox" id="group_01" class="checkAll"> 全て選択<br>
   
  <input type="checkbox" value="1" class="group_01"> 1<br>
  <input type="checkbox" value="2" class="group_01"> 2<br>
  <input type="checkbox" value="3" class="group_01"> 3<br>
  <input type="checkbox" value="4" class="group_01"> 4<br>
  <input type="checkbox" value="5" class="group_01"> 5<br>

全選択の起点となるチェックボックスにクラス checkAll を設定します。
クラス checkAll を付けたチェックボックスの id 値を、連動させたいチェックボックス全てに class の値として設定します。

## Github

<a href="https://github.com/klutche/checkAll" class="link" target="_blank">https://github.com/klutche/checkAll</a>
