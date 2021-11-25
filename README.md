# Error<br>


## yellowError

[1] _DontDestroyOnLoad only works for root GameObjects or components on root GameObjects._<br>

**이유** : DontDestroyOnLoad하는 스크립트는 대부분 싱글톤을 가진 스크립트로 이 스크립트를 가진 부모 오브젝트에 DontDestroyOnLoad를 시켜주지 않았기 때문입니다.<br>

**해결 방법** : 싱글톤을 가진 스크립트 오브젝트의 부모 또한 DontDestroyOnLoad를 시켜주는 방법과 부모 오브젝트에서 따로 분리 시켜야합니다.


 ![에러](https://user-images.githubusercontent.com/69668668/143507351-6f8c327b-5dc5-45b8-b924-90f19ce3eeaf.png)<br>
 
 [Manager]오브젝트의 자식들로 들어있는 3개의 매니저들 중 2개는 DontDestroyOnLoad함수가 존재합니다. 하지만 [Manager]오브젝트는 DontDestroyOnLoad시켜주지 않아 에러가 발생합니다.<br>
 
 
 
