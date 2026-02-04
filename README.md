### 📱 Handheld Data Center: Steam Deck Project

> **"손바닥 위에서 돌아가는 기업급 클라우드 생태계"**
<br>

본 프로젝트는 고성능 게임기(Steam Deck)에 기업용 표준 기술을 이식한 사례입니다. <br>
장소에 구애받지 않고 **개발-배포-운영**이 완결되는 독립적 인프라를 구축했습니다.

---

#### 💡 작동 시나리오
- [ ] VSCODE, GITEA - 소스 코드 수정 커밋/푸시
- [ ] GITEA-ACTION - 빌드
- [ ] KANIKO, GITEA - 패키징, 도커라이징 후 패키지 저장소에 저장
- [ ] ARGOCD - 패키지 변화 감지, 배포, 스케일링


#### 🏗️ 엔터프라이즈 기술 매핑
| 분류 | 적용 기술 | 기업용 솔루션 대응 |
| :--- | :--- | :--- |
| **KUBERNETES** | **K3s** | **Kubernetes, EKS** |
| **REPO** | **Gitea** | **GIT, SVN, GitLab, GitHub** |
| **BUILD** | **Gitea-Action** | **Jenkins, CodePipeline** |
| **PACKAGING** | **Kaniko** | **Docker, CodeBuild** |
| **CONATAINER** | **Gitea** | **DockerHub, ECR** |
| **DEPLOY** | **ArgoCD** | **Kubernetes, Docker** |

<br>

**[상세 역할 설명]**
* **Gitea:** 외부 의존성 없는 내부 코드 저장소
* **ArgoCD:** 코드 변경 시 서비스 자동 배포 및 확장
* **K3s:** 다수 서비스를 관리하는 표준 컨테이너 엔진
* **Prometheus:** 시스템 메트릭 수집 및 가용성 데이터 관리

---

#### 💻 일반 서버 vs Steam Deck 상세 스펙
*제한된 자원을 엔지니어링 최적화(K3s 튜닝 등)를 통해 극복했습니다.*

| 항목 | 일반 기업용 서버 (최소) | Steam Deck (본 환경) |
| :--- | :--- | :--- |
| **CPU** | 다중 Xeon / EPYC 코어 | **AMD Zen 2 (4코어/8쓰레드)** |
| **RAM** | 최소 32GB ~ 128GB+ | **16GB LPDDR5 (공유 메모리)** |
| **OS** | RHEL / Ubuntu Server | **SteamOS (Arch Linux 기반)** |
| **Storage** | NVMe RAID / SAN | **Internal NVMe + SD Card** |

<br>

**[최적화 포인트]**
* **리소스 절감:** 일반 K8s 대신 **K3s**를 사용하여 메모리 점유율을 70% 이상 절감.
* **환경 극복:** SteamOS의 **Read-only** 제약을 풀고 데이터 보존을 위한 스토리지 경로 재설계.

---

