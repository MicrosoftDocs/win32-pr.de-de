---
description: Multipoint-socketattribute in Windows Sockets (Winsock).
ms.assetid: f6e779c6-dd9d-470e-aad9-715b69ad8c5f
title: Multipoint-socketattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da67fd40c7c3bc7f1e9dbff22a3fef6cdaee4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214588"
---
# <a name="multipoint-socket-attributes"></a>Multipoint-socketattribute

In einigen Fällen können Sockets, die mit einer Multipoint-Sitzung verknüpft sind, einige Verhaltensunterschiede von Punkt-zu-Punkt-Sockets aufweisen. So kann z. b. ein d- \_ Blatt-Socket in einem Daten Ebenen Schema, das nur Informationen an den d-Stamm \_ Teilnehmer sendet. Dies führt dazu, dass der Client in der Lage sein muss, die beabsichtigte Verwendung eines socketcovorfalls mit seiner Erstellung anzugeben. Dies erfolgt über vier Multipoint-Attributflags, die über den *dwFlags* -Parameter in [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)festgelegt werden können:

-   WSA \_ Flag \_ -Multipoint- \_ C \_ -Stamm für die Erstellung eines als C-Stamm fungierenden Sockets \_ und nur zulässig, wenn im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag eine Stamm Steuerungsebene angegeben wird.
-   WSA \_ Flag \_ \_ \_ für das Multipoint-C-Blatt, für die Erstellung eines als C-Blatt fungierenden Sockets \_ und nur zulässig, wenn die XP1- \_ Unterstützung \_ für Multipoint im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag angegeben wird.
-   WSA \_ Flag \_ Multipoint \_ D \_ root für die Erstellung eines als D-Stamm fungierenden Sockets \_ und nur zulässig, wenn im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag eine Datenebene mit Stamms angegeben wird.
-   WSA \_ Flag \_ -Multipoint \_ -D- \_ Blatt für die Erstellung eines als D-Blatt fungierenden Sockets \_ und nur zulässig, wenn die XP1- \_ Unterstützung von \_ Multipoint im entsprechenden [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Eintrag angegeben wird.

Beim Erstellen eines Multipoint-Sockets muss genau eines der beiden Flags der Steuerungsebene festgelegt werden, und eines der beiden datenebenenflags muss im *dwFlags* -Parameter von [**wspsocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)festgelegt werden. Daher sind die vier Möglichkeiten zum Erstellen von Multipoint-Sockets: "c \_ root/d \_ root", "c \_ root/d \_ Blatt", "c \_ leaf/d \_ root" oder "c \_ leaf/d \_ Leaf".

 

 
