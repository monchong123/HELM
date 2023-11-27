# HELM
졸업프로젝트 2분반 6조

설치 환경<br/>
<front><br/>
비주얼 스튜디오 코드<br/>
node.js<br/>
React<br/>
<back><br/>
파이썬3.12<br/>
플라스크<br/>
<db><br/>
mysql8.0<br/>

설치법은 네이버, 구글 검색으로 따라하시면 됩니다. 특히, mysql 설치과정에서 본인만의 비밀번호를 설정하실텐데 꼭 필요하니까 주의하세요.<br/>

<설치가 다 됐다는 전제 하에><br/>
mysql workbench 열어서 connections 하나 생성하시고, 비밀번호 치고 들어가셔서 쿼리에<br/>
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%';<br/>
CREATE DATABASE blog CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;<br/>
use blog;<br/>
CREATE DATABASE testdb CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;<br/>
치고 전부 Ctrl+Enter(실행)하고 Sever Status(db서버실행)눌러서 서버 실행,<br/>

could not acquire management access for administration이라는 에러가 발생할 시 :<br/>
https://velog.io/@dongzooo/My-sql-workbench-%EC%97%90%EB%9F%AC%ED%95%B4%EA%B2%B0-could-not-acquire-management-access-for-administration<br/>

파이썬, 플라스크 설치 끝났으면cmd에 pip install -r requirements.txt 입력해서 종속성 설치. 설치 끝나면<br/>
 python wep.py 입력(백엔드 실행),<br/>

비주얼 스튜디오로 폴더 열기, 백엔드 파일에 있는 web.py파일을 열면<br/>
app.config["SQLALCHEMY_DATABASE_URI"] = "mysql+pymysql://root:159357jim@localhost:3306/testdb"<br/>
라는 코드가 보이는데, root:본인비밀번호@localhost:3306(=연결할 포트 번호:3306)/testdb(=연결할 데이터베이스) 라는 뜻이니 비밀번호 부분만 본인껄로 변경하면 됩니다.<br/>
변경하고 나면 Ctrl+Shift+` 를 눌러서 터미널 열고 코드에 비밀번호 변경(본인 mysql 비번으로 변경)후, npm start입력(프론트 실행)<br/>


<<주의사항>><br/>
1. cmd나 터미널에 명령어를 입력할 때는 파일 주소를 정확히 할 것.<br/>
ex)<br/>
예를 들어 C:\Users\soldesk\Downloads\SQLD에 있는 파일을 실행시키려 할때 주고가 C:\Users\soldesk\Downloads 이 상태면 실행오류가 납니다.<br/>
그럴땐 cd "C:\Users\soldesk\Downloads\SQLD"를 입력해서 경로를 정확히 해줘야 합니다.<br/>

2. 서버가 안열리면 비주얼 스튜디오를 먼저 열어서 root:비밀번호를 먼저 수정해주고, front 먼저 실행해보세요.<br/>

3. 구글검색과 챗GPT만 있어도 대부분의 문제는 해결 가능합니다.<br/>
