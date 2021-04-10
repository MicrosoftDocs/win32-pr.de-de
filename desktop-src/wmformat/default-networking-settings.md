---
title: Standard Netzwerkeinstellungen
description: Standard Netzwerkeinstellungen
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media-Format-SDK, standardmäßige Netzwerkeinstellungen
- Advanced Systems Format (ASF), Standard Netzwerkeinstellungen
- ASF (Advanced Systems Format), standardmäßige Netzwerkeinstellungen
- Windows Media-Format-SDK, Netzwerkeinstellungen
- Advanced Systems Format (ASF), Netzwerkeinstellungen
- ASF (Advanced Systems Format), Netzwerkeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856924"
---
# <a name="default-networking-settings"></a>Standard Netzwerkeinstellungen

In den folgenden Tabellen werden die Standardeinstellungen der Netzwerkparameter im Windows Media-Format-SDK, gruppiert nach Schnittstelle, beschrieben.



| Iwmreadernetworkconfig                | Standardeinstellung              |
|---------------------------------------|------------------------------|
| Pufferzeit                        | 5 Sekunden                    |
| Usefixedudpport                       | false                        |
| Fixedudpport                          | 0 (ungültig)                |
| Proxysetting: http                    | WMT- \_ Proxy \_ Einstellungs \_ Browser |
| Proxysetting: MMS                     | WMT- \_ Proxy \_ Einstellung \_ None    |
| Proxysetting: RTSP                    | WMT- \_ Proxy \_ Einstellung \_ None    |
| Proxyhostname (http, MMS, RTSP)       | ""                           |
| Proxyport: http                       | 80                           |
| Proxyport: MMS                        | 1755                         |
| Proxtport: RTSP                       | 554                          |
| Proxyexceptionlist (http, MMS, RTSP)  | ""                           |
| Proxybypassforlocal (http, MMS, RTSP) | false                        |
| Forcererunautoerkennungs               | false                        |
| Enablemulticast                       | TRUE                         |
| Enablehttp                            | TRUE                         |
| Enabletcp                             | TRUE                         |
| EnableUDP                             | TRUE                         |
| Verbindungs Bandbreite                  | 0 (automatische Erkennung)              |



 



| IWMReaderNetworkConfig2        | Standardeinstellung        |
|--------------------------------|------------------------|
| Beschleunigte streamingdauer | 100 Millionen (10 Sekunden) |
| Zwischenspeichern von Inhalt aktivieren         | TRUE                   |
| Schnellen Cache aktivieren              | TRUE                   |
| Erneute Sende Vorgänge aktivieren                 | TRUE                   |
| Inhalts Verdünnung aktivieren        | TRUE                   |
| Limit für erneute Verbindungs Herstellung                | 25                     |



 



| Iwmschreiternetworksink | Standardeinstellung         |
|----------------------|-------------------------|
| Max. Anzahl von Clients      | 5                       |
| Netzwerkprotokoll     | 0 (WMT- \_ Protokoll \_ http) |
| Host-URL             | 0 (ungültig)           |



 



| IWMWriterAdvanced2  | Standardeinstellung             |
|---------------------|-----------------------------|
| Maximale Paketgröße | 1400                        |
| Protokoll Client-ID       | false                       |
| Wiedergabemodus           | WMT- \_ Wiedergabe \_ Modus \_ Autoselect |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Netzwerkfunktionen**](implementing-network-functionality.md)
</dt> </dl>

 

 




