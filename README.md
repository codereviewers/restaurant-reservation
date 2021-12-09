# Restaurant Reservation 소개 

## 기능 명세
* BookingScheduler를 통해 시간대별 예약관리
* 예약은 정시에만 가능하다.
	* ex) 09:00(0), 09:03(x)
* 시간대별 수용가능 인원을 정할 수 있다.
	* 모든 시간대에 동일한 인원수 적용
	* 시간대별 수용가능 인원이상 예약요청시 Exception 발생
* 일요일은 예약이 불가하다.
	* ex) ‘20180916(일)’에 ‘20180917(월)’ 이용 예약 불가
	* ex) ‘20180917(월)’에 ‘20180923(일)’ 이용 예약 가능
* 예약완료 시 SMS발송
* E-Mail 주소가 있는 경우는 메일 발송

## 환경 설정
### 1. 프로젝트 다운로드 및 설정
* Clone 또는 zip 파일 다운로드
* IntelliJ로 프로젝트 열기
* JDK 버전 설정 

### 2. 패키지 추가
패지키 jar 파일로 다운로드 후 추가
* JUnit: https://mvnrepository.com/artifact/junit/junit/4.12
* Mockito: https://mvnrepository.com/artifact/org.mockito/mockito-all/1.10.19
* Joda-time: https://mvnrepository.com/artifact/joda-time/joda-time/2.9.9


## 실습 내용 
### 1. Test Case 작성
* JUnit 활용하여 Test Coverage 100% 되도록 작성.
* Mock Framework를 사용하지 않고 Test Case 작성.

### 2, Test Case 리팩토링
* 상수처리
* @Before

### Mock Framework를 사용하여 Test Case 리팩토링
Mockito Framework를 활용하여 리팩토링
* @RunWith(MockitoJunitRunner.class)
* @InjectMocks
* @Mock
* @Spy

### 디자인 패턴을 활용한 리팩토링
* Observer 패턴을 활용하여 리팩토링.
