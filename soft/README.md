# soft subdomain placeholder

This folder exists to serve a static 404 for the `soft.tekalaschool.edu.bd` vhost and to suppress repeated log noise from automated probes scanning for non-existent endpoints like `server.php`.

Contents:
- `404.shtml`: Minimal, static 404 page returned for any request.
- `.htaccess`: Rules to block `server.php` and route unmatched requests to the 404; disables directory listing and adds basic security headers.

Notes:
- If you later deploy real content under `soft/`, adjust `.htaccess` to permit those routes and update the 404 behavior.
- For stronger mitigation on the server, consider enabling `mod_security` (WAF), `mod_evasive` (rate limiting), and firewall blocks for abusive IPs seen in logs.
