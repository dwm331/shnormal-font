# shnormal-font

**jsdelivr cdn for jsPDF VFS font**

## 自定義中文(思源黑體)

參考資料: https://www.cnblogs.com/ww01/p/11496213.html

- 字型
https://github.com/be5invis/source-han-sans-ttf/releases


- 轉檔 
https://rawgit.com/MrRio/jsPDF/master/fontconverter/fontconverter.html

### 前端使用 jsPDF

- 套件網址
https://github.com/parallax/jsPDF

- 程式引用

引入 head

```html
<head>
	<!-- CDN https://github.com/dwm331/shnormal-font -->
	<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/dwm331/shnormal-font@v1.1/shnormal-normal_1.js"></script>
	<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/dwm331/shnormal-font@v1.1/shnormal-normal_2.js"></script>
	<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/dwm331/shnormal-font@v1.1/shnormal-normal_3.js"></script>
</head>
```

引入 script，載入字型

```javascript
const { jsPDF } = window.jspdf;
const doc = new jsPDF();

var jsPDFfont = jsPDFfont1 + jsPDFfont2 + jsPDFfont3;

doc.addFileToVFS('shnormal-normal.ttf', jsPDFfont);
doc.addFont('shnormal-normal.ttf', 'shnormal', 'normal');

// 字型列表
//console.log(doc.getFontList())

// 使用自訂字型
doc.setFont("shnormal", "normal");
```
