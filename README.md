### DEV-TO-SERVICE, PORTABLE KUBERNETES INFRASTRUCTURE
**🚀 쿠버네티스 클라우드 인프라 구축**<br>
본 포트폴리오는 일반PC에 쿠버네티스 인프라를<br>
운용하는 프로젝트 입니다.<br>
스팀덱은 기본운영체제가 리눅스 기반이라,<br>
윈도우 환경은 필수인 가상화 구성을 하지 않고도<br>
클라우드환경을 구축할 수 있습니다.<br>
실제 상용으로 쓰이는 소프트웨어들은 리소스 사용량이 많아,<br>
필요한 소프트웨어에 대응하는<br>
미니멀하고 경량화된 오픈소스들로 구성했습니다.

---

K3s - 쿠버네티스 파드 정보
![K3s](images/k3s.webp)

PostgreSql, DBeaver - 데이터베이스
![PostgreSQL](images/postgresql.webp)

VSCode, SpringBoot - 프로젝트 소스
![VSCode](images/vscode.webp)

Gitea - 소스코드 저장소
![Gitea](images/gitea.webp)

GiteaAction - 소스코드 빌드
![Build](images/build.webp)

GiteaAction, Kaniko - 도커라이징, 컨테이너 등록
![Dockerize](images/dockerize.webp)

Gitea - 컨테이너 레지스트리
![Registry](images/registry.webp)

ArgoCD - 최신 컨테이너로 파드 생성
![Deploy](images/deploy.webp)

ArgoCD - 스프링부트 파드 스타트
![SpringBoot](images/springboot.webp)

ArgoCD - 3개의 파드로 스케일링
![Scale](images/scale.webp)

Chrome - 스프링부트 프로젝트 접속
![Service](images/service.webp)





#### 🌐 적용 소프트웨어
* **SpringBoot (Framework):** 자바 기반의 표준 웹 애플리케이션 프레임워크입니다. 빠른 개발 속도와 높은 확장성을 바탕으로 실제 비즈니스 로직을 구동합니다.
* **PostgreSQL (Database):** 엔터프라이즈급 오픈소스 RDBMS입니다. 강력한 데이터 무결성을 제공하며 서비스의 모든 데이터를 안전하게 관리합니다.
* **K3s (Orchestration):** CNCF 인증을 받은 경량화된 쿠버네티스입니다. 단일 노드(스팀덱) 환경에 최적화되어 있으면서도 표준 쿠버네티스의 모든 기능을 수행합니다.
* **Gitea (SCM & Registry):** 외부 의존성(GitHub 등)을 배제한 온프레미스 코드 저장소입니다. 빌드된 컨테이너 이미지를 보관하는 Registry 기능까지 통합 운영합니다.
* **Kaniko (Image Builder):** 도커 데몬 없이 컨테이너 이미지를 제작하는 보안 최적화 도구입니다. 리소스 점유율이 낮아 저사양 하드웨어에서도 안정적인 패키징이 가능합니다.
* **ArgoCD (GitOps):** 'Git에 기록된 상태'와 '실제 서비스 상태'를 강제로 일치시키는 배포 자동화 도구입니다. 설정 변경만으로 서비스 확장(Scaling)과 롤백을 처리합니다.

#### 🏗️ 엔터프라이즈 기술 매핑
| 분류 | 적용 기술 | 기업용 솔루션 대응 |
| :-- | :-- | :--- |
| **Kubenetes** | **K3s** | **Kubernetes, EKS** |
| **Repository** | **Gitea** | **GIT, SVN, GitLab, GitHub** |
| **Build** | **Gitea-Action** | **Jenkins, CodePipeline** |
| **Packaging** | **Kaniko** | **Docker, CodeBuild** |
| **Container** | **Gitea** | **DockerHub, ECR** |
| **Deploy** | **ArgoCD** | **Flux, Kubernetes, Docker** |

#### 💻 기업용 서버 vs 스팀덱 스펙
| 항목 | 일반 기업용 서버 (최소) | Steam Deck (본 환경) |
| :--- | :--- | :--- |
| **CPU** | Multiple Xeon / EPYC 코어 | **AMD Zen 2 (4Core/8Thread)** |
| **RAM** | 8GB ~ 128GB+ | **16GB LPDDR5 (Shared)** |
| **OS** | RedHat / AM2 / Ubuntu | **SteamOS (Arch Linux)** |
| **Storage** | NVMe RAID / SAN | **Internal NVMe + SD Card** |

---

