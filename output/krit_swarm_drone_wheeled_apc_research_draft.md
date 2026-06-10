# 군집드론 탑재 차륜형장갑차 개발사업 소요기획서 기초자료 초안

작성 기준일: 2026년 6월 10일

본 문서는 군집드론 탑재 차륜형장갑차 개발사업의 국방기술진흥연구소 소요기획서 작성에 활용하기 위한 기초자료 초안이다. 모든 내용은 공개자료를 기반으로 작성하였으며, 확인되지 않은 세부 성능과 사업비는 “추정”으로 구분하였다. 실제 소요기획서 반영 시에는 국방부, 방위사업청, 육군, 국방기술진흥연구소, 국방기술품질원, 업체 제공 자료를 통해 최종 수치를 재확인해야 한다.

## 1. 해외 시장 분석

### 1.1 드론 전장화 추세

러시아-우크라이나 전쟁은 드론이 정찰 보조수단을 넘어 전술 단위의 핵심 전투수단으로 전환되고 있음을 보여준다. 소형 상용 드론, FPV 드론, 자폭형 드론, 장거리 일회용 드론이 동시에 운용되면서 전장의 감시, 표적 획득, 타격, 전자전, 심리전 기능이 저비용·고빈도 방식으로 수행되고 있다. 특히 FPV 드론은 기존 정밀유도무기보다 단가가 낮고, 병사 단위에서 비교적 빠르게 운용할 수 있어 보병, 포병, 기갑, 군수차량, 참호, 방공장비를 모두 위협하는 수단으로 확대되었다. 출처: NATO Review, RAND, CSIS, RUSI, Defense News 공개 분석자료.

러시아와 우크라이나 양측은 드론을 대량 소모품으로 운용하고 있다. 우크라이나 정부와 국방 관련 공개 발표에서는 연간 100만 대 이상 수준의 FPV 드론 확보와 생산 확대 목표가 반복적으로 언급되었고, 러시아 역시 Lancet 계열 자폭드론, Shahed 계열 장거리 공격드론, Molniya 계열 저가 고정익 드론을 대량 운용하는 방향으로 전환하고 있다. 이 흐름은 드론이 더 이상 특수부대나 항공부대만의 장비가 아니라, 지상군 전투단의 기본 화력·정찰 자산으로 자리 잡고 있음을 의미한다. 출처: Defense News, Army Recognition, CSIS, RUSI.

자폭드론은 전통적인 포병·미사일 화력과 다른 운용가치를 제공한다. 드론이 표적 상공에서 대기하다가 기회를 포착해 공격하는 방식은 “표적 탐색-식별-타격” 시간을 줄이고, 적 장비의 이동과 엄폐를 제한한다. 이스라엘 IAI의 Harop, AeroVironment의 Switchblade 계열, 러시아 Lancet 계열은 이러한 배회형 탄약의 대표 사례이다. Harop은 지상 발사 캐니스터 기반의 배회형 탄약으로 알려져 있으며, Switchblade 600은 대전차급 표적을 염두에 둔 휴대·차량 운용형 배회형 탄약으로 공개되어 있다. 출처: IAI Harop 공식자료, AeroVironment Switchblade 공식자료.

군집드론 기술은 단순히 여러 대의 드론을 동시에 띄우는 수준을 넘어, 서로 임무를 분담하고 재계획하며 일부 드론 손실에도 임무를 계속 수행하는 방향으로 발전하고 있다. 미국 DARPA OFFSET 프로그램은 도시지역에서 수십~수백 대 규모의 소형 무인체계를 운용하기 위한 전술·인터페이스·자율협동 기술을 실험한 대표 프로그램이다. 이 프로그램의 핵심은 군집 수량 자체보다, 지휘관이 다수 무인체계를 복잡한 조작 없이 전술 목적에 맞게 운용할 수 있는 통제방식에 있다. 출처: DARPA OFFSET 프로그램 공개자료.

AI 기반 자율협동은 군집드론 전력화의 핵심 조건이다. 사람이 드론 1대씩 조종하는 방식은 대량 운용에서 한계가 있으므로, 차량 내부 임무컴퓨터가 표적지역, 비행금지구역, 우선순위, 통신상태, 잔여 배터리, 위협정보를 종합해 드론 임무를 관리해야 한다. 여기서 AI는 “사람을 대체해 임의로 공격을 결정하는 기술”이 아니라, 다수 드론의 경로·역할·상태를 정리해 지휘관의 판단을 빠르게 돕는 임무관리 기술로 이해해야 한다.

유무인복합체계, 즉 사람이 탑승한 차량·항공기·지휘소와 무인기·무인지상차량이 함께 임무를 수행하는 MUM-T도 확대되고 있다. 미 공군의 CCA 프로그램은 유인 전투기와 협동하는 무인 전투항공기를 목표로 하고 있으며, 지상군 분야에서도 장갑차와 소형 드론, 무인지상차량, 배회형 탄약을 결합하는 개념이 확산되고 있다. 이는 군집드론 탑재 차륜형장갑차가 단일 장비가 아니라, 지상군 네트워크의 전방 무인전력 허브로 개발되어야 함을 시사한다. 출처: U.S. Air Force CCA 공개자료, NATO DIANA, RAND.

### 1.2 국가별 사례

미국은 저가·대량·자율 무인체계를 신속히 전력화하는 방향으로 움직이고 있다. 미 국방부 Replicator Initiative는 인도태평양과 대규모 분쟁 환경을 염두에 두고, 단기간 내 다수의 소모성·자율 무인체계를 배치하려는 정책이다. 이 사업은 개별 고가 플랫폼보다 많은 수량의 무인체계를 빠르게 배치하는 데 초점이 있으며, 군집드론 탑재 전투차량 개념과도 직접적으로 연결된다. 출처: U.S. Department of Defense Replicator 공개발표 및 보도자료.

