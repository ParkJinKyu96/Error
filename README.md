# Error<br>


## yellowError

### [1] _DontDestroyOnLoad only works for root GameObjects or components on root GameObjects._<br><br>

**이유** : DontDestroyOnLoad하는 스크립트는 대부분 싱글톤을 가진 스크립트로 이 스크립트를 가진 부모 오브젝트에 DontDestroyOnLoad를 시켜주지 않았기 때문입니다.<br>

**해결 방법** : 싱글톤을 가진 스크립트 오브젝트의 부모 또한 DontDestroyOnLoad를 시켜주는 방법과 부모 오브젝트에서 따로 분리 시켜야합니다.


 ![에러](https://user-images.githubusercontent.com/69668668/143507737-98b9eee5-0140-42c6-9350-471b6a318074.png)<br>
 
 - [Manager]오브젝트의 자식들로 들어있는 3개의 매니저들 중 2개는 DontDestroyOnLoad함수가 존재합니다.<br>
 하지만 3개의 매니저를 담고있는 빈 객체인 [Manager]오브젝트를 DontDestroyOnLoad시켜주지 않아 에러가 발생합니다.<br>
 
 ![에러](https://user-images.githubusercontent.com/69668668/143507614-d6ff3bea-7a69-4f30-9c02-c0d4b5230d1d.png)<br>
 
 - 다음과 같이 분리를 시켜주거나, [Manager]오브젝트에도 DontDestroyOnLoad함수를 추가 해줍니다.
 
