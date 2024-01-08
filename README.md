# Properties Editor Plugin

> Eclipse에서 프로퍼티 파일 편집할 때, 잘 사용하던 플러그인인데, 
>
> 어느 순간부터 업데이트 사이트들이 먹통이 되서 설치를 할 수가 없다.
>
> 그러다가 어떤분이 SVN 소스를 받아 Git 레파지토리에 올려둔 것으로 보이는 것이 있어서, Fork를 받아두었다.



#### 현재 동작하지 않는 업데이트 주소

*  http://propedit.sourceforge.jp/eclipse/updates

  

#### 접속은 되지만 업데이트 동작이 실패하는 주소

* https://osdn.net/projects/propedit/storage/eclipse/updates/

  

#### SVN 주소

* http://svn.osdn.net/svnroot/propedit/

> 나도 여기서 소스를 받긴 했음.. 
>
> 당장은 모르겠지만 이 SVN Repo를 Git Repo로 전환하는 연습을 해봐도 좋을 것 같음.



---

그런데.. Java 8 이하라면 메시지 프로퍼티를 ISO-8859-1 인코딩에 유니코드 코드 값으로 저장을 해야했지만,

Java 9 부터는 UTF-8 형식으로 저장된 메시지 프로퍼티 파일을 바로 읽을 수 있기 때문에,

이 플러그인도 나중에는 점점 필요가 없어질 것 같긴하다.
