# 면접대비 

### 1. 객체지향 프로그래밍(oop)
----------
   * 캡슐화: 객체 내부의 상태를 숨기고, 외부에는 필요한 인터페스만 제공.
   * 상속: 기존 클래스 속성과 메서드를 재사용하고 확장 기능
   * 다형성: 동일한 메서드가 다양한 방식으로 구현하는 방법(오버라이딩, 인터페이스)

### 2. MVC 패턴
---------
   * Model: 데이터베이스와 직접 상호작용하며 데이터를 처리.
   * View:  사용자에게 데이터를 보여주느 역할.
   * Controller: 사용자의 요청을 받고 Model과 View를 호출하여 처리.
    
     ```각자 역할에 집중할 수 있게끔하여 개발을 하고, 유지보수, 확장성, 유연성 증가하고 중복코당의 문제를 떄문에 사용합니다```

### 3. 세션(Session)과 쿠키(Cookie)의 차이점은 무엇인가?
-----------
    *  세션: 서버에 저장되는 방식. 서버에 저장되므로 보안성에 높지만, 
             클라이언트가 요청할 때마다 서버에서 정보를 확인 하기 때문에 서버의 부하가 증가 될 수 있다.
    
    *  쿠키: 브라우저에 데이터를 저장하는 방식. 외부에 노출될 위험성이 크다.


      Q: 그렇다면 세션이 서버에 부담을 주면 세션말고 쿠키를 써야하겠네요?
  
      A: 
         세션이 서버에 부담을 준다고 해서 반드시 쿠키로 대체해야 하는 것은 아닙니다, 
         예를 들면 
         용자가 로그인한 상태를 유지하거나, 장바구니에 담긴 상품 정보를 저장하는 데 세션을 사용.
        
         이유:
         민감한 사용자 정보(예: 사용자 ID, 인증 상태)는 클라이언트에 저장하면 보안 위험이 있으므로 서버에 안전하게 저장.
         쿠키 사용:
         사용자가 사이트를 방문한 적이 있는지 확인하거나, 비로그인 상태에서 장바구니 상태를 간단히 저장.
        
         이유:
         비로그인 상태에서는 민감한 데이터가 필요 없으며, 브라우저에 저장해 서버 부하를 줄일 수 있음.


