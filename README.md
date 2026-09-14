# Terraform AWS Infrastructure Practice

## 1. Nginx 파이프라인 구축 - Public Instance

Terraform을 사용하여 AWS 네트워크 인프라를 구성하고,
Public Subnet에 EC2 Instance를 생성하여 Nginx를 배포하는 실습입니다.

### 주요 구성

- VPC
- Public / Private / Cluster Subnet
- Internet Gateway
- Route Table 및 Subnet Association
- NAT Instance 또는 NAT Gateway
- Security Group
- Public EC2 Instance
- Nginx 자동 설치 및 실행

### Public EC2

Public Subnet에 EC2 Instance를 생성하고 User Data를 통해
Nginx를 자동으로 설치 및 실행합니다.

```text
Internet
   │
Internet Gateway
   │
Public Route Table
   │
Public Subnet
   │
EC2 Instance
   │
Nginx :80