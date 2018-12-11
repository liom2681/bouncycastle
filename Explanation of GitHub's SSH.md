# *Github SSH*

### SSH(Secure Shell)? 


```
네트워크 상의 다른 컴퓨터에 로그인하거나 
원격 시스템에서 명령을 실행하고 다른 시스템으로 파일을 복사할 수 있도록 
해 주는 응용 프로그램 또는 그 프로토콜을 가리킨다.
 - wikipedia -
```
##### 자료출처 :[SHH_위키백과](https://ko.wikipedia.org/wiki/%EC%8B%9C%ED%81%90%EC%96%B4_%EC%85%B8) 

![](https://github.com/liom2681/bouncycastle/blob/20157131/images/image1.png)
![](https://github.com/liom2681/bouncycastle/blob/20157131/images/image2.png)
--------------------------------------------------------------------------------
#### git_SSH설정 
```
 id_rsa     : private key 저장 되어 있다.
 id_rsa.pub : public  key 저장 되어 있다.
 
 id_ras.pub 파일에 있는 암호된 메시지
  - ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCqduxCothoenqH50HtABJglTv9CZe01tq+1hj2zy8IplHRnWiW1w...생략
    이내용을 그대로 server에 등록 한다. 
 
     Server                    client
 -------------              --------------   
 | public key |             | prvate key |
 --------------             --------------
     암호문     <-------      private key            
       |
       ∨
     복호화           
    (server에 저장된 공개키로 암호된 메시지를 client에 있는 private key로 복호화 하여서자동로그인을 하게 될 수 있다.)
```
### github에 public_key 설정 하는방법
- *setting ->  SSH and GPG Key -> new SSH Key*
- id_rsa.pub 내용을 그대로 복사하여 저장한다.
- 원격 저장소에 공개키가 저장.

![](https://github.com/liom2681/bouncycastle/blob/20157131/images/image4.png)


### git.ssh로 접속 하기
> clone or download -> use SSH 선택 -> git clone  git@github.com:khk37601/implement-of-C-DataStructure.git
>  -> continue connecting(yes/no) y -> private key 입력 
### 차이점
 ```
  HTTPS :  https://github.com/khk37601/implement-of-C-DataStructure.git
  SSH   :  git@github.com:khk37601/implement-of-C-DataStructure.git
 ```
![](https://github.com/liom2681/bouncycastle/blob/20157131/images/image6.png)

```
   Test_SSH.txt 파일을 만들어 저장소에 push가 되는지 확인 
   push가 잘되면 아이디 , 비빌번호를 묻지 않고 수행하게 된다.
```




