
## kc_etp 에서 tm_etpportal_talk를 날렸을 때 쓴 방법

- dump 파일 위치: /nas/backup/ndb
- dump 파일명: kc_etp_20210512.cmp

- 특정 테이블 내용만 떠서 저장
```
  # sed -n -e '/DROP TABLE.*tm_etpportal_talk/,/UNLOCK TABLES/p' kc_etp_20210512.dmp > kc_etp_talk_20210512.sql
```

- 주의사항:
kc_etp db에는 tm_etpportal_talk{$|_like|_test|_test_like}의 총 4가지 테이블이 있어서 모두 떠짐.
필요한 부분만 notepad 에서 추출해서 돌렸음.


  
  