Anduril은 Lattice 기반 임무통제, Altius 계열 발사형 드론, Roadrunner 대드론 체계, Barracuda 자율항공체 등으로 무인체계와 AI 기반 전장관리 역량을 확대하고 있다. AeroVironment는 Switchblade 계열 배회형 탄약과 Puma 계열 소형 UAS를 통해 휴대·차량·전술부대 운용형 무인체계 시장에서 강점을 보유하고 있다. DARPA OFFSET은 군집운용을, 미 공군 CCA는 유인-무인 협동전투를 대표하는 프로그램이다. 출처: Anduril 공식자료, AeroVironment 공식자료, DARPA OFFSET, U.S. Air Force CCA.

중국은 CH 시리즈, Wing Loong 계열, ASN 계열 등 다양한 무인항공체계를 보유하고 있으며, 군집드론 시범과 대량 운용 개념을 지속적으로 공개해 왔다. 특히 중국은 드론 기체 생산기반, 배터리, 통신장비, 상용 드론 생태계가 강해 대량 생산과 수출경쟁력 측면에서 높은 잠재력을 가진다. 중국의 드론전력은 단일 고성능 무인기뿐 아니라 소형 드론의 대량 투입, 전자전·정찰·타격 결합 운용까지 확대될 가능성이 크다. 출처: RAND, CSIS, Army Recognition, Jane's 공개자료.

러시아는 Lancet 배회형 탄약을 전장에서 대량 운용하며 장갑차, 포병, 방공자산을 공격하는 사례를 축적했다. 최근에는 Molniya 계열 저가 고정익 드론과 FPV 드론을 결합해 대량 소모형 전술을 강화하고 있으며, 일부 공개 보도에서는 드론을 다른 드론이나 차량에서 운용하는 모함 개념도 나타난다. 러시아 사례의 핵심은 고성능 단일 플랫폼보다, 저가·대량·소모·전자전 대응을 결합한 전술 생태계라는 점이다. 출처: Army Recognition, Defense News, RUSI, CSIS.

이스라엘은 배회형 탄약과 전술 UAS 분야에서 가장 오래된 운용경험을 보유한 국가 중 하나이다. IAI의 Harop·Harpy 계열은 방공망 제압과 표적탐색·타격을 위한 배회형 탄약으로 알려져 있고, Elbit의 SkyStriker는 전술부대가 운용 가능한 전기추진 배회형 탄약으로 공개되어 있다. 이스라엘 사례는 차량 탑재 발사, 전술 지휘통제, 정찰-타격 통합 면에서 참고 가치가 크다. 출처: IAI 공식자료, Elbit Systems 공식자료.

유럽은 NATO 중심의 혁신 프로그램과 각국 지상군 현대화 사업을 통해 드론·대드론·MUM-T를 확대하고 있다. NATO DIANA는 신흥기술 기업과 국방 수요를 연결하는 혁신 네트워크이며, 영국·독일·프랑스는 장갑차 기반 임무모듈, 무인지상차량, 전술 UAS, 대드론 방어체계를 결합하는 방향으로 전력화를 추진하고 있다. Boxer Mission Module, RCH155, Mission Master UGV는 유럽식 모듈화·개방형 아키텍처·유무인복합 운용의 참고사례로 볼 수 있다. 출처: NATO DIANA, ARTEC Boxer, KNDS RCH155, Rheinmetall Mission Master.

### 1.3 진입 추진 국가 선정

아래 표는 군집드론 탑재 차륜형장갑차 또는 차량형 드론운용 플랫폼의 해외 진입 가능성을 공개자료 기반으로 예비 분석한 것이다. 실제 수출 추진 시에는 방산수출통제, 현지 군 요구성능, 기존 보유차량, 예산주기, 정치·외교 환경을 별도로 검토해야 한다.

| 국가 | 운용현황 | 위협수준 | 도입가능성 | 시장성 | 비고 |
|---|---|---:|---:|---:|---|
| 폴란드 | 우크라이나 전쟁 인접국으로 드론·대드론·기갑전력 확충 중 | 매우 높음 | 높음 | 높음 | 러시아 위협 대응, 한국 방산 협력 기반 존재 |
| 루마니아 | 흑해·우크라이나 인접, NATO 동부전선 강화 중 | 높음 | 중간~높음 | 중간 | 차륜형 플랫폼과 감시정찰 수요 예상 |
| 에스토니아·라트비아·리투아니아 | 발트 3국, 소형 드론·대드론·분산방어 관심 높음 | 매우 높음 | 중간 | 중간 | 경량·모듈형 패키지 수요 적합 |
| 핀란드 | 러시아 접경, NATO 가입 이후 지상전 대비 강화 | 높음 | 중간 | 중간 | 혹한 운용·분산전 개념 중요 |
| 노르웨이 | 북극권·해안 방어, NATO 네트워크 중심전 강화 | 중간~높음 | 중간 | 중간 | 고가·고신뢰 장비 선호 |
| 호주 | 인도태평양 장거리 감시정찰·무인체계 관심 | 중간 | 중간 | 중간~높음 | 한국 장갑차 협력 경험 활용 가능 |
| 사우디아라비아 | 드론·미사일 위협 경험, 대드론·무인체계 투자 확대 | 높음 | 중간 | 높음 | 고가 체계 도입 여력, 현지화 요구 가능 |
| UAE | 무인체계·AI 국방산업 투자 활발 | 중간~높음 | 중간 | 높음 | 현지 방산기업 협력 모델 필요 |
| 인도 | 국경분쟁, 고산지·사막지형, 드론 운용 확대 | 높음 | 중간 | 높음 | 현지 생산·기술이전 요구 가능 |
| 필리핀 | 해양·도서 감시, 반군·회색지대 대응 수요 | 중간 | 중간 | 중간 | 경량형 드론모함·감시정찰형 적합 |

