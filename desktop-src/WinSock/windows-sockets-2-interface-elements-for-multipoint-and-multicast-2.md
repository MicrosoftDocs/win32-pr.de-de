---
description: Winsock-Schnittstellen Elemente (Windows Sockets 2) für Multipoint und Multicast.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Windows Sockets 2-Schnittstellen Elemente für Multipoint und Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360118"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Windows Sockets 2-Schnittstellen Elemente für Multipoint und Multicast

Die Mechanismen, die für die Verwendung von Multipoint-Funktionen in Windows Sockets 2 integriert wurden, können wie folgt zusammengefasst werden:

-   Drei Attribut Bits in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur.
-   Vier Flags, die für den *dwFlags* -Parameter von [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)definiert sind.
-   Eine Funktion, [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), zum Hinzufügen von Blattknoten zu einer Multipoint-Sitzung.
-   Zwei [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Befehls Codes zum Steuern des Multipoint-Loopbacks und des Bereichs von Multicast Übertragungen.

In den folgenden Abschnitten werden diese Schnittstellen Elemente ausführlicher beschrieben:

-   [Semantik für das beitreten von Multipoint-Blättern](semantics-for-joining-multipoint-leaves-2.md)
-   [Unterstützung für diese Erweiterungen durch vorhandene Multipoint-Protokolle](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
