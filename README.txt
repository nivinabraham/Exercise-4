# Exercise-4
Exercise 4: Windows problem solving

TroubleShooting Steps Folowed

1) RDP to the VM
2) checked browsing  http://localhost/   and received 503 exception, which was expected.
3) typed inetmgr to open IIS
4) Found the default app pool was in stopped state, and started the app pool and tried browsing http://localhost/ and still gave a 503 exception also stopped the app pool.
5) App pool getting automatically stopped while accessing localhost happens due to authentication issue.
6) Just to double check viewed event logs and found it was due to an authentication issue.
7) opened inetmgr navigated to default app pool-> advanced settings under process model updated the identity to the username and password provided.
8) Started the default app pool and browsed http://localhost/  and the default IIS page loaded
