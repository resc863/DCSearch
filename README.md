# 디시인사이드 유해물 탐색기  
![image](https://user-images.githubusercontent.com/50689611/125586980-52466ae2-a6a1-4acc-818f-aa793dc58c1f.png)

Google Cloud Vision API를 이용해 게시글속 사진들의 유해성을 판단하는 프로그램입니다.  
JPG, PNG, BMP, WEBP, GIF 등을 지원하며, GIF는 전체 프레임중 일부만을 추출하여 검사합니다.    

## 처음 사용시 주의사항  
Vision API는 유료 서비스이므로 직접 구글 클라우드에서 결제수단을 등록하고 API 키를 발급받아 사용하여야 합니다.    

main.py를 실행한 뒤 게시판 id와 정식 갤러리/마이너 갤러리 여부를 넣어주면 됩니다.  
그리고 Vision.py의 my_key 부분을 알아서 API 키로 바꿔주시기 바랍니다.    
매달 1000회까지는 무료, 그 뒤로는 1000회당 $1.5씩 지불해야 합니다.  
## 현재 사용중 나타나는 문제점  
1. 가끔 게시판 속 사진이 크롤링이 되지 않습니다. 이 경우 Error 메시지를 보낸 뒤 다음 게시글로 이동해 작업을 계속합니다.
2. Vision AI가 정상적인 사진도 유해물로 분류할 때가 있습니다.
