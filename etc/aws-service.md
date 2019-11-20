# AWS service 설명

## 주요 용어 정리

* region
  * 각 리전은 개별 지리 영역입니다.
  * [region별 service](https://aws.amazon.com/ko/about-aws/global-infrastructure/regional-product-services/)

* availity zone
  * 각 가용 영역은 서로 격리되어 있지만, 한 리전 안의 가용 영역은 지연 시간이 짧은 링크를 통해 연결되어 있습니다.
  * [AWS 글로벌 인프라 맵](https://aws.amazon.com/ko/about-aws/global-infrastructure/)

* edge location
  * AWS에서 CloudFront의 cache 서버
  * [CloudFront](https://aws.amazon.com/ko/cloudfront/features/?nc=sn&loc=2)

## computing

### ec2

#### instance

* spot instance

    Amazon EC2 스팟 인스턴스를 사용하면 AWS 클라우드에서 미사용 EC2 용량을 활용할 수 있습니다. 스팟 인스턴스는 온디맨드 요금과 비교하여 최대 90% 할인된 금액으로 제공됩니다.

* reserved instance

    Amazon EC2 예약 인스턴스(RI)는 온디맨드 요금과 비교하여 상당한 할인 혜택(최대 75%)을 제공하며 특정 가용 영역에서 사용하는 경우에는 용량 예약을 제공합니다.

* on-demand instance

### lambda

* AWS Lambda는 서버를 프로비저닝하거나 관리하지 않고도 코드를 실행할 수 있게 해주는 컴퓨팅 서비스입니다.

* AWS Lambda는 필요 시에만 코드를 실행하며, 하루에 몇 개의 요청에서 초당 수천 개의 요청까지 자동으로 확장이 가능합니다. 사용한 컴퓨팅 시간에 대해서만 요금을 지불하면 되고 코드가 실행되지 않을 때는 요금이 부과되지 않습니다.

## storage

* object storage(S3)
* file storage(EFS)
* volume storage(EBS)

## Database

### RDS

* Aurora
* MySQL

### NoSQL

* DynamoDB
* SimpleDB

## IAM

* group
* user
* rule
* policy

## network

* VPC
  * Virtual Private Cloud(VPC)는 사용자의 AWS 계정 전용 가상 네트워크입니다.
* subnet
  * 서브넷은 VPC의 IP 주소 범위입니다. 지정된 서브넷으로 AWS 리소스를 시작할 수 있습니다.
  * 인터넷에 연결되어야 하는 리소스에는 퍼블릭 서브넷을 사용하고, 인터넷에 연결되지 않는 리소스에는 프라이빗 서브넷을 사용하십시오.

## Cache

### CloudFront

* .html, .css, .js 및 이미지 파일과 같은 정적 및 동적 웹 콘텐츠를 사용자에게 더 빨리 배포하도록 콘텐츠를 edge location에 caching합니다.

* CloudFront는 edge location이라고 하는 데이터 센터의 전 세계 네트워크를 통해 콘텐츠를 제공합니다. CloudFront를 통해 서비스하는 콘텐츠를 사용자가 요청하면 지연 시간이 가장 낮은 엣지 로케이션으로 라우팅되므로 콘텐츠 전송 성능이 뛰어납니다.

## API Gateway

* Amazon API Gateway는 규모와 상관없이 REST 및 WebSocket API를 생성, 게시, 유지하고 모니터링 및 보안하기 위한 AWS 서비스입니다.

## Reference

* [storage 종류별 특징](https://www.redhat.com/ko/topics/data-storage/file-block-object-storage)
