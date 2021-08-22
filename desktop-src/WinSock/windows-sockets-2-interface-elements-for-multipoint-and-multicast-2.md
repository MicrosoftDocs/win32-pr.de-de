---
description: Windows Sockets 2-Schnittstellenelemente (Winsock) für Multipoint und Multicast.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Windows Sockets 2-Schnittstellenelemente für Multipoint und Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf2422d8171a041f75ba8abed6ea490982187af3affb3d3c3d1349984210ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558852"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Windows Sockets 2-Schnittstellenelemente für Multipoint und Multicast

Die Mechanismen, die in Windows Sockets 2 für die Nutzung von Multipointfunktionen integriert wurden, können wie folgt zusammengefasst werden:

-   Drei Attributbits in der [**WSAPROTOCOL \_ INFO-Struktur.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Vier Flags, die für den *dwFlags-Parameter* von [**WSASocket definiert sind.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
-   Eine Funktion, [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)zum Hinzufügen von Blattknoten zu einer Multipointsitzung.
-   Zwei [**WSAIoctl-Befehlscodes**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) zum Steuern des Multipoint-Loopbacks und des Bereichs von Multicastübertragungen.

In den folgenden Abschnitten werden diese Schnittstellenelemente ausführlicher beschrieben:

-   [Semantik zum Verbinden von Mehrpunktblättern](semantics-for-joining-multipoint-leaves-2.md)
-   [Unterstützung dieser Erweiterungen durch vorhandene Multipointprotokolle](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
