# Progress of Penetration Testing - Discovering

![](https://i.imgur.com/cZ5oMl9.png)
(The phase defintion is from IBM courses.)

* The phase of discovering will be a cycle if we get stuck to step to next phase. In this situation, we need to gather more clues.

## Server side

* First, we get ports and services by Nmap on server side, and narrow down the range gradually.
* Example: 

    In machine DC-9

    ``` 
    > nmap 192.168.100.0/24
    we found that the IP of DC-9 is 192.168.100.2
    
    > nmap -A -Pn -p- 192.168.100.2
    we can gather mor detail information in DC-9, such as ports, states, services, and versions.
    ```
    ![](https://i.imgur.com/EgZVGFo.png)
    
--- 
    
* Some ports may not scanned because the firewall blocks the specific ports. After accessing the target, we can scan this machine again to gather unshowed information before.

* Example:

    In machine Symfonos2
    ```
    > nmap -A -Pn -p- -sV 127.0.0.1
    we found 8080 port after entering Symfonos2.
    ```
    ![](https://i.imgur.com/OYIWZDh.png)

--- 




