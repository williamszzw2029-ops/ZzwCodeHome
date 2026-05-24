# 环境安装与打包说明（Windows）

## 一、安装第三方依赖（Windows）

```batch
pip install pandas numpy matplotlib PyQt5 openpyxl python-pptx zhconv
```

## 二、打包为单文件 exe（Windows）

推荐在虚拟环境中操作，避免打包多余环境：

```batch
python -m venv build_venv
build_venv\Scripts\activate
pip install pyinstaller pandas numpy matplotlib PyQt5 openpyxl python-pptx zhconv
pyinstaller --onefile --noconsole --clean --name "QualityAnalyseSystem" --icon QAS.ico QualityAnalyseSystemV1.1.py
```

打包完成后，单文件 exe 位于 `dist\QualityAnalyseSystem.exe`。
