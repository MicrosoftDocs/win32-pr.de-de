---
description: Beim Arbeiten mit Peerdiagrammen müssen Funktionen in einer bestimmten Reihenfolge aufgerufen werden. Der Fluss der Aufrufe hängt davon ab, ob Sie ein Peerdiagramm erstellen oder öffnen. In diesem Thema wird der Fluss von Funktionsaufrufen in einer einfachen Peergraphanwendung beschrieben.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Arbeiten mit Diagrammen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdb4a40f1c086ada772239798990c3dfb24326b3e70bd768a95eacc35ee384b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034030"
---
# <a name="working-with-graphs"></a>Arbeiten mit Diagrammen

Beim Arbeiten mit Peerdiagrammen müssen Funktionen in einer bestimmten Reihenfolge aufgerufen werden. Der Fluss der Aufrufe hängt davon ab, ob Sie ein Peerdiagramm erstellen oder öffnen. In diesem Thema wird der Fluss von Funktionsaufrufen in einer einfachen Peergraphanwendung beschrieben.

## <a name="starting-up-a-graph"></a>Starten eines Graph

Bevor eine Anwendung eine Funktion in der Peer Graphing-API aufruft, muss [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) aufgerufen werden, um die Peer Graphing-API für eine Anwendung zu initialisieren, und dann die unterstützte Version festlegen.

## <a name="creating-a-peer-graph"></a>Erstellen eines Peer-Graph

Das folgende Verfahren identifiziert den Fluss der Aufrufe zum Erstellen eines Peerdiagramms.

> [!IMPORTANT]
> Nur ein Peer sollte [**PeerGraphCreate aufrufen.**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) Alle anderen Peers sollten [**PeerGraphOpen aufrufen.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) Mehrere Aufrufe von **PeerGraphErkennen** eines Graphen ungültig.

 

