---
description: In diesem Abschnitt wird die PGM-Multicastprotokollimplementierungen (PGM) in Windows beschrieben, die häufig als zuverlässiges Multicast bezeichnet werden. Reliable Multicast wird über Windows Sockets in Windows Server 2003 und höher implementiert.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Zuverlässige Multicastprogrammierung (Reliable Multicast Programming, PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c34365bdc8db553d24182fcb193dc03177627ccf9b00a03f309ab4cf7bbe01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559952"
---
# <a name="reliable-multicast-programming-pgm"></a>Zuverlässige Multicastprogrammierung (Reliable Multicast Programming, PGM)

In diesem Abschnitt wird die PGM-Multicastprotokollimplementierungen (PGM) in Windows beschrieben, die häufig als zuverlässiges Multicast bezeichnet werden. Reliable Multicast wird über Windows Sockets in Windows Server 2003 und höher implementiert.

**Windows XP:** PGM wird nur unterstützt, wenn Microsoft Message Queuing (MSMQ) 3.0 installiert ist.

PGM ist ein zuverlässiges und skalierbares Multicastprotokoll, mit dem Empfänger Verlust erkennen, eine erneute Übertragung verlorener Daten anfordern oder eine Anwendung über nicht behebbaren Verlust benachrichtigen können. PGM ist ein zuverlässiges Empfängerprotokoll, was bedeutet, dass der Empfänger dafür verantwortlich ist, sicherzustellen, dass alle Daten empfangen werden, wodurch der Absender der Empfangsverantwortlichkeit entbindet wird.

PGM eignet sich für Anwendungen, die eine duplizierte, kostenlose Multicastdatenübermittlung aus mehreren Quellen an mehrere Empfänger erfordern. PGM unterstützt weder die bestätigten Übermittlungen noch die Reihenfolge von Paketen von mehreren Absendern.

Weitere Informationen zu PGM finden Sie unter RFC 3208 unter [www.ietf.org](https://www.ietf.org/).

In diesem Abschnitt wird beschrieben, wie Zuverlässiges Multicast auf Windows verwendet wird. In den folgenden Themen werden die verschiedenen Aspekte der Erstellung einer zuverlässigen Multicastanwendung mit Windows Sockets erläutert:

-   [PGM-Absender und -Empfänger](pgm-senders-and-receivers.md)
-   [Optionen für PGM-Absender](pgm-sender-options.md)
-   [Senden und Empfangen von PGM-Daten](sending-and-receiving-pgm-data.md)
-   [Multihoming und PGM](multihoming-and-pgm.md)
-   [PGM-Socketoptionen](pgm-socket-options.md)

 

 



