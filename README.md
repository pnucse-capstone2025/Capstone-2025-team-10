## 레파지토리 제출

- **`[주의]` 레파지토리 제출**은 해당 레파지토리의 ownership을 **학과 계정**으로 넘기는 것이므로 되돌릴 수 없습니다.
- **레파지토리 제출** 전, 더 이상 수정 사항이 없는지 다시 한번 확인하세요.
- github 레파지토리에서 Settings > General > Danger zone > Transfer 클릭
  <img src="https://github.com/user-attachments/assets/cb2361d4-e07e-4b5d-9116-aa80dddd8a8b" alt="소유주 변경 경로" width="500" />
- [ Specify an organization or username ]에 'PNUCSE'를 입력하고 확인 메세지를 입력하세요.
  <img src="https://github.com/user-attachments/assets/7c63955d-dcfe-4ac3-bdb6-7d2620575f3a" alt="소유주 변경" width="400" />

---

![메인 이미지](/img/banner.png)

# TMOJI

![간단한 시연 gif](/img/sample.gif)

> 폰트 스타일을 유지하며 이미지를 번역하는 서비스


- 현재 사용되는 기계 번역(machine translation) 및 OCR(Optical Character Recognition) 기반의 대부분의 번역 및 삽입 기법은 단순히 인식된 텍스트를 기계적으로 치환하거나 이미지를 덮어쓰는 기법이므로 더 고도화된 방법이 필요
- 글꼴, 색상, 크기, 위치와 같은 시각적 요소까지 자연스럽게 반영하도록 구현하는 것이 목표

## 파트별 Repository
> 각 파트별 자세한 내용은 아래 Repository에 접속하여 확인할 수 있습니다.

<table>
  <thead>
    <tr>
      <th>분류</th>
      <th>URL</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">텍스트 변환 모델</td>
      <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/TextCtrl-Translate'>TextCtrl-Translate</a></td>
      <td>한국어 환경에 맞게 파인튜닝된 텍스트 변환 모델</td>
    </tr>
    <tr>
      <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/ko_trocr_tr'>ko-trocr-tr</a></td>
      <td>한국어 환경 TextCtrl에 필요한 한국어 OCR 모델</td>
    </tr>
    <tr>
      <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/SRNet-Datagen_kr'>SRNet-Datagen(ko)</a></td>
      <td>한국어 환경의 TextCtrl 학습에 필요한 데이터셋 Generator</td>
    </tr>
    <tr>
      <td rowspan="2">웹 서비스</td>
      <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/tmoji-web'>웹(FE)</a></td>
      <td>TMOJI 프론트엔드</td>
    </tr>
    <tr>
      <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/tmoji-server'>서버(BE)</a></td>
      <td>TMOJI 백엔드</td>
    </tr>
  </tbody>
</table>

## 전체 시스템 구조

![system](/img/system.png)


## 이용 방법

### [TMOJI 바로가기](https://tmoji.org)

1️⃣ 사진 업로드 및 언어 선택 <br/>
2️⃣ 이미지 내 번역할 영역 지정 <br/>
3️⃣ 감지된 텍스트 확인 및 수정 <br/>
4️⃣ 번역된 텍스트 확인 및 수정 <br/>
5️⃣ 최종 이미지 합성 진행 <br/>


## 설명 영상

[![부산대학교 정보컴퓨터공학부 소개](http://img.youtube.com/vi/zh_gQ_lmLqE/0.jpg)](https://www.youtube.com/watch?v=zh_gQ_lmLqE)

- 이때 유튜브 영상 썸네일 URL은 유투브 영상 URL로부터 다음과 같이 얻을 수 있습니다.

- `Youtube URL`: https://www.youtube.com/watch?v={동영상 ID}
- `Youtube Thumbnail URL`: http://img.youtube.com/vi/{동영상 ID}/0.jpg
- 예를 들어, https://www.youtube.com/watch?v=zh_gQ_lmLqE 라고 하면 썸네일의 주소는 http://img.youtube.com/vi/zh_gQ_lmLqE/0.jpg 이다.


## 시연 영상

https://github.com/user-attachments/assets/9be9105e-f36d-44f2-8044-7fa6fed25c2b

## 팀 구성

| 문경환 | 이동훈 | 이승재 |
|:-------:|:-------:|:-------:|
| <a href="https://github.com/drmoon-1st"><img width="100px" alt="문경환" src="https://avatars.githubusercontent.com/u/67881688?v=4" /></a> | <a href="https://github.com/bluelemon61"><img width="100px" alt="이동훈" src="https://avatars.githubusercontent.com/u/67902252?v=4" /></a> | <a href="https://github.com/Ea3214"><img width="100px" alt="이승재" src="https://avatars.githubusercontent.com/u/130594798?v=4" /></a> |
| drmoon@pusan.ac.kr | therqq13@pusan.ac.kr | leesj6717@pusan.ac.kr |
| 실험 환경 구축 및 실험 <br/> OCR 모델 및 TextCtrl 실험 및 분석 <br/> 방법론 탐색 및 결과 분석 <br/> 보고서 및 관련 문서 작성 | 서비스 파트 담당 <br/> UI/UX 구상 <br/> API 명세 및 데이터베이스 ERD 작성 <br/> FE & BE & Infra 총괄 | 딥러닝 모델 분석 및 개발 <br/> OCR 모델과 TextCtrl 모델 실험 및 재학습 <br/> 데이터 생성 파이프라인 재구성 <br/> 모델 SSH 연결 관련 BE 파트 개발 |

## 참고 문헌 및 출처

[1] Josh Achiam, Steven Adler, Sandhini Agarwal, Lama Ahmad, Ilge Akkaya, Floren-cia Leoni Aleman, Diogo Almeida, Janko Altenschmidt, Sam Altman, Shyamal Anad-kat, et al. Gpt-4 technical report. arXiv preprint arXiv:2303.08774, 2023. <br/> <br/>
[2] Kyunghyun Cho, Bart Van Merriënboer, Caglar Gulcehre, Dzmitry Bahdanau, Fethi Bougares, Holger Schwenk, and Yoshua Bengio. Learning phrase representa-tions using rnn encoder-decoder for statistical machine translation. arXiv preprint arXiv:1406.1078, 2014. <br/> <br/>
[3] Sepp Hochreiter and Jürgen Schmidhuber. Long short-term memory. Neural computa-tion, 9(8):1735–1780, 1997. <br/> <br/>
[4] Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan NGomez, Łukasz Kaiser, and Illia Polosukhin. Attention is all you need. Advances in neural information processing systems, 30, 2017. <br/> <br/>
[5] Linting Xue, Noah Constant, Adam Roberts, Mihir Kale, Rami Al-Rfou, Aditya Sid-dhant, Aditya Barua, and Colin Raffel. mt5: A massively multilingual pre-trained text-to-text transformer. arXiv preprint arXiv:2010.11934, 2020. <br/> <br/>
[6] Weichao Zeng, Yan Shu, Zhenhang Li, Dongbao Yang, and Yu Zhou. Textctrl: Diffusion-based scene text editing with prior guidance control. Advances in Neural Information Processing Systems, 37:138569–138594, 2024. <br/> <br/>
