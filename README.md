# CMSmadesimple Stored XSS v2.2.18

## Author: (Sergio)

**Description:** Cross Site Scripting vulnerability in CMSmadesimple v.2.2.18 allows a local attacker to execute arbitrary code via a crafted script to the Title in the My Preferences - Manage Shortcuts

**Attack Vectors:** Scripting A vulnerability in the sanitization of the entry in the Title of "My Preferences - Manage Shortcuts" allows injecting JavaScript code that will be executed when the user accesses the web page.

---

### POC:


When logging into the panel, we will go to the "My Preferences - Manage Shortcuts" section off General Menu.

![XSS Shortcut](https://github.com/sromanhu/CMSmadesimple-Stored-XSS---Shortcut/assets/87250597/2b7b2c25-b1b8-4dcd-8847-158da95a78da)




We edit that Content - News Menu with the payload that we have created and see that we can inject arbitrary Javascript code in the Title field.


### XSS Payload:

```js
'"><svg/onload=alert('Title')>
```


In the following image you can see the embedded code that executes the payload in the main web.
![XSS Shortcut resultado](https://github.com/sromanhu/CMSmadesimple-Stored-XSS---Shortcut/assets/87250597/0348c5a5-84ad-4b19-8774-e3bbe1376e78)








</br>

### Additional Information:
http://www.cmsmadesimple.org/

https://owasp.org/Top10/es/A03_2021-Injection/
