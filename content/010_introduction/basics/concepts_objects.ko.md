---
title: "K8s 객체 개요"
date: 2018-10-03T10:15:55-07:00
draft: false
weight: 50
---

Kubernetes 객체는 클러스터의 상태를 표현하기위해 쓰인다.

객체는 "의도의 기록(record of intent)"이다 - 생성이 되면 클러스터는 해당 객체가 정의된 그대로 존재 할 수 있도록 최선을 다한다. 이 것을 클러스터의 "이상적 상태(desired state)"라고 한다.

Kubernetes는 언제나 객체의 "현 상태"와 "이상적 상태"가 동일 할 수 있도록 노력한다. 이상적 상태는 다음 정보를 가지고 있을 수 있다:

* 어떤 pod (containers)이 어떤 노드에서 실행되고 있는지
* 컨테이너들의 논리적 그룹과 연결되는 IP endpoint들
* 특정 컨테이너의 replica가 몇개 실행되고 있는지
* 이 외 수많은 것들이 있다...

이 k8s 객체들에 대해 조금더 자세히 알아보도록 하자.