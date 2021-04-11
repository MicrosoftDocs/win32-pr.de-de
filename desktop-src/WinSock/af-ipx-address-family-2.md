---
description: Die IPX-Adressfamilie definiert die Adressierungs Struktur für Protokolle, die die IPX-Standard socketadressierung verwenden. Für diese Transporte besteht eine Endpunkt Adresse aus einer Netzwerk Nummer, einer Knotenadresse und einer Socketnummer.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: AF_IPX-Adressfamilie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129228"
---
# <a name="af_ipx-address-family"></a>AF- \_ IPX-Adressfamilie

Die IPX-Adressfamilie definiert die Adressierungs Struktur für Protokolle, die die IPX-Standard socketadressierung verwenden. Für diese Transporte besteht eine Endpunkt Adresse aus einer Netzwerk Nummer, einer Knotenadresse und einer Socketnummer.

Die Netzwerk Nummer ist eine administrative Domäne und benennt in der Regel ein einzelnes Ethernet-oder tokenringsegment. Die Knotennummer ist die physische Adresse einer Station. Die Kombination aus Netz und Knoten bildet eine eindeutige Stationsadresse, die in der Welt als eindeutig angesehen wird. NET-und Knoten Nummern werden in ASCII-Text entweder in Block-oder gestrichelte Notation wie folgt dargestellt: "0101a040, 00001b498765" oder "01-01-a0-40, 00-00-1B-49-87-65". Führende Nullen müssen nicht vorhanden sein.

Die IPX-Socketnummer ist eine Netzwerk-/transportdienstnummer ähnlich einer TCP-Portnummer und sollte nicht mit dem Winsock-socketdeskriptor verwechselt werden. IPX-Socketnummern sind global für die Endstation und können nicht an bestimmte Netzwerk-/Knoten-Adressen gebunden werden. Wenn die Endstation beispielsweise über zwei Netzwerkschnittstellenkarten verfügt, kann ein gebundener Socket beide Karten senden und empfangen. Insbesondere Datagramm-Sockets würden Broadcast Datagramme auf beiden Karten empfangen.

> [!Caution]  
> SOCKADDR \_ IPX beträgt 14 Bytes und ist kürzer als die 16-Byte- [**sockaddr**](sockaddr-2.md) -Referenzstruktur. IPX/SPX-Implementierungen akzeptieren möglicherweise die Länge von 16 Byte und die tatsächliche Länge. Wenn Sie sockaddr \_ IPX und eine hart codierte Länge von 16 Bytes verwenden, kann die Implementierung davon ausgehen, dass Sie Zugriff auf die 2 Bytes nach ihrer Struktur hat.

 



| Feld           | Wert                                    |
|-----------------|------------------------------------------|
| **Sa- \_ Familie**  | Adressfamilie AF \_ IPX in der Host Reihenfolge.    |
| **Sa \_ netnum**  | IPX-Netzwerk Bezeichner in der Netzwerk Reihenfolge |
| **Sa- \_ nodenum** | Station-Knotenadresse, rechts geleert.     |
| **Sa- \_ Socket**  | IPX-Socketnummer in der Netzwerk Reihenfolge      |



 

 

 



