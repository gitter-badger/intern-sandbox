一、SVG:可縮放的向量圖形
‧與現有技術可以互動融合：CSS、JavaScript
‧開源前端技術，可以讀取原始碼
‧保持圖像清晰度，不會隨放大與縮小而有所失真，也不會大幅增加檔案的大小
‧可以被搜尋：以XML寫成，可被搜尋引擎讀取

二、製作.SVG
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg>
<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

...................
</svg>

三、在HTML中嵌入SVG

1.
<embed src="檔名.svg" type="image/svg+xml" />
優點：所有主要瀏覽器都支持，並允許使用腳本
缺點：不推薦在HTML4和XHTML中使用（但在HTML5允許）

2.
<object data="檔名.svg" type="image/svg+xml"></object>
優點：所有主要瀏覽器都支持，並支持HTML4、XHTML和HTML5標准
缺點：不允許使用腳本

3.
<iframe src="circle1.svg"></iframe>
優點：所有主要瀏覽器都支持，並允許使用腳本
缺點：不推薦在HTML4和XHTML中使用（但在HTML5允許）

4.
直接在HTML嵌入SVG代码
<html>
	<body>
		<svg xmlns="http://www.w3.org/2000/svg" version="1.1">...</svg>
	</body>
</html>

四、標籤

1.<rect>
<rect x="33" y="34" rx="10" ry="10" fill="white" stroke="black" stoke-width="3" width="75" height="75"/>

2.<circle>
<circle cx="80" cy="73" r="44" fill="#FF4343" stroke="#890000" stroke-width="5" />

3.<ellipse>
<ellipse cx="100" cy="75" rx="67" ry="44" fill="#77DD47" stroke="#246614" stroke-width="5"/>

4.<polygon>
<polygon fill="#68EADD" points="151,39 163,63 189,66 170,85 175,111 151,99 127,111 132,85 113,66 139,63 "/>

5.<line>
<line x1="0" y1="0" x2="300" y2="300" stroke="black" stroke-width="2"/>

6.<text>
<text x="0" y="15" fill="red“ style="font-size:24px;”>Hello</text>

<text x="0,20,50,80,120" y="60,80,70,55,60">Hello</text>

<text x="10" y="90" fill="red" rotate="30">Hello</text>

<text x="100" y="90" rotate="30,40,50,70,90" >Hello</text>

<text x="180" y="15" fill="red" style="font-size:24px; writing-mode: tb;">Hello</text>

<text x="180" y="100" textLength="100" lengthAdjust="spacing">Hello</text>

<text x="180" y="120" textLength="100" lengthAdjust="spacingAndGlyphs">Hello</text>

<text x="0,10,20,30,40" y="30">Hello</text>

<text x="0" y="60" dx="0,10,20,30,40">Hello</text>

<text>
  <tspan x="50" y="20" fill="brown">Hello</tspan>
  <tspan x="10" y="40" fill="pink">Hello</tspan>
  <tspan x="10,20,30,60,90" y="60" fill="blue">Hello</tspan>
  <tspan x="10" y="80,90,80,85,100" fill="black">Hello</tspan>
</text>

<defs>
 	<path id="a1" d="M0 50 C150 150 100 -50 300 50" stroke="#000" fill="none"/>
</defs>
<text>
	<textPath xlink:href="#a1">HelloHelloHelloHelloHello</textPath>
</text>
<text dy="30">
   <textPath startOffset="30%" xlink:href="#a1">HelloHelloHello</textPath>
</text>

7.<path>
M
<path d="M0 0" stroke="black"/>

H
<path d="M0 0 H50" stroke="black"/>

V
<path d="M0 0 V50" stroke="black"/>

L
<path d="M0 0 L50 50" stroke="black"/>

C
<path d="M0 0 C40 40,60 40,100,0" stroke="black" fill="none"/>

Q
<path d="M0 0 Q50 50, 100 0" stroke="black" fill="none"/>

S
T
Z


