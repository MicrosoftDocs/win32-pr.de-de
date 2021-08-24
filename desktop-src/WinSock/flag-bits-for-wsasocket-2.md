---
description: In einigen Fällen können Sockets, die mit einer Multipointsitzung verbunden sind, einige Unterschiede im Verhalten von Point-to-Point-Sockets haben.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Flagbits für WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bbe8a282fe0255e3efd9889216b7d44aee2a41feedb611ba5c2b1d38bae68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132473"
---
# <a name="flag-bits-for-wsasocket"></a>Flagbits für WSASocket

In einigen Fällen können Sockets, die mit einer Multipointsitzung verbunden sind, einige Unterschiede im Verhalten von Point-to-Point-Sockets haben. Beispielsweise kann ein Blattsocket in einem Schema mit Root-Datenebene nur Informationen \_ an den \_ d-Stammteilnehmer senden. Dies führt dazu, dass die Anwendung in der Lage sein muss, die beabsichtigte Verwendung eines Sockets im Zusammenhang mit der Erstellung anzugeben. Dies erfolgt über Bits mit vier Flags, die im *dwFlags-Parameter* auf [**WSASocket festgelegt werden können:**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)

-   WSA FLAG MULTIPOINT C ROOT für die Erstellung eines Sockets, der als c-Stamm verwendet wird, und nur zulässig, wenn im entsprechenden \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ INFO-Eintrag**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) eine Root-Steuerungsebene angegeben ist.
-   WSA FLAG MULTIPOINT C LEAF für die Erstellung eines Sockets, der als Blatt c verwendet wird, und nur zulässig, wenn \_ \_ \_ \_ \_ XP1 SUPPORT MULTIPOINT im entsprechenden \_ \_ [**WSAPROTOCOL \_ INFO-Eintrag angegeben**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) ist.
-   WSA FLAG MULTIPOINT D ROOT für die Erstellung eines Sockets, der als d-Stamm verwendet wird, und nur zulässig, wenn im entsprechenden \_ \_ \_ \_ \_ [**WSAPROTOCOL \_ INFO-Eintrag**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) eine Root-Datenebene angegeben ist.
-   WSA FLAG MULTIPOINT D LEAF, für die Erstellung eines Sockets, der als Blatt d verwendet wird, und nur zulässig, wenn \_ \_ \_ \_ \_ XP1 SUPPORT MULTIPOINT im entsprechenden \_ \_ [**WSAPROTOCOL \_ INFO-Eintrag angegeben**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) ist.

Beachten Sie, dass beim Erstellen eines Multipointsockets genau eines der beiden Flags der Steuerungsebene und eines der beiden Datenebenenflags im *dwFlags-Parameter* von [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)festgelegt werden muss. Daher sind die vier Möglichkeiten zum Erstellen von Multipointsockets:

-   "c \_ root/d \_ root"
-   "c \_ root/d \_ leaf"
-   "c \_ leaf/d \_ root"
-   "c \_ leaf /d \_ leaf"

 

 
