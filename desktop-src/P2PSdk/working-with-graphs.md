---
description: Beim Arbeiten mit Peer Diagrammen müssen Funktionen in einer bestimmten Reihenfolge aufgerufen werden. Der Ablauf von Aufrufen hängt davon ab, ob Sie ein Peer Diagramm erstellen oder öffnen. In diesem Thema wird der Ablauf von Funktionsaufrufen in einer einfachen Peer Graph-Anwendung beschrieben.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Arbeiten mit Diagrammen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4328b7a0109139421cf03c72a7228a3dc17e375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349417"
---
# <a name="working-with-graphs"></a>Arbeiten mit Diagrammen

Beim Arbeiten mit Peer Diagrammen müssen Funktionen in einer bestimmten Reihenfolge aufgerufen werden. Der Ablauf von Aufrufen hängt davon ab, ob Sie ein Peer Diagramm erstellen oder öffnen. In diesem Thema wird der Ablauf von Funktionsaufrufen in einer einfachen Peer Graph-Anwendung beschrieben.

## <a name="starting-up-a-graph"></a>Starten eines Diagramms

Bevor eine Anwendung eine Funktion in der Peer graphende-API aufruft, muss [**peergraphstartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) aufgerufen werden, um die Peer graphapi für eine Anwendung zu initialisieren und dann die unterstützte Version festzulegen.

## <a name="creating-a-peer-graph"></a>Erstellen eines Peer Diagramms

Im folgenden Verfahren wird der Fluss von Aufrufen zum Erstellen eines Peer Diagramms identifiziert.

> [!IMPORTANT]
> [**Peergraphcreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)sollte nur von einem Peer aufgerufen werden. Alle anderen Peers sollten [**peergraphopen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)aufruft. Mehrere Aufrufe von " **Peer Graph Create** " machen ein Diagramm ungültig.

 

-   Erstellen Sie ein Peer Diagramm. Rufen Sie " [**Peer graphcreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)" auf.
-   Registrieren Sie sich für Peer Ereignisse. Aufrufen von " [**Peer Diagramm Register Event**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)".
    > [!Note]  
    > Weitere Informationen zum Registrieren von Peer Ereignissen finden Sie unter [Events Infrastructure](peer-events-infrastructure.md).

     

-   Lauschen Sie auf Verbindungen mit einem Peer Diagramm. Nennen Sie " [**Peer Diagramm**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)".
-   Ausführen von Anwendungs abhängigen Funktionen für die restliche Dauer der Laufzeit, z. b. verarbeiten von Peer Ereignissen und arbeiten mit Verbindungen.
-   Schließen Sie die Verbindung mit einem Peer Diagramm. Ruft " [**Peer graphclose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)" auf.

## <a name="opening-a-peer-graph"></a>Öffnen eines Peer Diagramms

Der Ablauf von Funktionsaufrufen zum Öffnen eines Peer Diagramms hängt vom Rückgabewert des Aufrufs von [**peergraphopen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)ab. Die wichtigsten Werte sind **S \_ OK** und **Peer S- \_ \_ Daten \_**, die in den folgenden Abschnitten dieses Themas erläutert werden.

> [!Note]  
> Wenn bei einem [**peergraphopen-peergraphopen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) -Befehl keine **S \_ OK** -oder **Peer \_ S- \_ Daten \_** zurückgegeben werden, behandeln Sie den Fehler.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Wenn "Peer Diagramm Open" S \_ OK zurückgibt

Wenn ein Aufruf von [**peergraphopen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) **S \_ OK** zurückgibt, wurden ein Peer Diagramm und eine vorhandene Datenbank geöffnet. Das folgende Verfahren zeigt, wie Sie ein Peer Diagramm öffnen können, wenn ein Aufruf von **peergraphopen** **S \_ OK** zurückgibt.

-   Registrieren Sie sich für Peer Ereignisse. Aufrufen von " [**Peer Diagramm Register Event**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)".
    > [!Note]  
    > Weitere Informationen zum Registrieren von Ereignissen finden Sie unter [Events Infrastructure](peer-events-infrastructure.md).

     

