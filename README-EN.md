[![Main Banner](/img/banner.png)](https://tmoji.org)

# TMOJI

![simple demo gif](/img/sample.gif)

> ## An Image Translation Service that Preserves Font Style

Most existing machine translation (MT) and OCR (Optical Character Recognition) based text insertion methods simply replace recognized text mechanically or overwrite the original image. Therefore, a more advanced approach is required.

Our goal is to naturally preserve and reflect visual elements such as **font style, color, size, and position** when translating text within images.

---

## Repositories by Component

> For detailed information about each component, please visit the repositories below.

<table> <thead> <tr> <th>Category</th> <th>URL</th> <th>Description</th> </tr> </thead> <tbody> <tr> <td rowspan="3">Text Transformation Models</td> <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/TextCtrl-Translate'>TextCtrl-Translate</a></td> <td>Fine-tuned text transformation model optimized for Korean language environments</td> </tr> <tr> <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/ko_trocr_tr'>ko-trocr-tr</a></td> <td>Korean OCR model required for TextCtrl</td> </tr> <tr> <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/SRNet-Datagen_kr'>SRNet-Datagen(ko)</a></td> <td>Dataset generator for training TextCtrl in Korean environments</td> </tr> <tr> <td rowspan="2">Web Service</td> <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/tmoji-web'>Web (Frontend)</a></td> <td>TMOJI frontend</td> </tr> <tr> <td><a href='https://github.com/PNU-CSE-Graduation-TMOJI/tmoji-server'>Server (Backend)</a></td> <td>TMOJI backend</td> </tr> </tbody> </table>

---

## Overall System Architecture

![system](/img/system.png)

> Figure. TMOJI system architecture.

The frontend (Vite & React) is delivered through CloudFront and S3, communicates with a Dockerized FastAPI backend via REST API, processes asynchronous tasks using Celery and Redis, stores data in PostgreSQL and S3, and connects to a dedicated Ubuntu-based AI server running the PyTorch TextCtrl model via SSH.

---

## How to Use

### 👉 [Go to TMOJI](https://tmoji.org)

1️⃣ Upload an image and select the target language <br/>
2️⃣ Select the region within the image to translate <br/>
3️⃣ Review and edit detected text <br/>
4️⃣ Review and edit translated text <br/>
5️⃣ Generate the final composited image <br/>

---

## Introduction Video

[2025 Spring Graduation Project 10 – TMOJI Introduction Video](https://www.youtube.com/watch?v=xpn8hlP2sX8)

---

## Demo Video

[https://github.com/user-attachments/assets/9be9105e-f36d-44f2-8044-7fa6fed25c2b](https://github.com/user-attachments/assets/9be9105e-f36d-44f2-8044-7fa6fed25c2b)

---

## Team Members

| Kyunghwan Moon | Donghoon Lee | Seungjae Lee |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| <a href="https://github.com/drmoon-1st"><img width="100px" alt="Kyunghwan Moon" src="https://avatars.githubusercontent.com/u/67881688?v=4" /></a> | <a href="https://github.com/bluelemon61"><img width="100px" alt="Donghoon Lee" src="https://avatars.githubusercontent.com/u/67902252?v=4" /></a> | <a href="https://github.com/Ea3124"><img width="100px" alt="Seungjae Lee" src="https://avatars.githubusercontent.com/u/130594798?v=4" /></a> |
| [drmoon@pusan.ac.kr](mailto:drmoon@pusan.ac.kr) | [therqq13@pusan.ac.kr](mailto:therqq13@pusan.ac.kr) | [leesj6717@pusan.ac.kr](mailto:leesj6717@pusan.ac.kr) |
| Experimental environment setup and evaluation <br> OCR & TextCtrl experiments and analysis <br> Methodology research and result analysis <br> Documentation and reporting | Service development lead <br> UI/UX design <br> API specification & database ERD design <br> FE, BE, and Infrastructure overall management | Deep learning model research and development <br> OCR & TextCtrl experimentation and retraining <br> Data generation pipeline reconstruction <br> Backend development for model SSH integration |

---

## References

[1] Josh Achiam, Steven Adler, Sandhini Agarwal, Lama Ahmad, Ilge Akkaya, Floren-cia Leoni Aleman, Diogo Almeida, Janko Altenschmidt, Sam Altman, Shyamal Anad-kat, et al. Gpt-4 technical report. arXiv preprint arXiv:2303.08774, 2023. <br/> <br/> [2] Kyunghyun Cho, Bart Van Merriënboer, Caglar Gulcehre, Dzmitry Bahdanau, Fethi Bougares, Holger Schwenk, and Yoshua Bengio. Learning phrase representa-tions using rnn encoder-decoder for statistical machine translation. arXiv preprint arXiv:1406.1078, 2014. <br/> <br/> [3] Sepp Hochreiter and Jürgen Schmidhuber. Long short-term memory. Neural computa-tion, 9(8):1735–1780, 1997. <br/> <br/> [4] Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan NGomez, Łukasz Kaiser, and Illia Polosukhin. Attention is all you need. Advances in neural information processing systems, 30, 2017. <br/> <br/> [5] Linting Xue, Noah Constant, Adam Roberts, Mihir Kale, Rami Al-Rfou, Aditya Sid-dhant, Aditya Barua, and Colin Raffel. mt5: A massively multilingual pre-trained text-to-text transformer. arXiv preprint arXiv:2010.11934, 2020. <br/> <br/> [6] Weichao Zeng, Yan Shu, Zhenhang Li, Dongbao Yang, and Yu Zhou. Textctrl: Diffusion-based scene text editing with prior guidance control. Advances in Neural Information Processing Systems, 37:138569–138594, 2024. <br/> <br/>
