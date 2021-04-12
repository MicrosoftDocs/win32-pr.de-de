---
title: Informationen über EAP
description: Extensible Authentication Protocol (EAP), ein Standard, der von vielen Microsoft-Netzwerkkomponenten unterstützt wird.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Extensible Authentication-Protokoll, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391133"
---
# <a name="about-eap"></a>Informationen über EAP

In diesem Thema wird das Extensible Authentication Protocol (EAP) beschrieben, ein Standard, der von vielen Microsoft-Netzwerkkomponenten unterstützt wird.

## <a name="eap-components"></a>EAP-Komponenten

EAP ist für den Schutz der Sicherheit von drahtlosen LANs (802.1 x), verkabelten LANs und Einwähl-und VPN-Verbindungen (Virtual Private Networks, VPNs) entscheidend.

Die folgenden Komponenten unterstützen das EAP-Protokoll.

-   Microsoft-Remote Zugriffs Clients und-Server für DFÜ und VPN (PPTP und L2TP/IPSec) implementieren EAP als Erweiterung für PPP. Weitere Informationen finden Sie unter [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   Microsoft IEEE 802.1 x-kompatible drahtlose und verkabelte LAN-Clients implementieren EAP gemäß der Definition im IEEE 802.1 x-Entwurfs Standard.
-   Microsoft RADIUS Server (Internet Authentication Service, IAS) implementiert EAP, wie in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055)definiert.

Alle oben genannten Komponenten unterstützen diese erweiterbare Architektur über das Microsoft Windows Software Development Kit (SDK), sodass Sie Authentifizierungs Module von Drittanbietern integrieren können. Dieser erweiterbare Mechanismus kann verwendet werden, um Token-Karten, Kerberos-, Public Key-und S/Key-Authentifizierungsprotokolle zu unterstützen.

## <a name="protected-extensible-authentication-protocol"></a>Geschütztes erweiterbares Authentifizierungsprotokoll

Zusätzlich zu EAP unterstützen auch die Wireless-Implementierung (802.1 x) und der RADIUS-Server einen neuen Standard namens Protected EAP (PEAP).

PEAP bietet wie folgt verschiedene wichtige Dienste für andere EAP-Authentifizierungsprotokolle.

-   PEAP verschlüsselt EAP-Pakete anderer EAP-Authentifizierungsprotokolle mithilfe von Transport Layer Security (TLS), einer Secure Socket Layer (SSL)-basierten Technologie. Weitere Informationen finden Sie unter [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   Der Server wird von der Serverseite mithilfe eines Serverzertifikats mit RADIUS-Server authentifiziert.
-   Peer-App bietet eine schnelle erneute Authentifizierung, die effizientes Roaming zwischen drahtlosen Geräten unterstützt.
-   PEAP verwaltet die Fragmentierung und neuassembly von EAP-Paketen.
-   Peer generiert Schlüssel zum Verschlüsseln von drahtlosem Datenverkehr.

PEAP vereinfacht das Schreiben eines EAP-Protokolls erheblich, da der Programmierer diese Probleme nicht mehr beheben muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu EAP und EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




