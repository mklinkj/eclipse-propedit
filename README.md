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


---
### UTF-8 프로퍼티 파일

Java SE 9에서는 프로퍼티 파일을 UTF-8 인코딩으로 로드합니다. 이전 버전에서는 ISO-8859-1 인코딩이 프로퍼티 리소스 번들을 로드하는 데 사용되었습니다. UTF-8은 비라틴 문자를 표현하는 데 훨씬 편리한 방법입니다.

대부분의 기존 프로퍼티 파일은 영향을 받지 않아야 합니다: UTF-8과 ISO-8859-1은 ASCII 문자에 대해 동일한 인코딩을 갖고 있으며, 사람이 읽을 수 있는 비ASCII ISO-8859-1 인코딩은 유효한 UTF-8이 아닙니다. 유효하지 않은 UTF-8 바이트 시퀀스가 감지되면 Java 런타임은 자동으로 파일을 ISO-8859-1로 다시 읽습니다.

문제가 있으면 다음 옵션을 고려하십시오:

- 프로퍼티 파일을 UTF-8 인코딩으로 변환합니다.

- 프로퍼티 파일의 인코딩에 대한 런타임 시스템 속성을 지정합니다. 예를 들면 다음과 같습니다:

  ```
  java.util.PropertyResourceBundle.encoding=ISO-8859-1
  ```

* https://docs.oracle.com/javase/9/intl/internationalization-enhancements-jdk-9.htm#GUID-974CF488-23E8-4963-A322-82006A7A14C7
  * https://github.com/adoptium/jdk8u/blob/master/jdk/src/share/classes/java/util/PropertyResourceBundle.java
  * https://github.com/adoptium/jdk17u/blob/master/src/java.base/share/classes/java/util/PropertyResourceBundle.java


---
### [수동 설치](Files)
수동 설치 관련해서는...

* jp.gr.java_conf.ussiy.app.propedit_6.0.5.jar
* jp.gr.java_conf.ussiy.app.propedit.nl_6.0.0.jar

위의 두 파일만 eclipse의 `dropins` 디렉토리에 넣어두면 설치가 된다.
