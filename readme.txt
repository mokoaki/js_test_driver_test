docker pull java
docker run --rm -it --name js_test_driver -p 4224:4224 -v /Users/moko/Desktop/jstestdriver:/root/bin/test java

cd ~/bin
wget https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/js-test-driver/JsTestDriver-1.3.5.jar

# このへんでWifiを切っておくとデモ的に良いかもしれない

java -jar ./JsTestDriver-1.3.5.jar --port 4224

# ブラウザのキャプチャ
# 各ブラウザで localhost:4224 を開く

# もう一つコンソールを開く
docker exec -it js_test_driver bash

cd ~/bin
java -jar ./JsTestDriver-1.3.5.jar --tests all --config test/jsTestDriver.conf



// window.navigator.userAgent
