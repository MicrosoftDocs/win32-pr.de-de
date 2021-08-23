---
description: IP-Multicast fällt in die Kategorie der Nicht-Rooted-Datenebene und der Nicht-Root-Steuerungsebene.
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: IP-Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b80441826f490fedc3dac3dba405ddd0d9f09d57bfd0243a66cae320c76b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051498"
---
# <a name="ip-multicast"></a>IP-Multicast

IP-Multicast fällt in die Kategorie der Nicht-Rooted-Datenebene und der Nicht-Root-Steuerungsebene. Alle Anwendungen spielen eine Blattrolle. Derzeit verwenden die meisten IP-Multicastimplementierungen eine Reihe von Socketoptionen, die steve Deering der Internet Engineering Task Force (IETF) vorgeschlagen hat. Fünf Vorgänge werden somit verfügbar gemacht:

-   IP \_ MULTICAST \_ TTL – Legt die Livezeit fest und steuert den Bereich einer Multicastsitzung.
-   IP \_ MULTICAST \_ IF– Bestimmt die Schnittstelle, die für Multicasting verwendet werden soll.
-   IP \_ ADD \_ MEMBERSHI – Fügt einer angegebenen Multicastsitzung bei.
-   IP \_ DROP \_ MEMBERSHIP– Löscht eine Multicastsitzung.
-   IP \_ MULTICAST \_ LOOP – Steuert das Loopback des Multicastdatenverkehrs.

Das Festlegen der Livezeit für einen IP-Multicastsocket wird direkt der Verwendung des SIO MULTICAST SCOPE-Befehlscodes für \_ \_ [**WSAIoctl zu .**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)

Die Methode zum Bestimmen der IP-Schnittstelle, die für Multicasting verwendet werden soll, ist über eine TCP/IP-spezifische Socketoption, wie im Windows Sockets 2-Protocol-Specific Anhang beschrieben. Die restlichen drei Vorgänge werden gut mit der Windows Sockets 2-Semantik abgedeckt, die hier beschrieben wird.

Die Anwendung würde Sockets mit \_ blatt-/d-Blattflags in \_ [**WSASocket öffnen.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) wird verwendet, um sich selbst zu einer Multicastgruppe auf der Standardschnittstelle hinzuzufügen, die für Multicastvorgänge festgelegt ist. Wenn das Flag in **WSAJoinLeaf** angibt, dass dieser Socket nur ein Absender ist, ist der Joinvorgang im Wesentlichen kein Vorgang, und es müssen keine IGMP-Nachrichten gesendet werden. Andernfalls wird ein IGMP-Paket an den Router gesendet, um anzugeben, dass interesse am Empfang von Paketen besteht, die an die angegebene Multicastadresse gesendet werden. Da die Anwendung spezielle Blatt-/D-Blattsockets erstellt hat, die nur zum Ausführen von Multicast verwendet werden, wird die standardmäßige \_ \_ [**closesocket-Funktion**](/windows/desktop/api/winsock/nf-winsock-closesocket) verwendet, um die Multicastsitzung zu beenden. Der SIO MULTIPOINT LOOPBACK-Befehlscode für \_ \_ [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) bietet einen generischen Steuerungsmechanismus, mit dem bestimmt wird, ob daten, die an einen Blattsocket in einem nicht entfernten Multipointschema gesendet werden, auch auf demselben Socket empfangen werden \_ können.

> [!Note]  
> Die Winsock-Version der OPTION IP MULTICAST LOOP ist semantisch anders als die UNIX der \_ \_ IP \_ MULTICAST \_ LOOP-Option:

 

-   In Winsock gilt die OPTION IP \_ MULTICAST \_ LOOP nur für den Empfangspfad.
-   In der UNIX gilt die OPTION IP \_ MULTICAST \_ LOOP für den Sendepfad.

Beispielsweise verbinden Anwendungen ON und OFF (die einfacher nachverfolgt werden können als X und Y) dieselbe Gruppe auf derselben Schnittstelle. application ON legt die OPTION IP \_ MULTICAST LOOP auf fest, application OFF deaktiviert die \_ OPTION IP \_ MULTICAST \_ LOOP. Wenn ON und OFF Winsock-Anwendungen sind, kann OFF an ON senden, ON kann jedoch nicht an OFF gesendet werden. Wenn ON und OFF hingegen UNIX sind, kann ON an OFF senden, OFF kann jedoch nicht an ON senden.

 

 