-   Suchen Sie einen Knoten. Dabei handelt es sich um einen Prozess, der außerhalb der Peer Diagramm Infrastruktur durchgeführt wird, indem eine Methode oder eine Anwendung verwendet wird, die Sie identifizieren. Die Peer Graph-API bietet keinen spezifischen Mechanismus zum Suchen eines ersten Diagramm Knotens, mit dem eine Verbindung hergestellt werden soll. Eine Anwendung muss einen anderen Mechanismus, wie z. b. die API des [Peer Name Resolution-Protokolls (PNRP)](pnrp-namespace-provider-api.md) , verwenden, um den ersten Knoten zu suchen.
-   Wenn ein Knoten gefunden wird, stellen Sie eine Verbindung mit ihm her. Nennen Sie [**peergraphconnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect), und klicken Sie dann auf [**peergraphlauschen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) , um Verbindungen mit dem Peer Diagramm zu überwachen.
    > [!Note]  
    > Wenn ein Knoten nicht gefunden wird, dürfen Sie nicht " [**Peer Diagramm Connect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) " und " [**Peer Diagramm**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)" anrufen.

     

-   Ausführen von Anwendungs abhängigen Funktionen für die restliche Dauer der Laufzeit, z. b. verarbeiten von Peer Ereignissen und arbeiten mit Verbindungen, je nachdem, ob der Knoten mit dem peergraph verbunden ist oder nicht. Die Anwendung kann z. b. ein Timeout oder eine regelmäßige Ermittlung für einen aktiven Knoten im Diagramm auswählen.
-   Schließen Sie die Verbindung mit dem Peer Diagramm. Ruft " [**Peer graphclose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)" auf.

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Wenn peergraphopen Peer S-Daten zurückgibt, die \_ \_ \_ erstellt wurden

Wenn [**peergraphopen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) **Peer- \_ S- \_ Daten \_** zurückgibt, bedeutet dies, dass eine vorhandene Datenbank für ein Peer Diagramm nicht gefunden wird, eine neue Datenbank erstellt wird und diese zum ersten Mal geöffnet wird. Um ein Peer Diagramm zu verwenden oder zu lauschen, muss ein Peer mit einem Peer Diagramm verbunden und synchronisiert werden.

Das folgende Verfahren zeigt, wie Sie ein Peer Diagramm öffnen können, wenn ein Aufruf von [**peergraphopen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) **Peer- \_ S \_ - \_ Daten** zurückgibt.

-   Öffnen Sie ein Peer Diagramm. Ruft " [**Peer Diagramm Open**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)" auf.
-   Registrieren Sie sich für Peer Ereignisse. Aufrufen von " [**Peer Diagramm Register Event**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)".
    > [!Note]  
    > Weitere Informationen zum Registrieren von Peer Ereignissen finden Sie unter [Events Infrastructure](peer-events-infrastructure.md).

     

-   Suchen Sie einen Knoten. Dabei handelt es sich um einen Prozess, der außerhalb der Peer Diagramm Infrastruktur durchgeführt wird, indem eine Methode oder eine Anwendung verwendet wird, die Sie identifizieren. Die Peer Graph-API bietet keinen spezifischen Mechanismus zum Suchen eines ersten Diagramm Knotens, mit dem eine Verbindung hergestellt werden soll. Eine Anwendung muss einen anderen Mechanismus, wie z. b. die API des [Peer Name Resolution-Protokolls (PNRP)](pnrp-namespace-provider-api.md) , verwenden, um den ersten Knoten zu suchen.
-   Wenn ein Knoten gefunden wird, stellen Sie eine Verbindung mit ihm her. Nennen Sie [**peergraphconnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect), und klicken Sie dann auf [**peergraphlauschen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) , um Verbindungen mit dem Peer Diagramm zu überwachen.
    > [!Note]  
    > Wenn ein Knoten nicht gefunden wird, dürfen Sie nicht " [**Peer Diagramm Connect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) " und " [**Peer Diagramm**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)" anrufen.

     

-   Ausführen von Anwendungs abhängigen Funktionen für die restliche Dauer der Laufzeit, z. b. verarbeiten von Peer Ereignissen und arbeiten mit Verbindungen, je nachdem, ob der Knoten mit dem peergraph verbunden ist oder nicht. Die Anwendung kann z. b. ein Timeout oder eine regelmäßige Ermittlung für einen aktiven Knoten im Diagramm auswählen.
-   Schließen Sie die Verbindung mit dem Peer Diagramm. Ruft " [**Peer graphclose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)" auf.

 

 



