
- 리눅스 환경에서 RAM이 부족할 경우 HDD의 일정 공간을 RAM처럼 사용할 수 있는 방법

swap 메모리 할당
```bash
sudo dd if=/dev/zero of=/swapfile bs=128M count=16
```

swap 파일 권한 설정
```bash
sudo chmod 600 /swapfile
```

linux swap 영역 설정
```bash
sudo mkswap /swapfile
```

swap 공간에 파일 추가
```bash
sudo swapon /swapfile
```

부팅 시 스왑 파일 활성화: /etc/fstab 파일의 맨 끝에 아래 라인 추가 후 저장
```text
/swapfile swap swap defaults 0 0
```

- 레퍼런스: https://sundries-in-myidea.tistory.com/102
