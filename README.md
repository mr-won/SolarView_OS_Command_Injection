post /conf_mail.php http/1.1 host: 10.1.1.1 user-agent: mozilla/5.0 (x11; cros x86_64 14541.0.0) applewebkit/537.36 (khtml, like gecko) chrome/117.0.0.0 safari/537.36 connection: close content-length: 75 content-type: application/x-www-form-urlencoded accept-encoding: gzip mail_address=;cat${ifs}/etc/passwd;&button=

- 공격 이름: `Command Injection`
- 판단 근거: 페이로드에 `cat${ifs}/etc/passwd` 명령어가 포함되어 있음
- 탐지 패턴: `;cat${ifs}/etc/passwd;`
- 설명: Command Injection은 웹 애플리케이션에 악의적인 시스템 명령어를 주입하여 서버에서 실행시키는 공격 기법입니다.
- 대응 방법: 입력값 검증 및 필터링 강화, 웹 방화벽(WAF)에서 명령어 주입 패턴 차단 규칙 추가
