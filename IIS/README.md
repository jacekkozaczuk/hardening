hardening IIS

POWERShell script to IIS harden Transcript of IIS Lockdown and Server Hardening IIS Lockdown / Server hardening Agenda Certificate Installation Server Lock down IIS Lock down Enabling HTTPS / Disabling HTTP Enabling TLS / Disabling SSL Securing Cookie Adding Security Header Tool set to confirm the above IIS Lock down CIS Document https://benchmarks.cisecurity.org/downloads/browse/index.cfm?category=benchmarks.servers.web.iis

Enabling HTTPS / Disabling HTTP (DEMO) IIS Settings (Top Level) and all leve) Apache (similar settings > apache.conf / httpd.conf) https://www.google.com/search?q=enabling+https+in+apache https://www.google.com/search?q=enabling+https+in+IIS Adding Security Headers IIS Settings > HTTP Response Headers Top Level and all Levels

cache-control: no-cache, no-store, must-revalidate, private pragma: no-cache X-Content-Type-Options: 'nosniff' X-Frame-Options: Deny X-XSS-Protection: 1; mode=block Strict-Transport-Security: max-age=31536000; includeSubDomains http://caniuse.com/#feat=stricttransportsecurity

Removal / Modification of following header Server name IIS Version X-Powered-By ASP.Net Version Certificate Installation Certificates should be PURCHASED Clients should be advised to purchase SHA256 certificates at minimum

Command to run $ openssl req -x509 -nodes -sha256 -days 365 -newkey rsa:2048 -keyout key_name.key -out Certificate_name.crt $ openssl pkcs12 -inkey key_name.key -in Certificate_name.crt -export -out certificate_name.pfx

Lastly Import these Certificates in MMC > Certificate Bind them in IIS Settings Server Lock Down CIS Documentation https://benchmarks.cisecurity.org/downloads/browse/index.cfm?category=benchmarks

Windows Hardening Documents https://benchmarks.cisecurity.org/tools2/windows/CIS_Microsoft_Windows_Server_2012_R2_Benchmark_v1.1.0.pdf https://benchmarks.cisecurity.org/tools2/iis/CIS_Microsoft_IIS_8_Benchmark_v1.4.0.pdf Enabling TLS / Disable SSL Usually done through loads of Registry settings We recommend a tool to do this IIS Crypto (https://www.nartac.com/Products/IISCrypto )

Securing Cookie In IIS, use Top level node and all nodes Following is the setting that is to be kept in IIS Web.Config under <System.Web> node

https://msdn.microsoft.com/en-us/library/ms228262(v=vs.100).aspx Content Security Policy IIS Settings > HTTP Response Headers Top Level and all Levels

https://content-security-policy.com/ https://content-security-policy.com/browser-test/ (if your browser support it) CSP Evaluator (https://csp-evaluator.withgoogle.com/ )

Content-Security-Policy : default-src 'none'; script-src 'self'; connect-src 'self'; img-src 'self'; style-src 'self'; More presentations by Salman Khwaja Untitled Prezi Untitled Prezi

Release Management Release Management

EPM / TFS Integration EPM / TFS Integration

More prezis by author

Popular presentations See more popular or the latest prezis
