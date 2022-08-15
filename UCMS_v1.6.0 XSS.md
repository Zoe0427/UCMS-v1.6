# UCMS_v1.6.0 has a vulnerability, stored cross-site scripting (XSS)

####  **vendor: http://uuu.la/** 

**Download link for UCMS-1.6 installation package: http://uuu.la/uploadfile/file/ucms_1.6.zip** 

**1.Enter the background and click site management，Next, click Import column。**

**2.Configure parameters according to the picture. Click Submit after configuration**

![1660574007038](C:\Users\17553\AppData\Roaming\Typora\typora-user-images\1660574007038.png)

**3.Continue, click OK to import**

![1660574115465](C:\Users\17553\AppData\Roaming\Typora\typora-user-images\1660574115465.png)

**4.Next. Add after the column name:** 

```
666<script>alert(document.cookie)</script>
```

![1660574200011](C:\Users\17553\AppData\Roaming\Typora\typora-user-images\1660574200011.png)

**5.Check the submitted content, successfully trigger XSS attack code, pop-up cookie sensitive information** 

![1660574365910](C:\Users\17553\AppData\Roaming\Typora\typora-user-images\1660574365910.png)

**6.Any user visiting the home page will pop up. If he has logged in, the cookie value will be directly disclosed**

![1660574542291](C:\Users\17553\AppData\Roaming\Typora\typora-user-images\1660574542291.png)