## 2. 해외 경쟁 무기체계 분석

### 2.1 Stryker 기반 드론 플랫폼

Stryker 기반 드론 플랫폼은 완성된 단일 양산체계라기보다, 미 육군과 업체가 Stryker 차륜형장갑차의 내부공간·전력·전자구조를 활용해 무인체계 운용성을 확대하는 실증·개념 플랫폼으로 보는 것이 적절하다. Stryker 계열은 8×8 차륜형 장갑차로 병력수송, 지휘, 정찰, 화력지원 등 다양한 파생형이 존재하며, StrykerX와 같은 개념차량은 하이브리드 전원, 개방형 전자구조, 무인체계 운용, 능동방호, 드론 발사 기능을 결합하는 방향을 제시했다. 출처: General Dynamics Land Systems 공개자료, Army Recognition, The Defense Post.

공개자료 기준으로 Stryker 일반형은 2명 승무원과 약 9명 탑승병력 규모의 병력수송형 구조를 가진다. 드론 플랫폼으로 전환할 경우 병력 탑승공간 일부를 임무통제석, 드론 보관랙, 발사장치, 배터리 충전·관리장비, 데이터링크 장비로 전환하는 방식이 예상된다. 드론 탑재수량, 발사방식, 회수방식은 공개 제원이 확정되지 않았으므로 “체계개념 기준 추정”으로 처리해야 한다.

| 항목 | 공개 확인 내용 및 추정 |
|---|---|
| 차량 제원 | 8×8 차륜형 장갑차 기반, 파생형 다수, 내부 병력공간 보유 |
| 운용인원 | 기본 Stryker는 승무원 2명+탑승병력 약 9명 수준으로 알려짐. 드론형은 조종수·차장·드론운용병 2~3명 구성이 합리적 |
| 드론 탑재수량 | 공개 확정자료 없음. 소형 정찰드론 기준 12~24대, 튜브형 발사 드론 기준 8~16대 수준의 개념설계 가능 |
| 발사방식 | 후방 또는 상부 자동발사대, 튜브형 발사, 캐니스터 발사, 수직 이륙형 드론 이륙대 혼합 가능 |
| 회수방식 | 소형 멀티콥터는 차량 주변 자동착륙·수동회수, 고정익·배회형 탄약은 회수 없음 또는 지정구역 회수 |
| 임무개념 | 전방 ISR, 표적획득, 통신중계, 제한적 타격, 유무인복합작전 지휘 |

### 2.2 Leonidas

Leonidas는 Epirus가 개발한 고출력 마이크로파 기반 대드론 체계로, 다수 드론 또는 군집드론의 전자장비를 동시에 무력화하는 개념을 제시한다. 미 육군은 IFPC-HPM, 즉 고출력 마이크로파 기반 간접화력방어 역량과 관련해 Epirus와 계약을 체결한 바 있으며, Leonidas는 군집드론 대응 분야에서 대표적인 경쟁·보완 체계로 볼 수 있다. 출처: Epirus 공식자료, U.S. Army 및 공개 계약 보도자료.

Leonidas는 드론을 직접 운반·발사하는 드론모함은 아니지만, 군집드론 전장이 확대될수록 군집드론 운용차량은 동시에 대드론 방호수단과 통합되어야 함을 보여준다. 따라서 차륜형장갑차 기반 군집드론 모함차량도 자체 방호수단, 연동형 전자전 장비, 기동부대 방공망과의 데이터 연계를 초기 설계요구에 포함할 필요가 있다.

### 2.3 PIRANHA 10×10

PIRANHA 10×10 또는 PIRANHA Heavy Mission Carrier 계열은 대형 차륜형 장갑차의 넓은 내부공간과 후방 임무공간을 활용하는 사례로 볼 수 있다. 공개자료상 PIRANHA 계열은 병력수송, 지휘, 화력지원, 전문 임무모듈 탑재 등 다양한 확장성을 강조한다. 군집드론 모함 관점에서는 10×10 플랫폼의 높은 적재중량, 넓은 후방공간, 임무모듈 교체 가능성이 핵심 참고점이다. 출처: General Dynamics European Land Systems 공개자료, Army Recognition.

### 2.4 RCH155

RCH155는 Boxer 차륜형 장갑차 섀시에 원격조종 포탑형 155mm 자주포 모듈을 결합한 체계이다. 본 사업과 직접 같은 드론체계는 아니지만, 승무원 공간과 임무공간을 분리하고, 무인화된 임무모듈을 차량 상부 또는 후방에 통합하며, 디지털 사격통제와 차량 플랫폼을 결합한 사례라는 점에서 중요하다. RCH155는 장갑차 기반 임무모듈이 대구경 무장, 자동화, 원격운용까지 확장될 수 있음을 보여준다. 출처: KNDS RCH155 공개자료.

### 2.5 Boxer Mission Module

