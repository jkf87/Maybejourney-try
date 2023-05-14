# Maybejourney

미드저니 UI: 우아하게 디자인되고 고도로 사용자 정의 가능한 인터페이스로, ChatGPT로 신속한 엔지니어링을 향상시키기 위해 특별히 제작되었습니다.

![](assets/preview.gif)

## Features

- 고도로 커스터마이징할 수 있는 미드저니 UI
- 사용자 갤러리
- ChatGPT 프롬프트 도우미

## Installation

> from https://github.com/George-iam/Midjourney_api#midjourney_api

1.  Discord 계정을 생성하고 서버를 생성합니다 (instruction here: https://discord.com/blog/starting-your-first-discord-server)
2.  미드저니 계정을 생성하고 미드저니 봇을 서버에 초대합니다(instruction here: https://docs.midjourney.com/docs/invite-the-bot)
3.  서버에서 생성 기능이 작동하는지 확인합니다.

![자료이미지](https://github.com/jkf87/Maybejourney-try/blob/main/KakaoTalk_20230514_144008529.png "4-5")


4. Chrome 브라우저에서 Discord에 로그인하여 서버의 텍스트 채널을 열고 오른쪽 상단 모서리에 있는 점 세 개를 클릭한 다음 추가 도구, 개발자 도구를 차례로 클릭합니다.(단축키 F12).
5. 네트워크 탭을 선택하면 페이지의 모든 네트워크 활동을 볼 수 있습니다.
6. 이제 텍스트 채널에 생성할 프롬프트를 입력하고 Enter 키를 눌러 프롬프트와 함께 메시지를 보내면 네트워크 활동에서 "상호작용(interaction)"이라는 새 줄을 볼 수 있습니다. 이 줄을 누르고 페이로드 탭을 선택하면 페이로드_json이 표시됩니다 - 이것이 바로 우리가 필요한 것입니다! 채널 아이디, 애플리케이션 아이디, 길드 아이디, 세션 아이디, 버전, 아이디 값을 복사하세요. 나중에 필요할 테니까요. 
7. 그런 다음 페이로드 탭에서 헤더 탭으로 이동하여 "권한(authorization)" 필드를 찾아 값을 복사합니다.

![7번자료이미지](https://github.com/jkf87/Maybejourney-try/blob/main/2023-05-14 14 53 46.png "7")
---
8. 페이로드(payload) 및 헤더(header) 값을 복사하여 `.env` 파일에 붙여넣습니다. (Rename `.env.template` to `.env`)
9. OpenAI API 키를 가져와서 `.env`에 복사/붙여넣기 합니다. [here](https://platform.openai.com/account/api-keys)
10. mj.db.template`의 이름을 `mj.db`로 변경하여 sqlite3 데이터베이스를 준비합니다.
11. 실행:

```
$ pip install -r requirements.txt
$ streamlit run Imagine.py
```

## Dependency

- streamlit==1.22.0
- streamlit_extras==0.2.7
- streamlit_pills==0.3.0
- apsw==3.41.2.0
- htbuilder==0.6.1
- openai==0.27.6
- pandas==1.4.4
- python-dotenv==1.0.0
- Requests==2.30.0

## Credits

- Midjourney
- YouTube [빵형의 개발도상국](https://www.youtube.com/@bbanghyong)

## Reference

- https://github.com/George-iam/Midjourney_api
- https://www.reddit.com/r/aipromptprogramming/comments/11xuxoh/prompt_the_ultimate_midjourney_texttoimage_bot
