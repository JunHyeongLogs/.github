# 🚀 Engineering Portfolio & Archive

> **Note**: 본 리포지토리는 지금까지 직접 설계·개발·운영한 **40여 개의 프로젝트 및 연구/논문 소스코드, 아키텍처 문서**를 백업하고 정리해둔 프라이빗 스토리지입니다.  
> 
> 기술 협업, 프로젝트 문의, 프로젝트 관련 상세 소스코드 검토나 논의가 필요하신 분은 언제든 아래 **LinkedIn**을 통해 편하게 연락주시기 바랍니다.
>
> 📩 **Contact**: [함준형 LinkedIn 프로필](https://www.linkedin.com/in/%EC%A4%80%ED%98%95-%ED%95%A8-669898284/)

---

## 🛠️ Highlights & Selected Projects

### 1. Multi-Hypervisor Automated Provisioning Platform Evolution
> **키워드**: `Hyper-V` `XenServer` `Proxmox VE` `Network Automation` `Billing` `MRTG`
> 
> 단일 가상화부터 시작하여 멀티 호스트 운영 및 고가용성(HA) 환경을 목표로 지속 개선해 온 가상화 솔루션 개발 프로젝트입니다.

* **v1. Hyper-V 기반 가상화 자동화 콘솔**
  * **주요 기능**: OS, CPU, RAM, Disk, Bandwidth, Public/Private IP 선택 후 **3분 이내 VM 자동 생성 및 배포**
  * **네트워크 & 운영**: NAT/PAT 네트워크 자동 세팅, MRTG 기반 실시간 트래픽 모니터링 및 리포트 기능
  * **비즈니스 연동**: 알람 시스템 및 자동 연장/결제 시스템 구축
* **v2. Citrix XenServer 인프라 고도화**
  * **개선 사항**: 기존 PowerShell/Windows 기반의 호스트 확장 한계 및 라이선스 비용 문제를 해결하기 위해 XenServer 엔진 도입
  * **아키텍처**: Multi-host 운영 체계 지원, 리소스 분산 및 이중화(HA) 구성으로 인프라 안정성 증대
* **v3. Proxmox VE 전환 및 솔루션 매각 (개선 진행 버전)**
  * **개선 사항**: XenServer 운용 중 발생한 원인 미상 네트워크 장애 및 확장성 한계를 극복하기 위해 Proxmox VE 기반으로 전환
  * **기능 확장**: Container(LXC) 및 VM별 L2/L4 ACL 제어 등 확장된 네트워크 제어 기능 도입
  * **매각 및 종료**: 완벽히 완성된 솔루션은 아니며 부족한 점이 다수 존재했으나, 기술 구현 방식과 소스코드에 대한 참고 가치를 인정받아 솔루션 및 관련 서버 자산을 매각하고 서비스를 종료

---

### 2. BGP Anycast 기반 대용량 DDoS Mitigation Scrubbing Center
> **키워드**: `BGP` `IPv4 Anycast` `ASN` `Scrubbing Center` `DDoS Defense`
> 
> 온프레미스 보안 장비(IPS/UTM/NGFW)의 물리적 한계를 뛰어넘는 대용량 트래픽 공격 대응 인프라 구축 프로젝트입니다.

* **문제 정의**: 백본망 대역폭을 초과하는 대규모 Volumetric DDoS 공격은 상용 하드웨어 장비만으로 방어 불가능
* **해결 방안**: 
  * 자사 **ASN(Autonomous System Number)** 직접 발급
  * 주요 ISP(통신사)들과 BGP 피어링 연동을 통한 **IPv4 Anycast 기반 스크러빙 센터(Scrubbing Center)** 구축
* **성과**: 백본 유입 전 우회 세척(Clean Traffic 분리) 알고리즘 적용으로 대용량 공격 완화 및 서비스 연속성 확보 *(관련 연구 자료 및 성과 문서 보유)*

---

### 3. Serverless Security-as-a-Service (SaaS) Platform & Network Analytics
> **키워드**: `SaaS` `Securityless` `Pay-as-you-go` `Traffic Optimization` `OWASP Top 10`
> 
> 보안 인프라 구축이 어려운 환경을 위해 설계된 **Serverless 형태의 Security-as-a-Service** 플랫폼입니다.

* **컨셉**: "Securityless" — 복잡한 보안 장비 설정 없이 서비스 연동만으로 실시간 위협 탐지 및 차단
* **주요 기능 & 효과**:
  * **위협 방어**: L4/L7 계층 위협 차단(OWASP Top 10, PPS 기반 DoS), ASN/GeoIP 기반 접근 제어
  * **트래픽 비용 절감 & 분석**: 비정상 트래픽 탐지 및 네트워크 취약점 분석 알고리즘을 통해 불필요한 트래픽 유입을 차단하고 네트워크 운영 비용 절감
* **비즈니스 모델**: 트래픽 사용량 기반 종량제(Pay-as-you-go) 과금 체계 운용 *(현재 서비스 중단 및 소스코드 백업 완료)*

---

## 📁 Repository Archive Status

현재 상기 프로젝트를 포함한 **40여 개의 Private Repository**(소스코드, 논문, 네트워크 취약점 분석 자료, 아키텍처 다이어그램 등)는 안전하게 백업 및 보관되어 있습니다. 

* 가상화 콘솔 소스코드 및 오케스트레이션 스크립트
* BGP Scrubbing Center 구축 보고서 및 성과 데이터
* Security SaaS 모듈, 트래픽 최적화 알고리즘 및 결제 연동 백엔드 코드

*(상세한 구현 내용 및 비공개 기술 업데이트 문서는 순차적으로 정리 중이며, 소스코드 검토나 관련 문의는 아래 LinkedIn으로 연락주시기 바랍니다.)*

---

### 📬 Contact
* **LinkedIn**: [함준형 LinkedIn 프로필](https://www.linkedin.com/in/%EC%A4%80%ED%98%95-%ED%95%A8-669898284/)
