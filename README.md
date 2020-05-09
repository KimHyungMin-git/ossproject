
# 시계 재고관리 프로그램 #
이 프로그램은 여러 브랜드를 시계를 판매하는 그레이마켓과 같은 판매점에서
편하게 판매하는 시계들의 재고를 관리 할 수 있게 하는 프로그램이다.
## MAKE FILE 
Make 방법

        1.Make clean: object 파일과 main 실행파일 삭제
        
        2.Make main: product.o와 main 실행파일을 만듬
        
        3.Make main_debug: product.o와 디버그메크로가 포함된 main 실행파일을 만듬

Main 파일실행 방법

        ./main

## 메인메뉴 설명 ##

        1.create
        판매 할 새로운 시계에 대한 이름,브랜드명,사이즈,성별,가격,재고 수를 저장
        세일율은 자동으로 0으로 저장

        2.read
        이름을 입력하면 특정 시계의 이름,브랜드명,사이즈,성별,가격,세일이 적용된 가격, 재고 수,세일율을 불러와 보여줌

        3.update
   *이름을 입력하면 특정 시계의 브랜드명,사이즈,성별,가격 재고 수를 업데이트 할 수 있음
        *업데이트시 세일율은 자동으로 0으로 저장

        4.StockUpdate
        *이름을 입력하면 특정 시계의 재고 만을 업데이트 할 수 있다.

        5.Delete
        *이름을 입력하면 특정 시계의 레코드를 제거한다.

        6.List(Brand)
        *특정 브랜드 이름을 입력하면 그 저장된 특정 브랜드 시계들의 레코드를 모두 보여준다.

        7.List(Gender)
        *Man을 입력하면 저장된 남자 시계들의 레코드를, Woman을 입력하면 저장된 여자 시계들의 레코드를 모두 보여준다.

        8.List
        *저장된 모든 시계들의 레코드를 보여준다.

        9.SaveFile
        *저장된 모든 시계들의 레코드를 입력한 파일명으로 저장한다.

        10.RecallFile
        *특정 파일명을 입력하면 그 파일에 있는 시계 정보들을 불러온다.

        11.OrderByName
        *데이터 레코드를 이름 순으로 정렬시킨다.

        12.RecordOptimization
        *데이터 레코드 중 빈 곳을 끝으로 몰아준다.

        13.ApplyDiscount
        *특정 시계의 이름을 입력하면 그 시계의 가격을 알려주고 할인율을 입력하면 할인율에 따라 가격이 바뀐다.

## 시계 데이터 구조
```c
typedef struct st_watch{
    char name[20];  // 시계 이름
    char brname[20]; // 브랜드 이름
    char size[20];  // 시계 사이즈
    char gender[10];// 남성용,여성용
    float price;  // 시계 가격
    int stock; // 재고 수
    int sale; //세일율
} W_Record;
```