Boxer는 구동모듈과 임무모듈을 분리하는 구조가 특징이다. 같은 구동 플랫폼에 병력수송, 지휘, 의무, 정찰, 화력지원 등 다른 임무모듈을 결합할 수 있으며, 이는 드론운용차량 개발에 매우 중요한 참고사례이다. 군집드론 모함차량도 초기부터 “차량 플랫폼”과 “드론 임무모듈”을 가능한 한 분리해 설계하면, 드론 종류와 통제장비 변화에 따라 후속 개량이 쉬워진다. 출처: ARTEC Boxer 공식자료, Rheinmetall 공개자료.

### 2.6 Patria 6×6

Patria 6×6은 병력수송과 다양한 임무 개조를 고려한 6×6 장갑차이다. 고가 8×8 플랫폼보다 낮은 비용과 높은 기동성을 강조하며, 여러 국가가 공동조달 또는 현지생산 방식으로 도입하고 있다. 군집드론 모함차량 관점에서는 소형·중형 패키지, 국경감시, 경보병·해병대·영토방위군용 드론운용차량으로 참고할 수 있다. 출처: Patria 6×6 공식자료.

### 2.7 VBTP Guarani

VBTP Guarani는 브라질의 6×6 차륜형 장갑차로, 병력수송과 다양한 파생형 개발을 목표로 한다. 중저가 차륜형 플랫폼을 기반으로 통신, 지휘, 정찰, 무장 모듈을 조합하는 수출형 접근이 가능하다는 점에서 참고 가치가 있다. 군집드론 모함차량도 중형 차륜형장갑차형뿐 아니라 6x6급 또는 6×6급 소형 파생형까지 장기적으로 검토할 수 있다. 출처: Iveco Defence Vehicles 및 공개 제원자료.

### 2.8 JLTV 드론모함 개념

JLTV 기반 드론모함 개념은 경전술차량에 소형 UAS, 배회형 탄약, 발사튜브, 통신중계장비를 결합해 신속기동부대가 드론을 운용하는 방향이다. 장갑차급 방호력과 내부공간은 제한되지만, 신속전개, 공수·해상수송, 특수작전, 소규모 정찰·타격 임무에 적합하다. 차륜형장갑차 기반 체계와 비교하면 JLTV형은 저비용·고기동 패키지, 중형 차륜형장갑차형은 전방 장갑기동부대와 함께 움직이는 중형 드론 허브로 구분된다. 출처: Oshkosh JLTV 공개자료, Army Recognition, Defense News.

### 2.9 Mission Master UGV

Rheinmetall Mission Master는 무인지상차량 기반 임무플랫폼으로, 정찰, 수송, 화력지원, 대드론, 무인기 운용 등 다양한 임무킷을 적용할 수 있는 것으로 공개되어 있다. 이 체계는 “드론을 차량이 직접 싣고 다니는 방식”뿐 아니라, 모함장갑차가 UGV와 함께 드론을 전개·회수·중계하는 복합 운용으로 발전할 수 있음을 보여준다. 출처: Rheinmetall Mission Master 공식자료.

### 2.10 해외 경쟁체계 공통 특징

| 공통 특징 | 내용 | 차륜형장갑차 기반 개발 시 반영 방향 |
|---|---|---|
| 승무원 공간 최소화 | 운전·지휘·임무통제에 필요한 인원만 유지 | 조종수, 차장, 드론운용병 2명 중심 구성 |
| 후방 임무공간 확대 | 병력 탑승공간을 임무장비·드론 저장공간으로 전환 | 후방 드론랙, 자동발사대, 충전장치 배치 |
| 모듈화 설계 | 임무장비를 차량과 분리 가능한 모듈로 설계 | 정찰형, 공격형, 통신중계형, 대드론형 모듈화 |
| 개방형 전자구조 | 통신·센서·무장·드론을 표준 인터페이스로 연결 | 국산 데이터링크, BMS, AI 서버 연동 구조 채택 |
| 다수 드론 적재 | 단일 고가 드론보다 다수 소형 드론을 전방 운용 | 기본형 12~24대, 확장형 24~48대 개념 검토 |
| 자동 발사 | 수동 조립·이륙 시간을 줄이고 생존성 확보 | 후방 자동발사기, 상부 캐니스터, 수직이륙 패드 검토 |
| AI 기반 임무통제 | 사람의 조작부담을 줄이고 다수 드론 상태를 관리 | 임무계획, 경로관리, 충전관리, 통신상태 표시 기능 |

## 3. 개조개발 필요성

### 3.1 현재 문제점

첫째, 국내 지상군에는 군집드론 전용 플랫폼이 부족하다. 현재 드론은 부대별 정찰·감시 목적의 단품 장비로 운용되는 경향이 강하며, 장갑기동부대와 함께 전방에서 다수 드론을 저장·충전·발사·통제하는 전용 장갑차 개념은 아직 충분히 체계화되지 않았다. 우크라이나 전쟁 사례를 보면 드론은 대량으로 소모되고, 적 전자전과 포병 위협 아래에서 빠르게 재발진해야 하므로, 단순 휴대형 운용만으로는 지속적인 전장 감시와 타격을 보장하기 어렵다.

둘째, 대량 드론 수송능력이 부족하다. 군집드론은 드론 1~2대가 아니라 다수의 드론, 배터리, 예비부품, 안테나, 통제장비, 정비공구, 영상처리장비가 함께 있어야 전력으로 작동한다. 일반 차량이나 병력수송 차량에 임시 적재하는 방식은 공간, 전원, 통신, 안전관리 측면에서 한계가 있다.

셋째, 전방 운용에 제한이 있다. 드론 운용팀이 비장갑 차량이나 야외 임시진지에서 드론을 운용하면 포병, 박격포, FPV 드론, 소화기, 파편에 취약하다. 장갑차 기반 플랫폼은 전방 기동부대와 같은 속도로 이동하면서 운용팀을 보호하고, 신속히 진지전환을 할 수 있다.

