![image](https://user-images.githubusercontent.com/87350774/149661521-3ca6f984-6813-4e6c-94fe-adb0b862cb8a.png)

- GET 어노테이션
    - @GetMapping : Get Resource 설정
    - @RequestParam  : URL Query Param Parsing
    - @PathVariable : URL Path Variable Parsing
    - Object : Query Param Object로 Parsing
    - @RestController : RestAPI 설정
    - @RequestMapping : 리소스를 설정(method로 구분가능)
    
- GET Method
    - 키 밸류값을 넣기 위해선 주소뒤에 ?로 시작하여 키 밸류값을 넣어주고 그 다음 키 밸류값을 넣기 위해 &연산자가 필요하다
    - map으로 받는 방법
        
        키 밸류값을 다 받을 수 있다
        
    - path variable로 받는 방법
        
        경로를 지정하여 요청하는 법(데이터의 위치를 특정해서 보여줘야 할 경우)
        
    - queryParameter로 받는 방법
        
        ? 뒤에 id란 변수에 값을 담아 백엔드에 전달하는 방식(정렬하거나 필터해서 보여줘야 할 경우)
