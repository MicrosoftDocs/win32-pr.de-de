---
description: Die IPX-Adressfamilie definiert die Adressierungsstruktur für Protokolle, die IPX-Standardsocket-Adressierung verwenden. Für diese Transporte besteht eine Endpunktadresse aus einer Netzwerknummer, einer Knotenadresse und einer Socketnummer.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: AF_IPX-Adressfamilie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3915eefab8e6fc6c18cf4e2b81835b8c6821d0cdd65f5683f509504d4d2c24bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112803"
---
# <a name="af_ipx-address-family"></a>\_AF-IPX-Adressfamilie

Die IPX-Adressfamilie definiert die Adressierungsstruktur für Protokolle, die IPX-Standardsocket-Adressierung verwenden. Für diese Transporte besteht eine Endpunktadresse aus einer Netzwerknummer, einer Knotenadresse und einer Socketnummer.

Die Netzwerknummer ist eine Verwaltungsdomäne und benennt in der Regel ein einzelnes Ethernet- oder Tokenringsegment. Die Knotennummer ist die physische Adresse einer Station. Die Kombination aus "net" und "node" bildet eine eindeutige Stationsadresse, von der angenommen wird, dass sie weltweit eindeutig ist. Netz- und Knotennummern werden in ASCII-Text entweder in Block- oder Gestrichelter Notation dargestellt als: "0101a040,00001b498765" oder "01-01-a0-40,00-00-1b-49-87-65". Führende Nullen müssen nicht vorhanden sein.

Die IPX-Socketnummer ist eine Netzwerk-/Transportdienstnummer ähnlich wie eine TCP-Portnummer und darf nicht mit dem Winsock-Socketdeskriptor verwechselt werden. IPX-Socketnummern sind global für die Endstation und können nicht an bestimmte Netzwerk-/Knotenadressen gebunden werden. Wenn die Endstation beispielsweise über zwei Netzwerkschnittstellenkarten verfügt, kann ein gebundener Socket auf beiden Karten senden und empfangen. Datagrammsockets würden insbesondere Broadcast-Datagramme auf beiden Karten empfangen.

> [!Caution]  
> SOCKADDR IPX ist 14 Byte lang und kürzer als die \_ 16-Byte-Sockaddr-Referenzstruktur. [](sockaddr-2.md) IPX/SPX-Implementierungen akzeptieren möglicherweise die Länge von 16 Byte sowie die echte Länge. Wenn Sie SOCKADDR IPX und eine hart codierte Länge von 16 Bytes verwenden, kann die Implementierung davon ausgehen, dass sie Zugriff auf die 2 Bytes hat, die Ihrer Struktur \_ folgen.

 



| Feld           | Wert                                    |
|-----------------|------------------------------------------|
| **sa \_ family**  | Adressfamilie AF \_ IPX in Host reihenfolge.    |
| **Sa \_ netnum**  | IPX-Netzwerkbezeichner in Netzwerk reihenfolge. |
| **\_Sa-Nodenum** | Adresse des Stationsknotens, rechts geleert.     |
| **\_Sa-Socket**  | IPX-Socketnummer in Netzwerk reihenfolge.      |



 

 

 