넷째, 통제장비가 부족하다. 군집드론은 단순 조종기가 아니라 임무계획, 영상통합, 표적좌표 전송, 데이터링크, 전자전 탐지, 배터리 관리, 비행승인·안전통제 기능이 결합되어야 한다. 이를 위해 차량 내부에 임무컴퓨터, AI 임무관리 서버, 통신장비, 전원관리장치, 보안장비를 체계적으로 통합할 필요가 있다.

### 3.2 차륜형장갑차 기반 개조개발 개념

본 사업은 기존 차륜형장갑차 기반으로 군집드론 운용에 필요한 임무공간과 전자장비를 통합하는 개조개발 사업으로 추진하는 것이 타당하다. 차륜형장갑차는 8×8 차륜형 장갑차로 보병부대의 기동·방호·수송을 위해 개발되었고, 후방 병력 탑승공간을 보유하고 있다. 이 공간을 드론 운용 임무공간으로 전환하면 신규 차체 개발보다 개발기간과 위험을 줄일 수 있다. 출처: 방위사업청 차륜형장갑차 공개자료, 국내외 공개 제원자료.

차량 전방에는 조종수와 차장을 배치한다. 조종수는 차량 기동과 안전을 담당하고, 차장은 전술상황 판단, 상급부대 연동, 발사승인, 임무우선순위 결정을 담당한다. 전방 승무원 공간은 기존 차륜형장갑차 운용개념을 최대한 유지해 개조 위험을 낮춘다.

차량 중앙에는 드론 운용병을 배치한다. 드론 운용병은 2명 구성을 기본으로 하되, 임무규모에 따라 3명까지 확장할 수 있다. 이들은 다수 드론의 임무계획, 영상 확인, 비행상태 감시, 회수·재발진 준비, 긴급중지, 상급 지휘체계 보고를 수행한다. 조작화면은 드론별 세부 조종보다 임무상태 중심으로 구성해야 한다.

차량 후방은 드론 저장고, 자동 발사기, 충전 시스템, 데이터링크 장비, AI 임무관리 서버를 배치하는 공간으로 전환한다. 드론 저장고는 충격·진동·화재 안전을 고려한 랙 구조로 설계하고, 배터리 충전 시스템은 화재격리와 배기 기능을 포함해야 한다. 자동 발사기는 후방 도어 개방형, 상부 캐니스터형, 수직이륙 패드형을 임무별로 조합할 수 있다.

AI 임무관리 서버는 다수 드론 상태를 한 화면에서 통합 관리하는 역할을 수행한다. 이 서버는 드론의 위치, 잔여 배터리, 통신품질, 임무상태, 위험구역, 회수 가능성을 표시하고, 차장과 운용병이 빠르게 판단할 수 있도록 추천안을 제시한다. 단, 무장 사용과 표적공격은 반드시 인간 지휘관의 승인 절차를 포함하는 방향으로 요구성능을 설정해야 한다.

### 3.3 기대효과

첫째, 전방 ISR 범위가 확대된다. ISR은 감시·정찰·정보수집을 뜻하며, 지상부대가 보이지 않는 지역의 적 이동, 포병진지, 방공장비, 장애물, 매복 가능성을 빠르게 확인하는 기능이다. 군집드론 모함차량은 장갑기동부대 전방 또는 측방에서 다수 드론을 순차 발진시켜 감시 공백을 줄일 수 있다.

둘째, 공격범위가 증가한다. 배회형 탄약 또는 소형 타격드론과 연동할 경우, 장갑차 자체 무장의 사거리 밖 표적에 대해 정찰-표적획득-타격을 한 흐름으로 수행할 수 있다. 이는 기존 장갑차가 직접 접근해야 했던 위험을 줄이고, 적 포병·대전차팀·보급차량을 더 먼 거리에서 억제하는 효과를 제공한다.

셋째, 생존성이 향상된다. 드론 운용팀이 장갑차 내부에서 임무를 수행하면 포격 파편, 소화기, 드론 공격에 대한 방호수준이 높아진다. 또한 차량이 이동하면서 발사와 회수를 반복할 수 있어, 고정 운용지점이 적에게 탐지되어 타격받는 위험을 줄인다.

넷째, 유무인복합작전 수행능력이 강화된다. 차륜형장갑차 기반 모함차량은 보병전투차, 전차, 포병, 무인지상차량, 전술드론을 연결하는 전방 임무허브가 될 수 있다. 차량은 드론을 싣고 다니는 수송수단이 아니라, 유인 장갑차와 무인체계를 연결하는 통제·중계·임무관리 플랫폼이 된다.

다섯째, 네트워크 중심전 구현에 기여한다. 군집드론이 수집한 영상과 좌표가 전술지휘체계, 포병사격체계, 대드론체계, 전자전장비와 연동되면 부대 전체의 판단속도와 타격정확도가 향상된다. 이는 단일 장비 성능보다 네트워크 효과가 중요한 미래 지상전 방향과 부합한다.

### 3.4 개조개발 필요성 논리

현재 전장은 드론 중심으로 빠르게 변화하고 있다. 러시아-우크라이나 전쟁은 소형 드론과 FPV 드론이 장갑차, 보병, 포병, 방공장비를 상시 위협할 수 있음을 보여주었다. 앞으로 지상전에서는 드론을 먼저 보고, 먼저 띄우고, 먼저 연결하는 부대가 전술적 우위를 갖게 된다.

