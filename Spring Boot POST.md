## POST API의 특징

- 리소스의 생성 및 추가하는 작업을 해주는 API이다.
- CRUD에서 C에 해당한다.
- POST Request를 반복한다면 데이터들은 계속 추가될 것이고 서버는 매번 다른 응답을 나타낼 것이다. 이때 응답이 같을 수도 있지만 응답이 같더라도 서로 다른 데이터기에 POST API는 멱등하지 않다.
- 또한 GET은 데이터를 읽어오기만 하여 안전성이 있었지만 POST의 경우는 데이터를 추가하며 조작하기에 안전성은 없다.
- Path Variable을 사용가능하다.
- Data Body를 사용 가능하다.

## POST API 사용

@PostMapping

```java
@RestController
@RequestMapping("/api")
public class PostApiController {

    @PostMapping("/post")
    public void post(@RequestBody Map<String,Object> requestData){ //post 방식에서는 RequestBody
        requestData.forEach((key, value) -> {
            System.out.println("key : " + key);
            System.out.println("value : " + value);
        });
    }

    @PostMapping("/post1")
    public void post1(@RequestBody PostRequestDto requestData){ //post 방식에서는 RequestBody
       System.out.println(requestData);
    }
}
```

Post는 Data block을 받기 위해 **@RequestBody**를 붙여준다.
