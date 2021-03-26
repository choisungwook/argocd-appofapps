# 개요
* jmeter master, server(slave) helm
> jmeter 도커라이징: https://github.com/choisungwook-dockerfile/jmeter

# 준비
* jmeter jmx템플릿

# 설정
## override_values 필드 값 변경
* jmx템플릿 마운트 경로
```yaml
nodeSelector:
  kubernetes.io/hostname: [노드 이름]

master:
  persistence:
    hostPath:
      path: [jmx 경로]
```

# helm 설치
```sh
helm install jmeter -f override_values.yaml .
```

# 실행
```sh
./start.sh
```

# 참고자료
* https://github.com/pedrocesar-ti/distributed-jmeter-docker