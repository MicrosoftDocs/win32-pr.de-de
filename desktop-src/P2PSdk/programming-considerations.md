---
description: In diesem Thema werden bestimmte Überlegungen zur Programmierung bei der Verwendung der Peerinfrastruktur erläutert.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Überlegungen zur Programmierung (Peer-zu-Peer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d5af967503c216422e3a12572aeeaf91d751473f88d8589c2e125894721b41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518060"
---
# <a name="programming-considerations-peer-to-peer"></a>Überlegungen zur Programmierung (Peer-zu-Peer)

In diesem Thema werden bestimmte Überlegungen zur Programmierung bei der Verwendung der Peerinfrastruktur erläutert.

Wenn Sie die Peerinfrastruktur zum Entwickeln von Peeranwendungen verwenden, müssen Sie die folgenden Überlegungen zur Programmierung berücksichtigen:

-   IPv6

    Die Peerinfrastruktur erfordert, dass IPv6 installiert und gestartet wird, damit Peernetzwerkanwendungen funktionieren können.

-   Firewallports

    Wenn eine Firewall in einem Netzwerk verwendet wird (z. B. die IPv6-Internetverbindungsfirewall), müssen bestimmte Ports geöffnet werden, damit die Peerinfrastruktur funktioniert. Die folgenden Ports müssen geöffnet sein:

    TCP-Port 3587 für die Peergruppeninfrastruktur.

    UDP-Port 3540 für die Peer graphing-Infrastruktur.

    > [!Note]  
    > Anwendungen, die die Peer graphing-Infrastruktur über TCP verwenden, wählen beim Aufrufen von [**PeerGraphListen ihren eigenen TCP-Port aus.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Socketoption

    Wenn Sie versuchen, eine direkte Verbindung mit anderen IPv6-Peerknoten herzustellen (ohne die Peerinfrastruktur zu verwenden), stellen Sie sicher, dass die Socketoption IPV6 PROTECTION LEVEL auf \_ PROTECTION LEVEL UNRESTRICTED festgelegt \_ **\_ \_ ist.**

-   Bandbreite

    Bei Verwendung von PNRP kann eine Anwendung einen oder mehrere [Peernamen](peer-names.md) veröffentlichen, die aufgelöst werden können. Für jeden Peernamen, der bei PNRP registriert ist, erhöht sich die Netzwerkbandbreite, die PNRP zum Veröffentlichen des Peernamens verwendet, und hält ihn für die Lösung durch andere Knoten verfügbar.

    Um zu verhindern, dass zu viel Bandbreite verwendet wird, sollten Anwendungen vermeiden, eine große Anzahl von Peernamen auf einem Computer zu registrieren. Beispielsweise sollte eine Anwendung, die Bilder veröffentlicht, keinen Peernamen für jedes Bild erstellen, sondern einen Peernamen für den Dienst erstellen, der Bilder veröffentlicht, und ein anderes Protokoll für Clients verwenden, um den Dienst nach bestimmten Bildern abfragt.

-   Peernamenregistrierung

    Einige Anwendungen müssen möglicherweise den gleichen Peernamen [auf](peer-names.md) mehr als einem Computer registrieren. Dies geschieht in der Regel, wenn ein Peername einer Person zugeordnet ist, die mehrere Computer verwendet. Eine Methode, mit der Sie den gleichen Peernamen auf mehreren Computern registrieren können, ist das Erstellen einer Peergruppe für die Person und das Herstellen einer Verbindung mit dieser Gruppe von allen Computern aus. Eine andere Methode besteht in der Erstellung einer Peeridentität und eines Peernamens auf einem Computer, dem Exportieren der Peeridentität von diesem Computer und dem Importieren auf anderen Computern. Dadurch kann derselbe sichere Peername auf allen Computern erstellt werden, die die Peeridentität importiert haben.

 

 



