---
description: Windows Sockets 2 stellt eine generische Methode für die Verwendung der Multipoint- und Multicastfunktionen von Transporten bereit.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent Multicast und Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238949f017c2ecb910b533d12a809aa1c04af02e64d08aa0ef4e8d4f3d39b71b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857902"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Protocol-Independent Multicast und Multipoint

Windows Sockets 2 stellt eine generische Methode für die Verwendung der Multipoint- und Multicastfunktionen von Transporten bereit. Diese generische Methode implementiert diese Features genauso, wie sie den Zugriff auf die grundlegenden Datentransportfunktionen zahlreicher Transportprotokolle ermöglicht. Der Begriff Multipoint wird im Folgenden verwendet, um sowohl auf Multicast- als auch auf Multipointkommunikation zu verweisen.

Aktuelle Multipointimplementierungen (z. B. IP-Multicast, ST-II, T.120 und ATM UNI) variieren stark. Wie Knoten einer Multipointsitzung beitreten, ob ein bestimmter Knoten als zentraler Knoten oder Stammknoten festgelegt ist und ob Daten zwischen allen Knoten oder nur zwischen einem Stammknoten und den verschiedenen Blattknoten ausgetauscht werden, unterscheidet sich je nach Implementierung. Die [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für Windows Sockets 2 wird verwendet, um die verschiedenen Multipointattribute eines Protokolls zu deklarieren. Durch die Untersuchung dieser Attribute weiß der Programmierer, welche Konventionen mit den entsprechenden Windows Sockets 2-Funktionen zum Einrichten, Verwenden und Abbruch von Multipointsitzungen zu befolgen sind.

Im Folgenden werden winsock-Features zusammengefasst, die Multipoint unterstützen:

-   Bits mit zwei Attributen in der [**WSAPROTOCOL \_ INFO-Struktur.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Vier Flags, die für den *dwFlags-Parameter* der [**WSASocket-Funktion definiert**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) sind.
-   Eine Funktion, [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)zum Hinzufügen von Blattknoten zu einer Multipointsitzung
-   Zwei [**WSAIoctl-Befehlscodes**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) zum Steuern des Multipoint-Loopbacks und Zum Einrichten des Bereichs für Multicastübertragungen. (Letzteres entspricht dem IP-Multicast-Parameter "Time-to-Live" oder "TTL".)

> [!Note]  
> Die Einbeziehung dieser Multipointfunktionen in Windows Sockets 2 schließt nicht aus, dass eine Anwendung eine vorhandene protokollabhängige Schnittstelle verwendet, z. B. die Deering Socket-Optionen für IP-Multicast.

 

Unter [Multipoint- und Multicastsemantik](multipoint-and-multicast-semantics-2.md) finden Sie ausführliche Informationen dazu, wie die verschiedenen Multipointschemas gekennzeichnet sind und wie die anwendbaren Features von Windows Sockets 2 verwendet werden.

 

 