군집드론 확대는 기존 장갑차 운용방식의 한계를 드러낸다. 기존 차륜형장갑차는 병력수송과 방호에 최적화되어 있으나, 다수 드론을 안전하게 저장하고, 충전하고, 자동 발사하고, 임무를 통제하는 장비는 갖추지 못했다. 임시 적재 방식은 전원, 통신, 안전, 정비, 작전지속성 측면에서 한계가 분명하다.

따라서 전용 플랫폼이 필요하다. 군집드론 탑재 차륜형장갑차는 장갑기동부대와 같은 속도로 움직이면서 다수 드론을 전방에서 운용하는 장비이다. 이 플랫폼은 단순 드론 운반차량이 아니라, 드론 저장·충전·발사·통제·데이터연동 기능을 통합한 전방 무인전력 허브가 되어야 한다.

국내 개발이 필요한 이유도 분명하다. 국내 지상군은 기존 차륜형장갑차를 이미 운용하고 있으며, 국내에는 장갑차, 드론, 데이터링크, AI 소프트웨어, 전술통신, 체계통합 역량이 존재한다. 해외 완제품 도입보다 국내 차량 기반 개조개발을 추진하면 국내 지상군 전술체계와 보안요구에 맞춘 통합이 가능하고, 향후 수출형 파생모델 개발도 가능하다.

## 4. 예상 사업비

### 4.1 추정 전제

본 사업비는 공개 유사사업과 방산 연구개발 일반비용 구조를 참고한 기획단계 추정치이다. 실제 사업비는 요구성능, 시제차량 수량, 드론 포함 여부, 탄약형 드론 포함 여부, 군 운용시험 범위, 보안통신장비 수준, 기존 차륜형장갑차 차체 활용 여부에 따라 크게 달라진다. 따라서 아래 수치는 “소요기획서 초안용 범위 추정”으로 사용하고, 예비타당성 또는 선행연구 단계에서 비용분석 전문기관 검증을 받아야 한다.

추정 기준은 다음과 같다. 소형 시나리오는 차륜형장갑차 1~2대 개조와 소형 정찰드론 중심 실증이다. 중형 시나리오는 차륜형장갑차 3~4대 시제, 정찰드론·통신중계드론·제한적 배회형 드론 통합, 군 운용시험을 포함한다. 대형 시나리오는 차륜형장갑차 5~6대 이상 시제, 자동발사기, AI 임무관리, 다종 드론, 전술지휘체계 연동, 확대 시험평가를 포함한다.

### 4.2 항목별 추정

| 항목 | 소형 추정 | 중형 추정 | 대형 추정 | 산정 근거 |
|---|---:|---:|---:|---|
| 체계설계 | 20억 원 | 40억 원 | 70억 원 | 요구분석, 기본설계, 상세설계, 안전성 분석 |
| 임무컴퓨터 | 15억 원 | 35억 원 | 60억 원 | 차량 내부 통제콘솔, 서버, 영상처리장비 |
| AI 소프트웨어 | 20억 원 | 60억 원 | 120억 원 | 임무계획, 다중드론 상태관리, 운용자 화면, 시험데이터 학습 |
| 데이터링크 | 20억 원 | 50억 원 | 100억 원 | 전술통신, 안테나, 보안모듈, 중계기능 |
| 드론발사기 | 25억 원 | 70억 원 | 140억 원 | 자동발사대, 캐니스터, 안전장치, 후방 개방구조 |
| 차량개조 | 30억 원 | 80억 원 | 150억 원 | 차륜형장갑차 내부공간 개조, 전원, 냉각, 방호, 배선 |
| 시제제작 | 60억 원 | 180억 원 | 350억 원 | 시제차량, 임무모듈, 통합장비, 예비품 |
| 시험평가 | 30억 원 | 80억 원 | 160억 원 | 성능시험, 환경시험, 전자파, 주행, 발사 안정성 |
| 군 운용시험 | 20억 원 | 60억 원 | 120억 원 | 부대 운용시험, 교육, 정비, 데이터 수집 |
| 합계 | 240억 원 | 655억 원 | 1,270억 원 | 기획단계 범위 추정 |

### 4.3 계산과정

소형 시나리오는 “핵심 기능 실증”을 목표로 한다. 차륜형장갑차 기반 차량 1~2대를 개조하고, 소형 정찰드론과 임무통제장비를 통합하는 수준이다. 자동발사기는 단순형으로 구성하고, AI 기능은 완전 자율이 아니라 다수 드론 상태표시와 임무추천 중심으로 제한한다. 이 경우 총사업비는 약 240억 원 수준으로 추정된다.

중형 시나리오는 “군 운용시험 가능한 시제체계”를 목표로 한다. 차륜형장갑차 3~4대급 시제차량을 제작하고, 드론 저장고, 자동발사기, 충전장치, 데이터링크, AI 임무관리 서버, 전술지휘체계 연동을 포함한다. 정찰드론, 통신중계드론, 제한적 배회형 드론을 함께 검토하면 통합과 시험비가 증가한다. 이 경우 총사업비는 약 655억 원 수준으로 추정된다.

대형 시나리오는 “체계개발 및 양산 전 단계 수준”을 목표로 한다. 차륜형장갑차 5~6대 이상 시제, 다종 드론 통합, 고도화된 자동발사기, 차량 생존성 개량, 전술망 연동, 부대급 운용시험, 정비·교육체계 구축을 포함한다. 이 경우 총사업비는 약 1,270억 원 수준으로 추정된다.

