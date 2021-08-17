---
title: Standardnetzwerk-Einstellungen
description: Standardnetzwerk-Einstellungen
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Medienformat-SDK, Standardnetzwerkeinstellungen
- Advanced Systems Format (ASF), Standardnetzwerkeinstellungen
- ASF (Advanced Systems Format), Standardnetzwerkeinstellungen
- Windows Medienformat-SDK, Netzwerkeinstellungen
- Advanced Systems Format (ASF), Netzwerkeinstellungen
- ASF (Advanced Systems Format), Netzwerkeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591bf4aa2154d5cc04a8a17b5fc75f290a8493a39d530d4246bc0338c2424e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931420"
---
# <a name="default-networking-settings"></a>Standardnetzwerk-Einstellungen

In den folgenden Tabellen werden die Standardeinstellungen der Netzwerkparameter im Windows Media Format SDK nach Schnittstelle 2.



| IWMReaderNetworkConfig                | Standardeinstellung              |
|---------------------------------------|------------------------------|
| Pufferzeit                        | 5 Sekunden                    |
| UseFixedUDPPort                       | FALSE                        |
| FixedUDPPort                          | 0 (ungültig)                |
| ProxySetting: HTTP                    | \_ \_ WMT-PROXYEINSTELLUNGSBROWSER \_ |
| ProxySetting: MMS                     | \_WMT-PROXYEINSTELLUNG \_ \_ NONE    |
| ProxySetting: RTSP                    | \_WMT-PROXYEINSTELLUNG \_ \_ NONE    |
| ProxyHostName (HTTP, MMS, RTSP)       | ""                           |
| ProxyPort: HTTP                       | 80                           |
| ProxyPort: MMS                        | 1755                         |
| ProxtPort: RTSP                       | 554                          |
| ProxyExceptionList (HTTP, MMS, RTSP)  | ""                           |
| ProxyBypassForLocal (HTTP, MMS, RTSP) | FALSE                        |
| ForceRerunAutoDetection               | FALSE                        |
| EnableMulticast                       | TRUE                         |
| EnableHTTP                            | TRUE                         |
| EnableTCP                             | TRUE                         |
| EnableUDP                             | TRUE                         |
| Verbindungsbandbreite                  | 0 (automatische Erkennung)              |



 



| IWMReaderNetworkConfig2        | Standardeinstellung        |
|--------------------------------|------------------------|
| Beschleunigte Streamingdauer | 100000000 (10 Sekunden) |
| Aktivieren der Inhaltszwischenspeicherung         | TRUE                   |
| Aktivieren des schnellen Caches              | TRUE                   |
| Erneutes Senden aktivieren                 | TRUE                   |
| Aktivieren der Inhaltsverankerung        | TRUE                   |
| Grenzwert für erneute Verbindung                | 25                     |



 



| IWMWriterNetworkSink | Standardeinstellung         |
|----------------------|-------------------------|
| Max. Anzahl von Clients      | 5                       |
| Netzwerkprotokoll     | 0 (WMT \_ PROTOCOL \_ HTTP) |
| Host-URL             | 0 (ungültig)           |



 



| IWMWriterAdvanced2  | Standardeinstellung             |
|---------------------|-----------------------------|
| Maximale Paketgröße | 1400                        |
| Protokollclient-ID       | FALSE                       |
| Wiedergabemodus           | WMT \_ PLAY \_ MODE \_ AUTOSELECT |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von Netzwerkfunktionen**](implementing-network-functionality.md)
</dt> </dl>

 

 




