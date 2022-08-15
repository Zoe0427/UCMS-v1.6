# UCMS_v1.6.0 has a vulnerability, stored cross-site scripting (XSS)

####  **vendor: http://uuu.la/** 

**Download link for UCMS-1.6 installation package: http://uuu.la/uploadfile/file/ucms_1.6.zip** 

**1.Enter the background and click site management，Next, click Import column。**

**2.Configure parameters according to the picture. Click Submit after configuration**

![1660574007038](https://user-images.githubusercontent.com/75592724/184663698-ce4c0106-4028-43fd-941f-4e2af371c096.png)

**3.Continue, click OK to import**

![1660574115465](https://user-images.githubusercontent.com/75592724/184663833-d325b61c-5951-4be5-a318-05ab1a6b3aa1.png)

**4.Next. Add after the column name:** 

```
666<script>alert(document.cookie)</script>
```

![1660574200011](https://user-images.githubusercontent.com/75592724/184663868-1758a422-aabe-4701-acdf-a514f5a726e3.png)

**5.Check the submitted content, successfully trigger XSS attack code, pop-up cookie sensitive information** 

![1660574365910](https://user-images.githubusercontent.com/75592724/184663913-1b2a4e42-dd69-427b-9dd9-8c38e50752d6.png)

**6.Any user visiting the home page will pop up. If he has logged in, the cookie value will be directly disclosed**

![1660574542291](https://user-images.githubusercontent.com/75592724/184663949-8be4645d-b3c8-415c-ac4a-55a65f9c296c.png)
