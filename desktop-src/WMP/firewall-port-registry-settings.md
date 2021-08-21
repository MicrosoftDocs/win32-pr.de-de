---
title: firewall port registry Einstellungen
description: firewall port registry Einstellungen
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player,Firewallportregistrierungseinstellungen
- Windows Media Player, Portregistrierungseinstellungen
- Windows Media Player,Registrierung
- Registrierung, Firewallporteinstellungen
- Registrierung, Porteinstellungen
- Registrierung, Einstellungen für Windows Media Player
- Firewallportregistrierungseinstellungen
- Portregistrierungseinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140f55a4008a03c2b3bc4184e2eca92129a5e30dc69f0871da856b4555daec73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576767"
---
# <a name="firewall-port-registry-settings"></a>firewall port registry Einstellungen

Windows Media Player platziert Einträge in der Registrierung, sodass Firewalls bestimmen können, ob die von der Medienbibliotheksfreigabe verwendeten Ports geöffnet oder geschlossen werden sollen.

**AkzeptierterEULA-Registrierungseintrag**

Windows Media Player verwendet den folgenden Registrierungseintrag, um anzugeben, ob der Benutzer dem Endbenutzer-Lizenzvertrag (EULA) zugestimmt hat.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



Der Wert 1 gibt an, dass der Benutzer dem Lizenzvertrag zugestimmt hat. Der Wert 0 gibt an, dass der Benutzer dem Lizenzvertrag nicht zugestimmt hat.

**WMPNSSFirewallPortsRegistrierungseintragöffnen**

Windows Media Player verwendet den folgenden Registrierungseintrag, um anzugeben, ob der Benutzer seine Medienbibliothek für andere Computer in einem Heimnetzwerk freigegeben hat.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



Der Wert 1 gibt an, dass der Benutzer die Freigabe der Bibliothek ausgewählt hat. Der Wert 0 gibt an, dass der Benutzer die Bibliothek nicht freigegeben hat.

**Ports im Zusammenhang mit der Medienbibliotheksfreigabe**

Wenn der Registrierungseintrag **WMPNSSFirewallPortsOpen** auf Windows Vista den Wert 1 hat, sollten die folgenden Ports geöffnet sein.



| Port          | Protocol                  | Prozess                         | Direction            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | TCP RTSP                  | wmpnetwk.exe                    | eingehend und ausgehend |
| 8554 - 8558   | TCP RTSP                  | wmpnetwk.exe                    | eingehend und ausgehend |
| 5004, 5005    | UDP RTCP/RTP              | wmpnetwk.exe                    | eingehend und ausgehend |
| 50004 - 50013 | UDP RTCP/RTP              | wmpnetwk.exe                    | eingehend und ausgehend |
| 1.900          | UDP SSDP                  | SSDPsrv in svchost.exe          | eingehend und ausgehend |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost in svchost.exe | stadteinwärts              |
| 10280 - 10284 | UDP WMDRM-ND-Registrierung | wmpnetwk.exe                    | eingehend und ausgehend |
| 10243         | TCP-HTTP                  | wmpnetwk.exe                    | stadteinwärts              |
| 2177          | TCP UDP qWAVE             | svchost.exe                     | eingehend und ausgehend |



 

Wenn der **Registrierungseintrag AcceptedEULA** auf Windows Vista den Wert 1 hat, sollten die folgenden Ports geöffnet sein.



| Port          | Protocol       | Prozess                         | Direction            |
|---------------|----------------|---------------------------------|----------------------|
| Alle UDP-Ports | UDP RTP, MSB   | wmplayer.exe, beliebiges Subnetz        | stadteinwärts              |
| 1.900          | UDP SSDP       | SSDPsrv/UPnPHost in svchost.exe | eingehend und ausgehend |
| 2869          | TCP SSDP, UPnP | SSDPsrv, UPnPHost               | stadteinwärts              |



 

Wenn der Registrierungseintrag **WMPNSSFirewallPortsOpen** in Microsoft Windows XP den Wert 1 hat, sollten die folgenden Ports geöffnet sein.



| Port          | Protocol                  | Prozess                         | Direction            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1.900          | UDP SSDP                  | SSDPsrv in svchost.exe          | eingehend und ausgehend |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost in svchost.exe | stadteinwärts              |
| 10280 - 10284 | UDP WMDRM-ND-Registrierung | wmpnetwk.exe                    | eingehend und ausgehend |
| 10243         | TCP-HTTP                  | wmpnetwk.exe                    | stadteinwärts              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungseinstellungen**](registry-settings.md)
</dt> </dl>

 

 




