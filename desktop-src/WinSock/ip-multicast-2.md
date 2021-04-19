---
description: IP-Multicast fällt in die Kategorie der nicht stammenden Datenebene und der nicht-Stamm Steuerungsebene.
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: IP-Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf9469822ae974b7c616b7904f9dc7120682acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353066"
---
# <a name="ip-multicast"></a>IP-Multicast

IP-Multicast fällt in die Kategorie der nicht stammenden Datenebene und der nicht-Stamm Steuerungsebene. Alle Anwendungen spielen eine Blatt Rolle. Derzeit verwenden die meisten IP-Multicast Implementierungen eine Reihe von Socketoptionen, die von Steve Deering an die Internet Engineering Task Force (IETF) vorgeschlagen werden. So werden fünf Vorgänge verfügbar gemacht:

-   IP- \_ Multicast \_ -TTL – legt den Gültigkeitsbereich einer Multicast Sitzung auf den Gültigkeitsbereich fest.
-   IP- \_ Multicast \_ , wenn – die Schnittstelle bestimmt, die für Multicasting verwendet werden soll.
-   IP \_ Add \_ Membership – verbindet eine angegebene Multicast Sitzung.
-   IP- \_ Drop \_ Membership – löscht eine Multicast Sitzung.
-   IP- \_ Multicast \_ Schleife – steuert die Loopbacks von Multicast Datenverkehr.

Das Festlegen der Gültigkeitsdauer für einen IP-Multicast-Socket erfolgt direkt unter Verwendung des Befehls Codes für die Verwendung des Befehls "sio \_ Multicast \_ Scope" für [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl).

Die Methode zum Bestimmen der IP-Schnittstelle, die für Multicasting verwendet werden soll, ist eine TCP/IP-spezifische Socketoption, wie im Windows Sockets 2-Protocol-Specific Anhang beschrieben. Die verbleibenden drei Vorgänge werden mit der hier beschriebenen Semantik für Windows Sockets 2 gut abgedeckt.

Die Anwendung würde Sockets mit c-Blatt- \_ /d- \_ endflags in [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)öffnen. Dabei würde [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) verwendet werden, um sich selbst zu einer Multicast Gruppe auf der Standardschnittstelle hinzuzufügen, die für Multicast Vorgänge festgelegt ist. Wenn das Flag in **wsajoinleaf** angibt, dass es sich bei diesem Socket nur um einen Absender handelt, ist der Joinvorgang im Grunde ein No-op-Vorgang, und es müssen keine IGMP-Nachrichten gesendet werden. Andernfalls wird ein IGMP-Paket an den Router gesendet, um die Interessen beim Empfangen von Paketen anzugeben, die an die angegebene Multicast Adresse gesendet werden. Da die Anwendung spezielle c- \_ Blatt/d- \_ Blatt Sockets nur zum Ausführen von Multicast verwendet, wird die standardmäßige [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion verwendet, um aus der Multicast Sitzung zu löschen. Der "sio \_ Multipoint \_ Loopback Command Code" für [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) stellt einen generischen Steuerungsmechanismus bereit, mit dem bestimmt werden kann, ob Daten, die auf einem d- \_ Blatt-Socket in einem nicht stammenden Multipoint-Schema gesendet werden, auch auf demselben Socket empfangen

> [!Note]  
> Die Winsock-Version der IP- \_ Multicast \_ Schleifen Option unterscheidet sich semantisch von der UNIX-Version der IP- \_ Multicast \_ Schleifen Option:

 

-   In Winsock gilt die IP- \_ Multicast- \_ Schleifen Option nur für den Empfangs Pfad.
-   In der UNIX-Version wird die IP- \_ Multicast \_ Schleifen Option auf den Sende Pfad angewendet.

Beispielsweise können Anwendungen, die ein-und ausschalten (die leichter nachverfolgt werden können als X und Y), derselben Gruppe auf derselben Schnittstelle beitreten. Anwendung on legt die IP- \_ Multicast \_ Schleifen Option auf fest, die Anwendung off legt die Option IP- \_ Multicast \_ Schleife auf OFF fest. Wenn das on und Off Winsock-Anwendungen ist, kann off an on senden, aber on kann nicht an off gesendet werden. Wenn im Gegensatz dazu UNIX-Anwendungen auf on und Off ausgeführt werden, kann on auf Off senden, aber off kann nicht an on senden.

 

 