본 사업의 적정 기획안은 중형 시나리오를 기준으로 삼는 것이 타당하다. 소형은 실증에는 적합하지만 소요기획서 수준의 군 운용성을 충분히 보여주기 어렵고, 대형은 초기 소요기획 단계에서 예산 부담이 크다. 따라서 1단계는 중형 규모의 시제개발로 추진하고, 2단계에서 양산형 임무모듈과 드론 종류를 확대하는 단계적 접근이 적절하다.

## 5. 과제카드 이미지 기획안

다음 이미지는 국기연 과제카드 또는 소요기획서 설명자료에 사용할 수 있는 생성형 AI 이미지 콘셉트이다. 모든 이미지는 실제 기밀 장비나 실존 부대 표식을 재현하지 않고, 공개 가능한 일반 개념 이미지로 제작해야 한다. 이미지 안에는 제목, 수치, 긴 설명문을 넣지 않고, 문구는 HWP 또는 PPT에서 별도 텍스트로 배치한다.

### 5.1 차륜형장갑차 기반 군집드론 모함차량

이미지 목적: 사업의 핵심 장비를 한눈에 보여주는 대표 이미지이다. 8×8급 일반 차륜형 장갑차가 전방 기동부대와 함께 이동하며 상부·후방에 드론 운용 모듈을 탑재한 모습을 표현한다.

생성 프롬프트:

16:9 realistic defense proposal concept image, generic olive drab 8x8 wheeled armored vehicle, not an exact replica of any real platform, modular rear drone mission bay, clean modern military engineering visualization, matte olive drab and dark gray, no real unit markings, no national flags, no readable text, non-classified concept vehicle, several small reconnaissance drones staged near the vehicle, realistic lighting, professional government defense proposal style, high detail, safe generic concept

### 5.2 후방 드론 컨테이너 개방 장면

이미지 목적: 차량 후방 임무공간의 필요성을 보여준다. 후방 도어 또는 컨테이너가 열리고 내부에 드론랙, 배터리 충전함, 발사튜브, 임무장비가 정돈되어 있는 장면을 표현한다.

생성 프롬프트:

16:9 realistic military vehicle rear mission bay concept, generic Korean-style wheeled armored vehicle rear door open, modular drone storage racks, battery charging cabinets, secure data-link equipment, compact launch tubes, two soldiers inspecting equipment, no readable labels, no classified details, clean organized interior, professional defense acquisition proposal visualization, realistic materials, olive drab vehicle, gray equipment modules, safe non-sensitive concept design

### 5.3 군집드론 동시 발사 장면

이미지 목적: 자동발사와 다수 드론 운용 효과를 보여준다. 차량 후방 또는 상부에서 소형 드론 여러 대가 순차적으로 이륙하는 장면을 표현한다.

생성 프롬프트:

16:9 realistic battlefield concept image, generic 8x8 armored drone carrier launching multiple small reconnaissance drones simultaneously, drones taking off in coordinated formation, vehicle positioned behind cover, dust and daylight, generic olive drab military vehicle style with no exact real markings, no explosions, no gore, no readable text, emphasis on launch automation and networked ISR, professional military technology proposal style, realistic but non-classified

### 5.4 전장 네트워크 구성도

이미지 목적: 드론모함차량이 전차, 보병, 포병, 지휘소, 무인지상차량과 정보를 공유하는 네트워크 중심전 개념을 설명한다. 이 이미지는 사진풍보다 정보그래픽 배경 이미지로 활용한다.

생성 프롬프트:

16:9 clean defense network concept diagram background, generic armored drone carrier connected to small drones, command post, artillery unit, infantry vehicle, unmanned ground vehicle, satellite or radio relay icons, thin green network lines on light gray and white background, no readable text, no official logos, modern Korean defense proposal infographic style, editable text will be added separately, minimal and professional

### 5.5 유무인복합작전 개념도

이미지 목적: 유인 장갑차와 무인 드론·UGV가 함께 작전하는 미래 지상전 개념을 보여준다.

생성 프롬프트:

16:9 realistic manned-unmanned teaming battlefield concept, Korean-style armored vehicles operating with small aerial drones and unmanned ground vehicles, command vehicle coordinating ISR and target information, mountainous Korean terrain, realistic daylight, no exact real equipment replication, no readable text, no flags, no insignia, professional defense concept art, balanced composition, safe non-classified technology visualization

## 6. 참고문헌

