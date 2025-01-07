# wordpresssecurity
Wordpress Security and Audit 
# Best Practices and Plugins For a Secure WordPress Site

# WordPress Security Vulnerabilities and Risks
WordPress is widely popular, powering approximately 40% of global websites as of 2021. Even though the platform is built to be secure, security vulnerabilities are commonly found and arise due to the actions of users or malpractices of site administrators. Since vulnerabilities typically exist in themes and plugins, securing a WordPress website often goes beyond securing the core WordPress source code.

Brute Force Attacks
Each WordPress site has a default login page (http://www.example.com/wp-admin) for administrator accounts. Attackers exploit this by trying to gain administrator privileges for the website. Considered one of the most common forms of WordPress attack, brute force attacks are initiated by hackers trying to guess user credentials using sophisticated techniques and automation. Since they do not rely on existing vulnerabilities, brute force attacks present one of the simplest means to obtain user accounts and passwords. Some administrators use weak passwords that make it easy to program bots to help them obtain the user role.

In a successful brute force WordPress attack, attackers can steal user data, install malware or erase a crucial application’s service. Even if they don’t successfully log in to the account, hackers carrying out brute force attacks can initiate denial-of-service by attempting thousands of simultaneous logins. These attacks are also difficult to identify since the bots use different locations and IP addresses for login attempts, which allows them to persist without detection. While it is a trial and error method, a brute force attack is widely popular and was involved in over 80% of the attacks on WordPress websites in 2018.

Cross-Site Scripting
In an XSS attack, hackers use existing WordPress vulnerabilities to inject malicious code into the website. These attacks mainly aim to steal another user’s identification information by hijacking their session and then executing unwanted scripts on the client side. In a typical XSS attack, a hacker utilizes a user input form to insert the malicious URL/string into the website’s database. When a victim requests a page from the site, the web server’s response includes the malicious script, which is sent to the victim’s browser. When the browser executes this script, it sends the user’s session cookies to the hacker’s machine.

WordPress XSS vulnerabilities remain a critical challenge for web security teams since they are exploited differently, making them hard to identify and mitigate on time. For this purpose, there are various tools that you can use to detect XSS attacks and take action against them.

Various types of XSS vulnerabilities include:

Stored cross-site scripting, also known as Persistent XSS, is the most alarming type of XSS that relies on malicious scripts to be permanently stored on the website’s database. This implies that whenever any user requests a page of the site, the malicious payload is sent to the user’s browser as part of the HTML response.
Reflected cross-site scripting, also known as non-persistent XSS, involves a malicious script to be sent along with the user request. A successful attack typically requires the attacker to send the malicious script to each user separately. The script is then ‘reflected’ back such that the web server’s HTTP response includes the malicious payload sent as part of the request. In this case, attackers use ambush social engineering to deceive users into sending the malicious script to the webserver.
In DOM-based XSS attacks, hackers inject malicious payloads if the website’s client-side scripts can write data provided by a Document Object Model (DOM). A common cause of this vulnerability is when developers do not include additional security measures to handle data correctly. Once injected, the malicious payload is then executed when the webserver reads data back from the DOM.
File Inclusion Exploits
WordPress file inclusion exploits affect websites that utilize a scripting runtime, allowing hackers to upload files to the WordPress server, submit input into files or modify file permissions. To do so, attackers use a configuration file to enumerate the system, provide download functionality, and allow access for undefined user roles. In the absence of sufficient user input validation, attackers also use dynamic file inclusion capabilities to include a file on the server.

WordPress file inclusion exploits are categorized as:

Local file inclusion (LFI) — These vulnerabilities enable hackers to include files on the server using their web browser. LFI exploits are easily performed on websites that accept files without properly sanitizing user input. An attacker can modify the input so that they inject special characters into the path and access other files hosted on the webserver. In most WordPress applications, successful LFI exploits occur due to insufficient validation of the Ajax path parameter when requesting the Ajax shortcode pattern.php script.
Remote file inclusion (RFI) — Attackers leverage RFI vulnerabilities to include remote files on the webserver. These attacks are less common and are carried out on websites that dynamically include external scripts and files. If the application receives an arbitrary file through an unsanitized path, it creates an attack surface, leading to information theft, XSS attacks, and remote code execution attacks.
Malware attacks
With the popularity of WordPress, there is a plethora of malicious software that disrupts how users interact with the website. Common variations of malware for WordPress websites include:

Viruses — Software that replicates by injecting malicious code into other applications. Attackers use viruses to affect the website’s core functionality or add spam content that degrades the user experience.
Trojan horse — Hackers use Trojan horses to perform a wide range of malicious actions for a WordPress website, including corrupting the wp-config.php file, FTP files and exploiting the system’s resources.
Ransomware — Some attacks, like the WannaCry attack, make WordPress websites inaccessible until the hackers are paid to remove the malicious software. This can have catastrophic effects, including loss of revenue, tarnished reputation, and penalties from compliance authorities.
Other malware used to compromise WordPress websites includes cryptocurrency mining bots, adware, and spyware.

The major security issue to be considered for WordPress sites
Attackers could use malicious SQL statements to compromise the database of WordPress websites, orchestrating SQL injection attacks. They inject SQL codes in stealth mode via the data accepted and transmitted from the website. This commonly involves using an input field to supply masked queries that contain special characters. These characters are used by the SQL interpreter in the execution of external commands. Common entry points for WordPress SQLi attacks include feedback fields, search bars, shopping carts, and logging-in forms, signing up, or contact submission.

The WordPress CMS uses SQL-based databases, making SQLi attacks a standard mode of exploitation. Since all the forums, blogs, and websites have input interfaces that accept user data; most WordPress sites have at least one known SQL injection point. In addition, many available SQLi vulnerability scanning tools are online, making it easy for an attacker to get started on the exploit. In successful SQLi attacks, the hackers gain complete control of the database, thereby leading to deeper penetration of the system and the exposure of sensitive data.

The importance to find WordPress Security issues for business
Being an open-source platform, almost anyone can contribute to the core WordPress software. While this openness offers flexibility, it also raises concerns regarding the security of the platform’s overall construct. Identifying and fixing vulnerabilities before they make it to production helps security teams avoid the expenses associated with recovering from a breach. Businesses also avoid the hefty penalties and fines that compliance authorities charge for exposing private information.

Addressing WordPress security issues also helps protect the firm’s reputation since safeguarding customer data is known to maintain a competitive edge. Furthermore, with every additional security measure in place, administrators can operate websites without compromising business relationships. Along with safeguarding access credentials, addressing WordPress vulnerabilities mostly requires administering robust practices to prevent all platform layers, including the core WordPress functionality, external themes and plugins, and the underlying infrastructure.

Why have WordPress Sites vulnerabilities?
Various factors make WordPress websites susceptible to attack. These include:

Use of an outdated theme, plugin, or core
Using outdated versions increases the chance of successful exploits since version updates include fixes for known vulnerabilities in the code. WordPress rolls out new versions every three months, so it is important to check for the stable version update list to ensure the website’s components are up to date.



Use of common and weak passwords
The WordPress admin login is one of the most highly targeted threat vectors since it grants the highest possible privileges. Some WordPress users set up the admin portal with common passwords that are easy to guess and are naturally more susceptible to exploits. In cases where the admin user ID is admin, it is easy to brute-force login into the system since bots go through fewer login attempts. A compromised admin account makes it easy to orchestrate a data breach on the website and is the most commonly known first level of penetration for full-blown attacks.



