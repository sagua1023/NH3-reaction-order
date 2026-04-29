# NH3 GC Reaction Order Calculator

GitHub Pages용 정적 웹앱입니다.

## 사용법
1. GitHub repository를 만듭니다.
2. `index.html`, `style.css`, `app.js`를 root에 업로드합니다.
3. Settings → Pages → Branch: main, Folder: /root 선택.
4. 생성된 URL로 접속합니다.

## 핵심 계산식
NH3 -> 0.5 N2 + 1.5 H2

Ftot,out = Ftot,in + x  
FH2,out = FH2,in + 1.5x  
FN2,out = FN2,in + 0.5x  
FNH3,out = FNH3,in - x  

Calibration: y = m Area + b

x_H2 = (FH2,in - y_H2 Ftot,in)/(y_H2 - 1.5)  
x_N2 = (FN2,in - y_N2 Ftot,in)/(y_N2 - 0.5)  
x_NH3 = (FNH3,in - y_NH3 Ftot,in)/(1 + y_NH3)

X_NH3 = x / FNH3,in

Reaction order = slope of ln(rate) vs ln(partial pressure)
