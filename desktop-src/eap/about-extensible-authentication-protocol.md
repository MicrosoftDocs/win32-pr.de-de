---
title: Informationen zu EAP
description: Extensible Authentication Protocol (EAP), ein Standard, der von vielen Microsoft-Netzwerkkomponenten unterstützt wird.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Extensible Authentication Protocol, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84866f7f550213850bf95c39a6f0847df31bed3550db66139f2ec30bf921b5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276043"
---
# <a name="about-eap"></a>Informationen zu EAP

In diesem Thema wird das Extensible Authentication Protocol (EAP) beschrieben, ein Standard, der von vielen Microsoft-Netzwerkkomponenten unterstützt wird.

## <a name="eap-components"></a>EAP-Komponenten

EAP ist entscheidend für den Schutz der Sicherheit von DRAHTLOSEN (802.1X) LANs, kabelgebundenen LANs und DFÜ- und virtuellen privaten Netzwerken (VPNs).

Die folgenden Komponenten unterstützen das EAP-Protokoll.

-   Microsoft-Remotezugriffsclients und -server für DFÜ und VPN (PPTP und L2TP/IPSec) implementieren EAP als Erweiterung für FTP. Weitere Informationen finden Sie unter [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   Microsoft IEEE 802.1X-kompatible Drahtlos- und Kabel-LAN-Clients implementieren EAP gemäß definition im IEEE 802.1X-Entwurfsstandard.
-   Der MICROSOFT RADIUS-Server mit dem Namen Internet Authentication Service (IAS) implementiert EAP gemäß [RFC 2865.](https://go.microsoft.com/fwlink/p/?linkid=84055)

Alle oben genannten Komponenten unterstützen diese erweiterbare Architektur über das Microsoft Windows Software Development Kit (SDK), wodurch die Integration von Authentifizierungsmodulen von Drittanbietern möglich ist. Dieser erweiterbare Mechanismus kann verwendet werden, um Tokenkarten, Kerberos, öffentlicher Schlüssel und S/Key-Authentifizierungsprotokolle zu unterstützen.

## <a name="protected-extensible-authentication-protocol"></a>Protected Extensible Authentication Protocol

Zusätzlich zu EAP unterstützen die Drahtlose Implementierung (802.1X) und der RADIUS-Server auch einen neuen Standard namens Protected EAP (PEAP).

PEAP stellt wie folgt mehrere wichtige Dienste für andere EAP-Authentifizierungsprotokolle bereit.

-   PEAP verschlüsselt EAP-Pakete anderer EAP-Authentifizierungsprotokolle mithilfe von Transport Layer Security (TLS), einer SSL-basierten Technologie (Secure Socket Layer). Weitere Informationen finden Sie unter [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   PEAP authentifiziert die serverseitige Mithilfe eines Serverzertifikats mit RADIUS-Server.
-   PEAP bietet eine schnelle Funktion zur erneuten Authentifizierung, die effizientes Roaming zwischen Drahtlosgeräten unterstützt.
-   PEAP verwaltet die Fragmentierung und Neuassembly von EAP-Paketen.
-   PEAP generiert Schlüssel, die zum Verschlüsseln von Funkdatenverkehr verwendet werden.

PEAP erleichtert das Schreiben eines EAP-Protokolls, da der Programmierer diese Probleme nicht mehr beheben muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu EAP und EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




