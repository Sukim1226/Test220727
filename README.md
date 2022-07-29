# Test220727

## CPPChcek 실행
```
"c:\Program Files\Cppcheck\cppcheck.exe" --enable=all --inconclusive --xml --xml-version=2 src 2> cppcheck.xml
```


## Liazrd 설치
```
pip install lizard
```

## Lizard 실행해서 엑셀파일로 저장 (순환복잡도 10 이상)
```
lizard.exe -C 10 --csv > lizard_result.csv
```

## Lizard Jenkins 실행 설정
```
lizard ./src -C 10 -L 80 --xml > lizard.xml
```
or
```
"C:\Users\cypark\AppData\Local\Programs\Python\Python310\Scripts\lizard" ./src -C 10 -L 80 --xml > lizard.xml
```
## Jenkins의 CPPNCSS 플러그인 설치할 것

## 이후의 설정

![image](https://user-images.githubusercontent.com/8405564/176076421-faeea442-97b4-47c0-8abc-f251027a1fb2.png)


## CLOC 다운로드
[https://github.com/AlDanial/cloc/releases/tag/v1.92](https://github.com/AlDanial/cloc/releases/tag/v1.92)

## CLOC 실행
```
cloc-1.92.exe --by-file --csv . > cloc_result.csv
```

## CPD 실행
100 Token 이상, C++ 을 대상으로 분석, 엑셀에서 확인하기 위해 csv로 출력해서 저장
```
cpd.bat --minimum-tokens 100 --files . --language cpp --format csv > cpd_result.csv
```

### CPD Jenkins에서 실행
```
cpd --minimum-tokens 100 --files ./src --language cpp --format xml > cpd.xml || exit 0
```

### CPD Jenkins Report 설정
![image](https://user-images.githubusercontent.com/8405564/176077844-ea35faa3-84aa-4455-84e4-b968bb0be7e2.png)


