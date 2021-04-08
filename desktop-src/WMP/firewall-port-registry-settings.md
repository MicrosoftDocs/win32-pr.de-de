---
title: Registrierungs Einstellungen für den Firewallport
description: Registrierungs Einstellungen für den Firewallport
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, Registrierungs Einstellungen für Firewallports
- Windows Media Player, Port Registrierungs Einstellungen
- Windows Media Player, Registrierung
- Registrierung, firewallporteinstellungen
- Registrierung, Port Einstellungen
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für den Firewallport
- Port Registrierungs Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855564"
---
# <a name="firewall-port-registry-settings"></a>Registrierungs Einstellungen für den Firewallport

Windows Media Player fügt Einträge in die Registrierung ein, damit Firewalls feststellen können, ob die von der Medien Bibliotheks Freigabe verwendeten Ports geöffnet oder geschlossen werden.

**Registrierungs Eintrag "akzeptede"**

Windows Media Player verwendet den folgenden Registrierungs Eintrag, um anzugeben, ob der Benutzer den Endbenutzer-Lizenzvertrag (EULA) akzeptiert hat.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



Der Wert 1 gibt an, dass der Benutzer den Lizenzvertrag akzeptiert hat. Der Wert 0 gibt an, dass der Benutzer den Lizenzvertrag nicht akzeptiert hat.

**Wmpnssfirewallportsopen-Registrierungs Eintrag**

Windows Media Player verwendet den folgenden Registrierungs Eintrag, um anzugeben, ob der Benutzer seine Medienbibliothek auf anderen Computern in einem Heimnetzwerk freigeben möchte.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



Der Wert 1 gibt an, dass der Benutzer die Bibliothek freigegeben hat. Der Wert 0 gibt an, dass der Benutzer die Bibliothek nicht freigeben möchte.

**Ports im Zusammenhang mit der Medien Bibliotheks Freigabe**

Wenn unter Windows Vista der Registrierungs Eintrag **wmpnssfirewallportsopen** den Wert 1 aufweist, sollten die folgenden Ports geöffnet sein.



| Port          | Protocol                  | Prozess                         | Richtung            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | TCP-RTSP                  | wmpnetwk.exe                    | eingehende und ausgehende Daten |
| 8554-8558   | TCP-RTSP                  | wmpnetwk.exe                    | eingehende und ausgehende Daten |
| 5004, 5005    | UDP RTCP/RTP              | wmpnetwk.exe                    | eingehende und ausgehende Daten |
| 50004-50013 | UDP RTCP/RTP              | wmpnetwk.exe                    | eingehende und ausgehende Daten |
| 1.900          | UDP-SSDP                  | SSDPSRV in svchost.exe          | eingehende und ausgehende Daten |
| 2869          | TCP SSDP, UPnP            | SSDPSRV/UPnPHost in svchost.exe | stadteinwärts              |
| 10280-10284 | UDP WMDRM-ND-Registrierung | wmpnetwk.exe                    | eingehende und ausgehende Daten |
| 10243         | TCP http                  | wmpnetwk.exe                    | stadteinwärts              |
| 2177          | TCP-UDP-qWave             | svchost.exe                     | eingehende und ausgehende Daten |



 

Wenn unter Windows Vista der Registrierungs Eintrag " **akzeptedeula** " den Wert 1 aufweist, sollten die folgenden Ports geöffnet sein.



| Port          | Protocol       | Prozess                         | Richtung            |
|---------------|----------------|---------------------------------|----------------------|
| Alle UDP-Ports | UDP RTP, MSB   | wmplayer.exe, alle Subnetze        | stadteinwärts              |
| 1.900          | UDP-SSDP       | SSDPSRV/UPnPHost in svchost.exe | eingehende und ausgehende Daten |
| 2869          | TCP SSDP, UPnP | SSDPSRV, UPnPHost               | stadteinwärts              |



 

Wenn unter Microsoft Windows XP der Registrierungs Eintrag **wmpnssfirewallportsopen** den Wert 1 aufweist, sollten die folgenden Ports geöffnet sein.



| Port          | Protocol                  | Prozess                         | Richtung            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1.900          | UDP-SSDP                  | SSDPSRV in svchost.exe          | eingehende und ausgehende Daten |
| 2869          | TCP SSDP, UPnP            | SSDPSRV/UPnPHost in svchost.exe | stadteinwärts              |
| 10280-10284 | UDP WMDRM-ND-Registrierung | wmpnetwk.exe                    | eingehende und ausgehende Daten |
| 10243         | TCP http                  | wmpnetwk.exe                    | stadteinwärts              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen**](registry-settings.md)
</dt> </dl>

 

 




