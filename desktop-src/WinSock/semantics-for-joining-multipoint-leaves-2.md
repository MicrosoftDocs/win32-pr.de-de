---
description: In den folgenden Fällen wird ein Multipoint-Socket häufig beschrieben, indem seine Rolle in einer der beiden Ebenen (Steuerelement oder Daten) definiert wird.
ms.assetid: 34f639e2-9363-4f3f-a8de-b7c5d12618c9
title: Semantik für das beitreten von Multipoint-Blättern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df12683838fbad89f717b08d7a19802f24556761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343439"
---
# <a name="semantics-for-joining-multipoint-leaves"></a>Semantik für das beitreten von Multipoint-Blättern

In den folgenden Fällen wird ein Multipoint-Socket häufig beschrieben, indem seine Rolle in einer der beiden Ebenen (Steuerelement oder Daten) definiert wird. Es sollte erkannt werden, dass derselbe Socket eine Rolle in der anderen Ebene aufweist, aber dies wird nicht erwähnt, um die Verweise kurz zu halten. Wenn z. b. ein Verweis auf einen "c-Stamm \_ Socket" erfolgt, kann dies entweder ein c-Stamm \_ /d-Stamm \_ oder ein c- \_ root/d- \_ Blatt-Socket sein.

In den Schemas der Ebene der Steuerungsebene werden einer Multipoint-Sitzung auf zwei verschiedene Arten neue Blattknoten hinzugefügt. In der ersten Methode verwendet der Stamm [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) , um eine Verbindung mit einem Blattknoten zu initiieren und ihn zu einem Teilnehmer einzuladen. Auf dem Blattknoten muss die Peer Anwendung einen c \_ -Blatt Socket erstellt haben und [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , Sie in den Abhör Modus einzustellen. Der Blattknoten empfängt \_ bei Einladung zum Beitritt zur Sitzung eine FD-Annahme-Anzeige und signalisiert seine Bereitschaft, durch Aufrufen von [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)zu beitreten. Die Stamm Anwendung empfängt dann eine FD- \_ Verbindungsanzeige,  wenn der Joinvorgang abgeschlossen wurde.

In der zweiten Methode werden die Rollen im Grunde umgekehrt. Die Stamm Anwendung erstellt einen c \_ -root-Socket und legt ihn auf den Abhör Modus fest. Ein Blattknoten, der an der Sitzung teilnehmen möchte, erstellt einen c \_ -Blatt Socket und verwendet [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) , um die Verbindung zu initiieren und die Anforderung anzufordern. Die Stamm Anwendung empfängt FD \_ Accept, wenn eine eingehende Zutritt-Anforderung eingeht, und gibt den Blattknoten durch Aufrufen von [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)an. Der Blattknoten empfängt FD \_ Connect, wenn er zugelassen wurde.

In einer nicht-Stamm Steuerungsebene, bei der alle Knoten c \_ -Blatt sind, wird das [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) -Element verwendet, um die Einbindung eines Knotens in eine vorhandene Multipoint-Sitzung zu initiieren. Eine FD \_ -Verbindungsanzeige wird bereitgestellt, wenn der Join abgeschlossen wurde und der zurückgegebene socketdeskriptor in der Multipoint-Sitzung verwendet werden kann. Im Fall von IP-Multicast entspricht dies der IP-Option zum \_ Hinzufügen von \_ Mitgliedschafts Sockets.

(Leser, die mit der Verwendung des Verbindungs losen UDP-Protokolls von IP-Multicast vertraut sind, sind möglicherweise von der hier dargestellten Verbindungs orientierten Semantik betroffen. Insbesondere das Konzept der Verwendung von [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) für einen UDP-Socket und das warten auf eine FD- \_ Verbindungsanzeige kann beunruhigend sein. Es gibt jedoch einen umfassenden Präzedenzfall für das Anwenden der Verbindungs orientierten Semantik auf verbindungslose Protokolle. Es ist zulässig und manchmal nützlich, z. b. um die Standard- [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion für einen UDP-Socket aufzurufen. Das allgemeine Ergebnis der Anwendung der Verbindungs orientierten Semantik auf verbindungslose Sockets ist eine Einschränkung darin, wie solche Sockets verwendet werden können, und dies ist auch hier auch der Fall. Ein UDP-Socket, der in **wsajoinleaf** verwendet wird, weist bestimmte Einschränkungen auf und wartet auf eine FD- \_ Verbindungsanzeige (die in diesem Fall einfach anzeigt, dass die entsprechende IGMP-Nachricht gesendet wurde) ist eine solche Einschränkung.)

Aus diesem Grund gibt es drei Instanzen, in denen eine Anwendung [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) als fungiert:

-   Multipoint-Stamm und einladen eines neuen Blatts zum Beitreten zur Sitzung
-   Blatt, das eine Zutritt-Anforderung an eine Stamm-Multipoint-Sitzung sendet
-   Blatt Suche nach Zutritt zu einer nicht stammenden Multipoint-Sitzung (z. b. IP-Multicast)

 

 



