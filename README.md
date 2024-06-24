
# Hydra

## Introduction
Hydra is a powerful tool for performing brute-force attacks on various services. It supports a wide range of protocols and can be used to test the security of your systems by identifying weak passwords.
## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
  - [Example 1: SSH Brute Force](#example-1-ssh-brute-force)
  - [Example 2: FTP Brute Force](#example-2-ftp-brute-force)
  - [Example 3: Web Form Brute Force](#example-3-web-form-brute-force)
  - [Example 4: SMTP Brute Force](#example-4-smtp-brute-force)
  - [Example 5: MySQL Brute Force](#example-5-mysql-brute-force)
  - [Example 6: RDP Brute Force](#example-6-rdp-brute-force)
  - [Example 7: Telnet Brute Force](#example-7-telnet-brute-force)
  - [Example 8: HTTP Basic Authentication Brute Force](#example-8-http-basic-authentication-brute-force)
  - [Example 9: VNC Brute Force](#example-9-vnc-brute-force)
  - [Example 10: SNMP Brute Force](#example-10-snmp-brute-force)
- [Best Practices](#best-practices)
- [Contributing](#contributing)
- [Credits](#credits)
- [License](#license)


## Installation
To install Hydra, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/vanhauser-thc/thc-hydra
    ```
2. Change to the Hydra directory:
    ```sh
    cd thc-hydra
    ```
3. Compile Hydra:
    ```sh
    ./configure
    make
    make install
    ```

## Usage
Hydra can be used to perform brute-force attacks on various services. Here is a basic usage example:

```sh
hydra -L username_list.txt -P password_list.txt target_ip ssh
```

## Examples
Here are some pseudocode examples to illustrate how Hydra can be used:

### Example 1: SSH Brute Force
```pseudo
// Define the target IP and the protocol
target_ip = "192.168.1.1"
protocol = "ssh"

// Define the username and password lists
username_list = ["admin", "user", "test"]
password_list = ["password123", "admin", "123456"]

// Execute the brute force attack
hydra -L username_list -P password_list target_ip protocol
```

### Example 2: FTP Brute Force
```pseudo
// Define the target IP and the protocol
target_ip = "192.168.1.2"
protocol = "ftp"

// Define the username and password lists
username_list = ["ftpuser", "anonymous"]
password_list = ["ftp123", "anonymous"]

// Execute the brute force attack
hydra -L username_list -P password_list target_ip protocol
```

### Example 3: Web Form Brute Force
```pseudo
// Define the target URL and the protocol
target_url = "http://example.com/login"
protocol = "http-post-form"

// Define the username and password lists
username_list = ["admin", "user"]
password_list = ["admin123", "password"]

// Define the login form parameters
form_parameters = "/login:username=^USER^&password=^PASS^:Invalid username or password"

// Execute the brute force attack
hydra -L username_list -P password_list target_url protocol form_parameters
```

### Example 4: SMTP Brute Force
```
// Define the target IP and the protocol
target_ip = "192.168.1.3"
protocol = "smtp"

// Define the username and password lists
username_list = ["admin@example.com", "user@example.com"]
password_list = ["admin123", "password"]

// Execute the brute force attack
hydra -L username_list -P password_list target_ip protocol
```
### Example 5: MySQL Brute Force
```
// Define the target IP and the protocol
target_ip = "192.168.1.4"
protocol = "mysql"

// Define the username and password lists
username_list = ["root", "admin"]
password_list = ["rootpass", "adminpass"]

// Execute the brute force attack
hydra -L username_list -P password_list target_ip protocol
```
### Example 6: RDP Brute Force
```
// Define the target IP and the protocol
target_ip = "192.168.1.5"
protocol = "rdp"

// Define the username and password lists
username_list = ["Administrator", "User"]
password_list = ["admin123", "password"]

// Execute the brute force attack
hydra -L username_list -P password_list target_ip protocol
```
### Example 7: Telnet Brute Force
```
// Define the target IP and the protocol
target_ip = "192.168.1.6"
protocol = "telnet"

// Define the username and password lists
username_list = ["root", "admin"]
password_list = ["toor", "admin123"]

// Execute the brute force attack
hydra -L username_list -P password_list target_ip protocol
```
### Example 8: HTTP Basic Authentication Brute Force
```
// Define the target URL and the protocol
target_url = "http://example.com/protected"
protocol = "http-get"

// Define the username and password lists
username_list = ["admin", "user"]
password_list = ["admin123", "password"]

// Execute the brute force attack
hydra -L username_list -P password_list target_url protocol
```
### Example 9: VNC Brute Force
```
// Define the target IP and the protocol
target_ip = "192.168.1.7"
protocol = "vnc"

// Define the password list (VNC typically only uses a password)
password_list = ["password", "vncpass"]

// Execute the brute force attack
hydra -P password_list target_ip protocol
```


## Best Practices
- Always ensure you have permission before performing any brute-force attacks.
- Use strong and unique passwords to protect your own systems.
- Regularly update Hydra to benefit from the latest features and security updates.

## Contributing
Contributions are welcome! Please submit a pull request or open an issue to discuss your ideas.

## Credits
Hydra is developed by van Hauser and other contributors. See [Link](https://github.com/vanhauser-thc/thc-hydra)

## License
Hydra is licensed under the GPL-3.0 License. See the `LICENSE` file for more details.
