# financialDisclosure
공직자 재산공개 파일 변환 코드

대한민국 전자관보에서 공개되는 공직자 재산공개 파일을 txt 데이터 형식으로 변환할 수 있습니다.
국회와 대법원, 지방정부의 재산공개 역시 형식만 비슷하다면 변환 가능합니다.

먼저 pdf로 된 원본 파일을 xml형식으로 export해야 합니다.
아래한글이나 다른 포맷으로 공개된 문서가 있다면 pdf로 1차 변환 후 pdf를 xml로 export해서 사용하면 됩니다.  
이 코드를 이용해서 고위공직자 재산 xml파일을 데이터로 변환할 수 있습니다.
 
셀의 테두리 선들을 확인하면서 눈으로 보는 판단과 유사하도록 인지시켜 변환하는 방식입니다.
'인지'라는 고 수준의 단어를 사용하였지만, 결국 if절로 도배가 되어 있는 점 양해바랍니다.

중간에 에러가 발생하면 코드를 수정해 줄 수도 있지만 워낙 다양한 에러들이 있기 때문에 코드 수정으로 대응하기는 힘이 듭니다.
차라리 xml을 excel로 열어서 해당 부분의 테두리처리가 잘못 되어 있으면(사람이 눈으로 직접 봐도 표가 이상하게 되어 있으면) 해당 부분의 테두리나 데이터를 적절히 수정한 후 xml로 그대로 저장하여 다시 이 코드를 실행해보면 웬만한 경우 잘 됩니다.

애매한 경우가 발생할때는 경고 메시지가 출력되도록 하여 수정에 참고가 되도록 했습니다.

현재의 공직자재산공개파일변환에 최적화된 코드입니다. 
내용을 살펴보면 아시겠지만, 그리 스마트한 코드가 아니니, 더 좋은 코드로 수정해주실 분이 있다면 적극 환영합니다.
디버깅을 하지 않고 println으로 대신했습니다..... ^^; 

다른 언어로 포팅할 경우, 다른 사용자들을 위해서 이 문서들과 연결시켜주세요.

XMLParser.java
xml파일을 파싱하여 데이터로 저장하는 코드

BuildingPropertiesParser.java
전체재산 중 건물재산내역을 처리하여 표준화된 법정동주소를 뽑아내 는코드

나머지파일3개.txt
건물 재산 처리에 관련된 파일들
