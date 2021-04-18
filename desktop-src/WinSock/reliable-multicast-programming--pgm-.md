---
description: Dieser Abschnitt beschreibt die pragmatische allgemeine Multicast-Protokoll Implementierung (PGM) in Windows, häufig als zuverlässiges Multicast bezeichnet. Zuverlässiges Multicast wird durch Windows Sockets in Windows Server 2003 und höher implementiert.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Zuverlässige Multicast Programmierung (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343441"
---
# <a name="reliable-multicast-programming-pgm"></a>Zuverlässige Multicast Programmierung (PGM)

Dieser Abschnitt beschreibt die pragmatische allgemeine Multicast-Protokoll Implementierung (PGM) in Windows, häufig als zuverlässiges Multicast bezeichnet. Zuverlässiges Multicast wird durch Windows Sockets in Windows Server 2003 und höher implementiert.

**Windows XP:** PGM wird nur unterstützt, wenn Microsoft Message Queuing (MSMQ) 3,0 installiert ist.

PGM ist ein zuverlässiges und skalierbares Multicast Protokoll, das es Empfängern ermöglicht, Verluste zu erkennen, eine erneute Übertragung verlorener Daten anzufordern oder eine Anwendung mit nicht BEHEB barem Verlust zu benachrichtigen. Bei PGM handelt es sich um ein zuverlässiges Empfänger Protokoll. Dies bedeutet, dass der Empfänger dafür verantwortlich ist, sicherzustellen, dass alle Daten empfangen werden, sodass er den Absender der Empfangs Verantwortung übernimmt.

PGM eignet sich für Anwendungen, die eine duplizierte Multicast-Datenübermittlung von mehreren Quellen an mehrere Empfänger benötigen. PGM unterstützt weder eine bestätigte Übermittlung noch die Reihenfolge von Paketen mehrerer Absender.

Weitere Informationen zu PGM finden Sie 3208 unter [www.ietf.org](https://www.ietf.org/).

In diesem Abschnitt wird beschrieben, wie Sie zuverlässiges Multicast unter Windows verwenden. In den folgenden Themen werden die verschiedenen Aspekte der Erstellung einer zuverlässigen Multicast Anwendung mithilfe von Windows Sockets erläutert:

-   [PGM-Absender und-Empfänger](pgm-senders-and-receivers.md)
-   [PGM-Sender Optionen](pgm-sender-options.md)
-   [Senden und empfangen von PGM-Daten](sending-and-receiving-pgm-data.md)
-   [Multihosting und PGM](multihoming-and-pgm.md)
-   [PGM-Socketoptionen](pgm-socket-options.md)

 

 



