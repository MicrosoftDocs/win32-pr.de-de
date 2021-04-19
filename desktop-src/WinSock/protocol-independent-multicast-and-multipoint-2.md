---
description: Windows Sockets 2 bietet eine generische Methode für die Verwendung der Multipoint-und Multicast-Funktionen von Transporten.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Multicast-und Multipoint-Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348288"
---
# <a name="protocol-independent-multicast-and-multipoint"></a>Multicast-und Multipoint-Protocol-Independent

Windows Sockets 2 bietet eine generische Methode für die Verwendung der Multipoint-und Multicast-Funktionen von Transporten. Diese generische Methode implementiert diese Features genauso wie die grundlegenden Datentransport Funktionen von zahlreichen Transportprotokollen. Der Begriff "MultiPoint" wird im folgenden verwendet, um auf Multicast-und Multipoint-Kommunikationen zu verweisen.

Die aktuellen Multipoint-Implementierungen (z. b. IP-Multicast, St-II, T. 120 und ATM Uni) variieren stark. Gibt an, wie Knoten einer Multipoint-Sitzung beitreten, ob ein bestimmter Knoten als zentraler Knoten oder als Stamm Knoten festgelegt ist und ob zwischen allen Knoten oder nur zwischen einem Stamm Knoten und den verschiedenen Blattknoten zwischen den einzelnen Implementierungen Daten ausgetauscht werden. Die [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für Windows Sockets 2 wird verwendet, um die verschiedenen Multipoint-Attribute eines Protokolls zu deklarieren. Durch die Untersuchung dieser Attribute weiß der Programmierer, welche Konventionen mit den entsprechenden Windows Sockets 2-Funktionen zum Einrichten, verwenden und Beenden von Multipoint-Sitzungen befolgt werden müssen.

Im folgenden werden die Winsock-Funktionen zusammengefasst, die Multipoint unterstützen

-   Two-Attribute Bits in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur.
-   Vier Flags, die für den *dwFlags* -Parameter der [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktion definiert sind.
-   Eine Funktion, [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), zum Hinzufügen von Blattknoten zu einer Multipoint-Sitzung
-   Zwei [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Befehls Codes zum Steuern des Multipoint-Loopbacks und zum Festlegen des Bereichs für Multicast Übertragungen. (Letzteres entspricht dem IP-Multicast-"Time-to-Live"-oder "TTL"-Parameter.)

> [!Note]  
> Durch die Einbindung dieser Multipoint-Features in Windows Sockets 2 wird verhindert, dass eine Anwendung eine vorhandene Protokoll abhängige Schnittstelle verwendet, wie z. b. das Deering von Socketoptionen für IP-Multicast.

 

Ausführliche Informationen dazu, wie die verschiedenen Multipoint-Schemas charakterisiert sind und wie die entsprechenden Features von Windows Sockets 2 verwendet werden, finden Sie unter [Multipoint-und Multicast-Semantik](multipoint-and-multicast-semantics-2.md) .

 

 