1. U.S. Department of Defense, Replicator Initiative public announcements and releases, https://www.defense.gov/
2. DARPA, OFFensive Swarm-Enabled Tactics (OFFSET), https://www.darpa.mil/program/offensive-swarm-enabled-tactics
3. U.S. Air Force, Collaborative Combat Aircraft program public releases, https://www.af.mil/
4. NATO DIANA, Defence Innovation Accelerator for the North Atlantic, https://www.diana.nato.int/
5. RAND Corporation, reports and commentaries on unmanned systems and Russia-Ukraine war lessons, https://www.rand.org/
6. CSIS, analysis on drone warfare and unmanned systems, https://www.csis.org/
7. RUSI, analysis on Ukraine war drones, electronic warfare, and attritable systems, https://rusi.org/
8. Defense News, public reporting on Replicator, drones, and Ukraine drone warfare, https://www.defensenews.com/
9. Army Recognition, public vehicle and unmanned systems reporting, https://www.armyrecognition.com/
10. AeroVironment, Switchblade loitering missile systems, https://www.avinc.com/
11. Anduril Industries, autonomous systems and mission command products, https://www.anduril.com/
12. IAI, Harop/Harpy loitering munition product information, https://www.iai.co.il/
13. Elbit Systems, SkyStriker loitering munition product information, https://elbitsystems.com/
14. Epirus, Leonidas high-power microwave counter-electronics system, https://www.epirusinc.com/
15. General Dynamics Land Systems, Stryker family public information, https://www.gdls.com/
16. General Dynamics European Land Systems, PIRANHA vehicle family, https://www.gdels.com/
17. ARTEC, Boxer vehicle and mission module concept, https://www.artec-boxer.com/
18. KNDS, RCH155 public product information, https://www.knds.com/
19. Patria, Patria 6x6 armoured vehicle, https://www.patriagroup.com/
20. Rheinmetall, Mission Master unmanned ground vehicle, https://www.rheinmetall.com/
21. Oshkosh Defense, JLTV public product information, https://oshkoshdefense.com/
22. Hyundai Rotem, wheeled armored vehicle public information, https://www.hyundai-rotem.co.kr/
23. 방위사업청, 차륜형장갑차 및 무기체계 관련 공개자료, https://www.dapa.go.kr/
24. 국방기술품질원, 국방과학기술 및 무기체계 품질 관련 공개자료, https://www.dtaq.re.kr/
25. 국방기술진흥연구소, 국방기술기획 및 과제기획 관련 공개자료, https://www.krit.re.kr/
26. 한국국방연구원, 미래전 및 무인체계 관련 공개 연구자료, https://www.kida.re.kr/
27. 국회예산정책처, 국방예산 및 방위력개선사업 분석자료, https://www.nabo.go.kr/

## 7. PDF 원문 링크 목록

아래 목록은 소요기획서 작성 시 PDF 원문 확보를 우선 권장하는 자료이다. 일부 기관은 웹페이지에서 PDF가 수시로 이동하거나 검색형 게시판으로 제공되므로, 최종 작성 시 각 기관명과 제목으로 재검색해 최신 원문을 내려받아야 한다.

| 우선순위 | 기관 | 확보 권장 PDF | 활용 목적 |
|---:|---|---|---|
| 1 | 국방기술품질원 | 국방과학기술조사서, 글로벌 국방기술 동향, 무기체계 품질자료 | 국내 기술수준, 무기체계 분류, 기술동향 근거 |
| 2 | 국방기술진흥연구소 | 국방기술기획서, 미래도전국방기술 관련 공개자료, 과제기획 안내자료 | 국기연 과제카드 문체와 기술기획 논리 반영 |
| 3 | 방위사업청 | 차륜형장갑차 전력화, 드론봇·무인체계 관련 보도자료 PDF | 국내 사업 필요성 및 전력화 근거 |
| 4 | KIDA | 미래전, 유무인복합체계, 전장 네트워크 관련 연구보고서 | 정책·전략적 필요성 근거 |
| 5 | 국회예산정책처 | 국방예산 분석, 방위력개선사업 분석 | 사업비 추정과 예산 논리 보강 |
| 6 | NATO | DIANA, EDT, unmanned systems 관련 PDF | NATO 국가 수요와 국제 협력 근거 |
| 7 | RAND | unmanned systems, Ukraine lessons, autonomy 관련 PDF | 해외 시장·전장 변화 분석 근거 |
| 8 | CSIS | drone warfare, Ukraine, defense innovation 관련 PDF | 드론 전장화 수치·정책 근거 |
| 9 | DARPA | OFFSET 프로그램 자료 | 군집드론 기술 발전 근거 |
| 10 | 업체 공식자료 | AeroVironment, IAI, Elbit, Epirus, Rheinmetall, Patria, KNDS, ARTEC | 경쟁체계 제원·임무개념 근거 |

## 8. 소요기획서 반영용 핵심 문장

본 사업은 러시아-우크라이나 전쟁 이후 급격히 확대된 드론 전장화 추세에 대응하여, 한국군 차륜형장갑차 기반의 군집드론 운용 플랫폼을 확보하기 위한 개조개발 사업이다. 기존 차륜형장갑차는 병력수송과 방호에는 적합하나, 다수 드론의 저장, 충전, 자동발사, 임무통제, 데이터링크, AI 기반 임무관리를 통합하는 전용 구조를 갖추지 못하고 있다. 이에 기존 차륜형장갑차의 후방 병력공간을 군집드론 임무공간으로 개조하여 전방 ISR 확대, 장거리 표적획득, 유무인복합작전, 네트워크 중심전 수행능력을 확보할 필요가 있다.

해외 사례를 보면 미국 Replicator Initiative, DARPA OFFSET, Stryker 기반 무인체계 운용 개념, 이스라엘 배회형 탄약, 유럽 Boxer Mission Module 및 Mission Master UGV는 모두 저비용 다수 무인체계, 모듈형 임무공간, 개방형 전자구조, AI 기반 임무통제 방향으로 발전하고 있다. 이는 국내 지상군도 개별 드론 도입을 넘어 장갑기동부대와 함께 움직이는 전방 무인전력 허브를 확보해야 함을 시사한다.

본 사업은 신규 차체 개발보다 기존 차륜형장갑차를 활용한 개조개발 방식이 타당하다. 기존 플랫폼을 활용하면 개발기간과 기술위험을 줄일 수 있고, 국내 장갑차·드론·통신·AI·체계통합 역량을 결합해 한국군 운용환경에 맞는 전용 플랫폼을 확보할 수 있다. 특히 후방 임무공간에 드론 저장고, 자동발사기, 충전 시스템, 데이터링크 장비, AI 임무관리 서버를 통합하면, 기존 장갑차의 한계를 보완하면서 미래 지상전의 유무인복합작전 요구에 대응할 수 있다.



