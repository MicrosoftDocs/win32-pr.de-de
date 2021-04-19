---
description: In diesem Thema werden spezifische Programmierungs Überlegungen bei der Verwendung der Peer-Infrastruktur erläutert.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Überlegungen zur Programmierung (Peer-to-Peer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367943"
---
# <a name="programming-considerations-peer-to-peer"></a>Überlegungen zur Programmierung (Peer-to-Peer)

In diesem Thema werden spezifische Programmierungs Überlegungen bei der Verwendung der Peer-Infrastruktur erläutert.

Wenn Sie Peer-Anwendungen mithilfe der Peer Infrastruktur entwickeln, müssen Sie die folgenden Programmier Überlegungen berücksichtigen:

-   IPv6

    Die Peer Infrastruktur erfordert, dass IPv6 installiert und gestartet wird, damit Peer Netzwerkanwendungen funktionieren.

-   Firewallports

    Wenn eine Firewall in einem Netzwerk verwendet wird (z. b. die IPv6-Internetverbindungs Firewall), müssen bestimmte Ports geöffnet werden, damit die Peer Infrastruktur funktioniert. Die folgenden Ports müssen geöffnet sein:

    TCP-Port 3587 für die Peer Gruppierungs Infrastruktur.

    UDP-Port 3540 für die Peer graphinginfrastruktur.

    > [!Note]  
    > Anwendungen, die die Peer-graphinginfrastruktur über TCP verwenden, wählen beim Aufrufen von [**peergraphlover**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)ihren eigenen TCP-Port aus.

     

-   Socketoption

    Wenn Sie versuchen, direkt mit anderen IPv6-Peer Knoten zu verbinden (ohne die Peer Infrastruktur), stellen Sie sicher, dass die IPv6-Schutz Ebene für die Socket-Option \_ \_ auf **Schutz \_ Ebene \_ uneingeschränkt** festgelegt ist.

-   Bandbreite

    Bei der Verwendung von PNRP kann eine Anwendung einen oder mehrere [Peernamen](peer-names.md) veröffentlichen, die aufgelöst werden können. Für jeden in PNRP registrierten Peernamen gibt es eine Erhöhung der Netzwerkbandbreite, die PNRP zum Veröffentlichen des Peer namens verwendet, und bleibt verfügbar, damit Sie von anderen Knoten aufgelöst werden kann.

    Um zu vermeiden, dass zu viel Bandbreite verwendet wird, sollten Anwendungen eine große Anzahl von Peer Namen auf einem Computer nicht registrieren. Eine Anwendung, die beispielsweise Bilder veröffentlicht, sollte keinen Peernamen für jedes Bild erstellen, sondern einen Peernamen für den Dienst erstellen, der Bilder veröffentlicht, und ein anderes Protokoll verwenden, damit Clients den Dienst nach bestimmten Bildern Abfragen können.

-   Peer Namen Registrierung

    Einige Anwendungen müssen möglicherweise denselben [Peernamen](peer-names.md) auf mehr als einem Computer registrieren. Dies geschieht in der Regel, wenn ein PeerName einer Person zugeordnet ist, die mehr als einen Computer verwendet. Eine Methode, mit der Sie denselben Peernamen auf mehreren Computern registrieren können, besteht darin, eine Peer Gruppe für die Person zu erstellen und von allen Computern aus eine Verbindung mit dieser Gruppe herzustellen. Eine andere Methode besteht darin, eine Peer Identität und einen Peernamen auf einem Computer zu erstellen, die Peer Identität von diesem Computer zu exportieren und auf anderen Computern zu importieren. Dadurch kann derselbe sichere Peer Name auf allen Computern erstellt werden, die die Peer Identität importiert haben.

 

 



