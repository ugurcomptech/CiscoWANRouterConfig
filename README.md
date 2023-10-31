# Cisco WAN(Wide Area Network) Router Config

Bu yazı da routerların birbiri arasında nasıl haberleştiğini göreceğiz, dış network ile nasıl konuşacağız onları öğreneceğiz.

LAN da Router Config yaparken birbirlerine ağ geçitleri sayesinde paket gönderiyordular, WAN'da da aynısını yapacağız routerların kendi arasında konuşacağı bir network oluşturacağız ve o IP blokları üzerinden paketler geçecektir.

## PC IP Config

Şimdi iki tane farklı networkümüz var:

- **10'lu Blok:**
  - **Ip Adres:** 192.168.10.10
  - **Ağ Maskesi:** 255.255.255.0
  - **Ağ Geçidi:** 192.168.10.1
 
- **20'lu Blok:**
  - **Ip Adres:** 192.168.20.10
  - **Ağ Maskesi:** 255.255.255.0
  - **Ağ Geçidi:** 192.168.20.1

 
![image](https://github.com/ugurcomptech/CiscoWANRouterConfig/assets/133202238/e2e3a5fe-d760-4375-a70a-50dd570d1d66)


## Router Default Gateway Config
 
İki network de farklı routerlara bağlı. Şimdi bu routerları yapılandıralım:

- **İstanbul Router FastEthernet 0/0: **
  - **Ip Adres:** 192.168.10.1
  - **Ağ Maskesi:** 255.255.255.0

- **Bursa Router FastEthernet 0/0:**
  - **Ip Adres:** 192.168.20.1
  - **Ağ Maskesi:** 255.255.255.0
 

**Not:** Bunlar bu haliyle haberleşemez çünkü routerların kendi arasında konuşacağı bir network henüz oluşturmadık.


## Router Network Config

Routerların kendi arasında konuşacağı bir network oluşturalım:


- **İstanbul Router Serial 2/0:**
  - **Ip Adres:** 10.1.1.1
  - **Ağ Maskesi:** 255.0.0.0


- **Bursa Router Serial 3/0:**
  - **Ip Adres:**10.1.1.2
  - **Ağ Maskesi:** 255.0.0.0

 
Routerların kendi arasında konuşacağı bir network oluşturduk şimdi yönlendirme yapacağız:

![image](https://github.com/ugurcomptech/CiscoWANRouterConfig/assets/133202238/64b2823f-467f-4668-af0b-bb6315b0d73f)










