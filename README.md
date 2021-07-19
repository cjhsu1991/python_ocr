# python_ocr
--- 使用 windows 64位元環境
1.  下載 tesseract-ocr-w64-setup-v5.0.0-alpha.20210506.exe 安裝到本機電腦上
2.  設定環境變數 在 Path 中加入:tesseract-ocr-w64-setup-v5.0.0-alpha.20210506.exe 的執行檔路徑
3.  如果要辨識繁體中文 下載 chi_tra 的 train data 資料放置到 C:\Program Files\Tesseract-OCR\tessdata 中
4.  撰寫 Python 程式進行程式辨識
```
安裝套件
!pip3 install pillow
!pip3 install pytesseract
------------------------------------
from PIL import Image
import pytesseract
img = Image.open('1.tif')
text = pytesseract.image_to_string(img, lang='chi_tra+eng')
print(text)
```