-   Erstellen Sie ein Peerdiagramm. Rufen Sie [**PeerGraphErzeugen auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)
-   Registrieren Sie sich für Peerereignisse. Rufen Sie [**PeerGraphRegisterEvent auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Weitere Informationen zum Registrieren für Peerereignisse finden Sie unter [Ereignisinfrastruktur.](peer-events-infrastructure.md)

     

-   Lauschen Sie auf Verbindungen mit einem Peerdiagramm. Rufen Sie [**PeerGraphListen auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)
-   Führen Sie anwendungsabhängige Funktionen für den Rest der Ausführungszeit aus, z. B. Verarbeiten von Peerereignissen und Arbeiten mit Verbindungen.
-   Schließen Sie die Verbindung mit einem Peerdiagramm. Rufen Sie [**PeerGraphClose auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

## <a name="opening-a-peer-graph"></a>Öffnen eines Peer-Graph

Der Fluss von Funktionsaufrufen zum Öffnen eines Peerdiagramms hängt vom Rückgabewert des Aufrufs von [**PeerGraphOpen ab.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) Die wichtigsten Werte sind **S \_ OK** und **PEER S DATA \_ \_ \_ CREATED,** die in den folgenden Abschnitten dieses Themas erläutert werden.

> [!Note]  
> Wenn bei einem Aufruf von [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) **weder S \_ OK** noch **PEER S DATA \_ \_ \_ CREATED** zurückgegeben wird, behandeln Sie den Fehler.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Wenn PeerGraphOpen S \_ OK zurückgibt

Wenn ein Aufruf von [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) **S \_ OK** zurückgibt, wurden ein Peerdiagramm und eine vorhandene Datenbank geöffnet. Das folgende Verfahren identifiziert, was Sie tun können, um ein Peerdiagramm zu öffnen, wenn ein Aufruf von **PeerGraphOpen** **S OK \_ zurückgibt.**

-   Registrieren Sie sich für Peerereignisse. Rufen Sie [**PeerGraphRegisterEvent auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Weitere Informationen zum Registrieren für Ereignisse finden Sie unter [Ereignisinfrastruktur.](peer-events-infrastructure.md)

     

-   Suchen Sie einen Knoten. Dies ist ein Prozess, der außerhalb der Peer graphing-Infrastruktur mithilfe einer von Ihnen identifizierten Methode oder Anwendung ausgeführt wird. Die Peer Graphing-API bietet keinen bestimmten Mechanismus zum Suchen eines anfänglichen Graphknotens, mit dem eine Verbindung hergestellt werden soll. Eine Anwendung muss einen anderen Mechanismus verwenden, z. B. die [PNRP-API (Peer Name Resolution Protocol),](pnrp-namespace-provider-api.md) um den ersten Knoten zu finden.
-   Wenn ein Knoten gefunden wird, stellen Sie eine Verbindung mit ihm herstellen. Rufen [**Sie PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)auf, und rufen Sie [**dann PeerGraphListen auf,**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) um auf Verbindungen mit dem Peerdiagramm zu lauschen.
    > [!Note]  
    > Wenn kein Knoten gefunden wird, rufen Sie [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) und [**PeerGraphListen nicht auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Führen Sie anwendungsabhängige Funktionen für den Rest der Ausführungszeit aus, z. B. Verarbeiten von Peerereignissen und Arbeiten mit Verbindungen, je nachdem, ob der Knoten mit dem Peerdiagramm verbunden ist oder nicht. Beispielsweise kann die Anwendung ein Timeout festlegen oder regelmäßig eine Ermittlung für einen aktiven Knoten im Graphen durchführen.
-   Schließen Sie die Verbindung mit dem Peerdiagramm. Rufen Sie [**PeerGraphClose auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Wenn PeerGraphOpen PEER \_ S \_ DATA CREATED \_ zurückgibt

Wenn [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) **PEER S DATA \_ \_ \_ CREATED** zurückgibt, bedeutet dies, dass keine vorhandene Datenbank für einen Peergraphen gefunden wird, eine neue Datenbank erstellt wird, und dies ist das erste Mal, wenn sie geöffnet wird. Um ein Peerdiagramm zu verwenden oder zu lauschen, muss ein Peer mit einem Peerdiagramm verbunden und mit diesem synchronisiert werden.

Das folgende Verfahren identifiziert, was Sie tun können, um ein Peerdiagramm zu öffnen, wenn ein Aufruf von [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) **PEER S DATA CREATED \_ \_ \_ zurückgibt.**

-   Öffnen Sie ein Peerdiagramm. Rufen Sie [**PeerGraphOpen auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)
-   Registrieren Sie sich für Peerereignisse. Rufen Sie [**PeerGraphRegisterEvent auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)
    > [!Note]  
    > Weitere Informationen zum Registrieren für Peerereignisse finden Sie unter [Ereignisinfrastruktur.](peer-events-infrastructure.md)

     

-   Suchen Sie einen Knoten. Dies ist ein Prozess, der außerhalb der Peer graphing-Infrastruktur mithilfe einer von Ihnen identifizierten Methode oder Anwendung ausgeführt wird. Die Peer Graphing-API bietet keinen bestimmten Mechanismus zum Suchen eines anfänglichen Graphknotens, mit dem eine Verbindung hergestellt werden soll. Eine Anwendung muss einen anderen Mechanismus verwenden, z. B. die [PNRP-API (Peer Name Resolution Protocol),](pnrp-namespace-provider-api.md) um den ersten Knoten zu finden.
-   Wenn ein Knoten gefunden wird, stellen Sie eine Verbindung mit ihm herstellen. Rufen [**Sie PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)auf, und rufen Sie [**dann PeerGraphListen auf,**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) um auf Verbindungen mit dem Peerdiagramm zu lauschen.
    > [!Note]  
    > Wenn kein Knoten gefunden wird, rufen Sie [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) und [**PeerGraphListen nicht auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Führen Sie anwendungsabhängige Funktionen für den Rest der Ausführungszeit aus, z. B. Verarbeiten von Peerereignissen und Arbeiten mit Verbindungen, je nachdem, ob der Knoten mit dem Peerdiagramm verbunden ist oder nicht. Beispielsweise kann die Anwendung ein Timeout festlegen oder regelmäßig eine Ermittlung für einen aktiven Knoten im Graphen durchführen.
-   Schließen Sie die Verbindung mit dem Peerdiagramm. Rufen Sie [**PeerGraphClose auf.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

 

 



