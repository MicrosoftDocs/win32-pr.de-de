---
description: In einigen Fällen können Sockets, die einer Multipoint-Sitzung beitreten, einige Unterschiede im Verhalten von Punkt-zu-Punkt-Sockets aufweisen.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Bits für wsasocket markieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372815"
---
# <a name="flag-bits-for-wsasocket"></a>Bits für wsasocket markieren

In einigen Fällen können Sockets, die einer Multipoint-Sitzung beitreten, einige Unterschiede im Verhalten von Punkt-zu-Punkt-Sockets aufweisen. So kann z. b. ein d- \_ Blatt-Socket in einem Daten Ebenen Schema, das nur Informationen an den d-Stamm \_ Teilnehmer sendet. Dies führt dazu, dass die Anwendung in der Lage ist, die beabsichtigte Verwendung eines socketcovorfalls mit ihrer Erstellung anzugeben. Dies erfolgt über vier-Flag-Bits, die im *dwFlags* -Parameter auf [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)festgelegt werden können:

-   WSA \_ Flag \_ -Multipoint- \_ C \_ -Stamm für die Erstellung eines als C-Stamm fungierenden Sockets \_ und nur zulässig, wenn im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag eine Stamm Steuerungsebene angegeben wird.
-   WSA \_ Flag \_ \_ \_ für das Multipoint-C-Blatt, für die Erstellung eines als C-Blatt fungierenden Sockets \_ und nur zulässig, wenn die XP1- \_ Unterstützung \_ für Multipoint im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag angegeben wird.
-   WSA \_ Flag \_ Multipoint \_ D \_ root für die Erstellung eines als D-Stamm fungierenden Sockets \_ und nur zulässig, wenn im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag eine Datenebene mit Stamms angegeben wird.
-   WSA \_ Flag \_ -Multipoint \_ -D- \_ Blatt für die Erstellung eines als D-Blatt fungierenden Sockets \_ und nur zulässig, wenn die XP1- \_ Unterstützung von \_ Multipoint im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag angegeben wird.

Beachten Sie, dass beim Erstellen eines Multipoint-Sockets genau eines der beiden Flags der Steuerungsebene und eines der beiden Flags für die Datenebene im *dwFlags* -Parameter von [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)festgelegt werden muss. Daher sind die vier Möglichkeiten zum Erstellen von Multipoint-Sockets:

-   "c \_ root/d \_ root"
-   "c \_ root/d- \_ Blatt"
-   "c- \_ Blatt/d-Stamm \_ "
-   "c- \_ Blatt/d \_ Blatt"

 

 
