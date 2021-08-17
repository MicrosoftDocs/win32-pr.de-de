---
description: Windows Sockets (Winsock) und protokollunabhängige Multipoint- und Multicastfunktionen von Transporten.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent Multicast und Multipoint in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f6e7176d9b64ac8c7ef339ee82b8252e2a0d466dd8709fa008363ec3ef954e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993620"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent Multicast und Multipoint in der SPI

So wie Windows Sockets 2 den generischen Zugriff auf die grundlegenden Datentransportfunktionen zahlreicher Transportprotokolle ermöglicht, bietet sie auch eine generische Möglichkeit, Multipoint- und Multicastfunktionen von Transporten zu verwenden, die diese Features implementieren. Zur Vereinfachung wird der Begriff *Multipoint* im Folgenden verwendet, um sowohl auf Multicast- als auch auf Multipointkommunikation zu verweisen.

Aktuelle Multipunktimplementierungen (z. B. IP-Multicast, ST-II, T.120, ATM UNI) variieren stark in Bezug darauf, wie Knoten einer Multipointsitzung beitreten, ob ein bestimmter Knoten als zentraler Knoten oder Stammknoten festgelegt ist und ob Daten zwischen allen Knoten oder nur zwischen einem Stammknoten und verschiedenen Blattknoten ausgetauscht werden. Die [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Windows Sockets 2 wird verwendet, um die Multipointattribute eines Protokolls zu deklarieren. Durch Untersuchen dieser Attribute weiß der Programmierer, welche Konventionen bei der Verwendung der entsprechenden Winsock-Funktionen zum Einrichten, Verwenden und Ablöschen von Multipointsitzungen befolgt werden müssen.

Die Features von Windows Sockets 2, die Multicast unterstützen, können wie folgt zusammengefasst werden:

-   Drei Attributbits in der [**WSAPROTOCOL \_ INFO-Struktur.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Vier Flags, die für den *dwFlags-Parameter* von [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) definiert sind
-   Eine Funktion, [**WSPJoinLeaf,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)zum Hinzufügen von Blattknoten zu einer Multipointsitzung.
-   Zwei [**WSPIoctl-Befehlscodes**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) zum Steuern des Multipoint-Loopbacks und zum Festlegen des Bereichs für Multicastübertragungen. (Letzteres entspricht dem Ip-Multicast-Time-to-Live- oder TTL-Parameter.)

> [!Note]  
> Die Einbeziehung dieser Multipointfeatures in Windows Sockets 2 schließt nicht aus, dass ein Dienstanbieter auch eine vorhandene protokollabhängige Schnittstelle unterstützt, z. B. die Deering Socket-Optionen für IP-Multicast.

 

 

 
