## JSON이란?

JSON은 Object, Array, Key-Value 형태로 이루어져 있으며 String, Int, Long, Boolean 등의 타입을 지원합니다.

### Object

`Object`는 `{ }`(curly brace)로 감싸여 있는 것을 말합니다. 예를들어 아래 JSON 코드는 1개의 Object가 있고 그 Object는 title, url, draft, star라는 4개의 key와 그에 해당하는 value를 갖고 있습니다.



## JSON 파싱

다음 3종류의 JSON을 파싱하는 예제를 소개합니다.

1. 간단한 Key-Value만 있는 JSON
2. 하위에 여러 Object가 있는 JSON
3. Array가 있는 JSON

```java
import org.json.JSONArray;
import org.json.JSONObject;

public void jsonParsing1() {
    String jsonString = "{\"title\": \"how to get stroage size\","
            + "\"url\": \"https://codechacha.com/ko/get-free-and-total-size-of-volumes-in-android/\","
            + "\"draft\": false,"
            + "\"star\": 10"
            + "}";

    // JSONObjet를 가져와서 key-value를 읽습니다.
    JSONObject jObject = new JSONObject(jsonString);
    String title = jObject.getString("title");
    String url = jObject.getString("url");
    Boolean draft = jObject.getBoolean("draft");
    int star = jObject.getInt("star");

    System.out.println("title: " + title);
    System.out.println("url: " + url);
    System.out.println("draft: " + draft);
    System.out.println("star: " + star);
}
```

