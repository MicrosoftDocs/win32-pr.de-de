---
description: Windows Sockets (Winsock) und Protokoll unabhängige Multipoint-und Multicast-Funktionen von Transporten.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent Multicast und Multipoint in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131176"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent Multicast und Multipoint in der SPI

Ebenso wie Windows Sockets 2 ermöglicht, dass die grundlegenden Datentransport Funktionen von zahlreichen Transportprotokollen auf generische Weise aufgerufen werden können, bietet es auch eine generische Möglichkeit, Multipoint-und Multicast-Funktionen von Transporten zu verwenden, die diese Features implementieren. Um dies zu vereinfachen, wird im folgenden der Begriff *Multipoint* verwendet, um auf Multicast-und Multipoint-Kommunikation zu verweisen.

Aktuelle Multipoint-Implementierungen (z. b. IP-Multicast, St-II, T. 120, ATM Uni) variieren in Bezug darauf, wie Knoten mit einer Multipoint-Sitzung verknüpft werden, ob ein bestimmter Knoten als zentraler Knoten oder Stamm Knoten festgelegt ist und ob zwischen allen Knoten oder nur zwischen einem Stamm Knoten und verschiedenen Blattknoten Daten ausgetauscht werden. Die [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur von Windows Sockets 2 wird zum Deklarieren der Multipoint-Attribute eines Protokolls verwendet. Durch die Untersuchung dieser Attribute weiß der Programmierer, welche Konventionen bei der Einrichtung, Verwendung und Löschung von Multipoint-Sitzungen bei der Verwendung der anwendbaren Winsock-Funktionen befolgt werden müssen.

Die Features von Windows Sockets 2, die Multicast unterstützen, können wie folgt zusammengefasst werden:

-   Drei Attribut Bits in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur.
-   Vier Flags, die für den *dwFlags* -Parameter von [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) definiert sind
-   Eine Funktion, [**wspjoinleaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), zum Hinzufügen von Blattknoten zu einer Multipoint-Sitzung.
-   Zwei [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) -Befehls Codes zum Steuern des Multipoint-Loopbacks und zum Festlegen des Bereichs für Multicast Übertragungen. (Letzteres entspricht dem IP-Multicast-"Time-to-Live"-oder "TTL"-Parameter.)

> [!Note]  
> Durch die Einbindung dieser Multipoint-Features in Windows Sockets 2 wird verhindert, dass ein Dienstanbieter auch eine vorhandene Protokoll abhängige Schnittstelle unterstützt, wie z. b. das Deering von Socketoptionen für IP-Multicast.

 

 

 
