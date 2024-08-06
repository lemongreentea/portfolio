1. 아파치 설치
2. 규칙 등록
3. 포트포워딩 설정
4. 프로젝트 빌드 npm run build
5. httpd.config 설정 변경
   <VirtualHost *:80>
    ServerAdmin admin@example.com
    DocumentRoot "C:/path/to/your/project/dist"

    <Directory "C:/path/to/your/project/dist">
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog "logs/project-error.log"
    CustomLog "logs/project-access.log" common

    ServerName [내ip주소]
</VirtualHost>
6. httpd -k start