### 4. PHP 관련 
  1. 접근제어자 설명?
   
     ```public, private, protected```

     ```public```: ```어디서나 접근 가능하도록 합니다.```

     ```private```: ```같은 클래스내에서 사용 합니다.```

     ```protected```: ```같은 클래스 및 자식 클래스에서 사용합니다.```
  
  3. PSR은 무엇인가?
     
     ``` php를 작성하기 위한 규칙으로 php 표준 규약입니다.```
  
  5. PSR 아는거 설명?

     ```PSR-1```:  파일은 태그는 <?php, <?= 태그만 사용해야한다, UTF-8 인코딩을 사용햐야한다. 클래스 상수는 모두 대문      자로 한다

     ```PSR-2```: 코딩스타일 가이드로  namespace선언 뒤에 빈 줄이 하나 있어야하며, use 선언 블록 뒤에 빈 줄이 하나 있어야 한다.

     ```PSR-3```: 로거 인터페이스

     ```PSR-4```: 파일경로에서 클래스를 자동으로드가이위한 규칙 가이드 <Namespace>/<subNameSpace>/<className>
  
  6. Null coalescing operator란?

     키워드가 ??인 이항 연사자로 완쪽의 값이 없으면 오른쪽 값이 출력되는 연산자

     ```$user = $_GET['user'] ?? 'guest';```

  7. PHP에서 참조란?

     C의 포인터와 비슷한 개녕으로 메모리 주소 공간을 의미하며  &키워드를 사용해 주소를 표시한다.
     남용하면 메모리 누수 문제가 발생할 가능성이 있습니다.

  9. include, require, include_once, require_once 차이점

     ```include```는 호출될때 파일을 포함시키며 파일이 없더라도 코드가 계속 실행

     ```require```는 무조건 파일을 포함시키며 파일 없다면 오류를 발생시켜 코드가 실행되지 않습니다.

     ```once```는 해당 파일을 오직 한번만 추가한다는 의미이다.
     
  10. Modern php란

      ```최신버전의 PHP사용```

      ```PSR 표준 준수```

      ```composer 사용```


   11.  PHP 스코프 연산자

       A : parent로 부모 클래스에 접근할 수 있고, self로 본인 클래스에 접근할 수 있음

  12. PHP 가비지 컬랙션

      A : PHP 5.3에 추가된걸로 메모리 관리법, 강제로 수집할 수 있고 가비지 수집 메커니즘을 켜거나 끌 수 있음

  13. PDO는 무엇인가
    
      A : PHP에서 데이터베이스에서 접속할 때 여러가지 처리하기 위한 메서드를 모은 클래스

  14. PHP 상수 선언
    
    A : define 함수를 사용하거나 클래스 내에서 const 키워드로 선언할 수 있음

  15. PHP는 서버에서 어떻게 동작하는가?

    A: PHP는 서버 측 스크립트 언어로, 웹 서버에서 요청을 받으면 PHP코드를 해석하고 실행하여 HTML을 클라이언트 반환합니다.
  16. PHP CGI(Common gateWay interface) 동작방법
    
    A: 웹 서버와 외부 프로그램을 연결해주는 표준화된 프로토콜로 클라이언트가 PHP파일 요청 시 웹서버가 CGI 프로세스를 호출 하고 요청마다 별도의 PHP 인터프리터 프로세스를 실행 되고 인터프리터가 스크립트를 실행하고 생성된 결과를 웹서버에 전달합니다

  단점: 각 요청마다 새로운 프로세스가 생성되므로  CPU와 메모리 사용량이 증가합니다.또는 병목 현상이 발생합니다.
  
  17. PHP-FPM(FastCGI Process Manage)

      A: CGI의 단점을 개선하고 PHP 인터프리터 프로세스를 재활용하여 선능을 높히는 방법으로 실행 시 하나의 마스터 프로세스를 생성하고 요청을 처리하기 위해 여러 개의 워커 프로세스를 미리 생성 합니다. 요청마다 새로운 프로세스를 생성하지 않아 CGI의 오버헤드를 제거.클라이언트가 PHP 요청 → 웹 서버(Nginx, Apache)가 FastCGI 프로토콜로 PHP-FPM에 전달.
PHP-FPM의 워커 프로세스가 요청을 처리하고 결과를 반환.
   
### 5. Composer
------------
   PHP 의존성 관리 도구로, 필요한 라이브러리 설치 및 자동로드에 사용됩니다.

   Q: Composer를 실무에서 어떻게 활용하셨나요?

   A: ``` monolog/monolog 라이브러리를 도입해 로깅 기능을 강화했고, JWT를 사용해서 JWT 생성 및 조회 기능 및 Autoload 기능을 통새 클래스 파일을 자동으로 로드하도록 설정하여 psr-4 규칙을 준수하도록 했습니다```

   Q: Composer 오토로딩에 대한 정보를 업데이트 해주는 명령어는?
   
   A: ``` composer dump-autoload ```

   Q PSR-4를 사용하는 이유?
   
   A: ```프로젝트의 파일과 클래스가 체계적으로 관리되며, include, require가 필요없어집니다. 네임스페이스를 사용햐 충돌을 방지하고, 모듈화된 코드를 작성 할 수 있습니다.```

### 5. 예외처리
   Q: PHP에서 에러 처리를 어떻게 구현했나요?
   
   A: ```데이터베이스 연결 시 try-catch문을 사용하여 예외처리 및 로깅하여 사용자에게 알리는 기능을 추가 했습니다.```



