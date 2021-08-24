---
description: Die Peerinfrastruktur verwendet Ereignisse, um Anwendungen über Änderungen zu benachrichtigen, die innerhalb eines Peernetzwerks aufgetreten sind, z. B. über einen Knoten, der einem Diagramm hinzugefügt oder daraus entfernt wird.
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: Peerereignisseinfrastruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a889f59e4429e64258c047dfbf0249bb4dca125bfc3f9d659e6042dd40be9443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775950"
---
# <a name="peer-events-infrastructure"></a>Peerereignisseinfrastruktur

Die Peerinfrastruktur verwendet Ereignisse, um Anwendungen über Änderungen zu benachrichtigen, die innerhalb eines Peernetzwerks aufgetreten sind, z. B. über einen Knoten, der einem Diagramm hinzugefügt oder daraus entfernt wird. Die Peer graphing- und peer grouping-Infrastruktur verwenden die Peerereignisse-Infrastruktur.

## <a name="receiving-peer-event-notification"></a>Empfangen von Peerereignisbenachrichtigungen

Ein Peer kann sich registrieren, um Benachrichtigungen zu erhalten, wenn sich ein Attribut eines Graphen oder einer Gruppe ändert oder ein bestimmtes Peerereignis auftritt. Eine Peeranwendung ruft die [**PeerGraphRegisterEvent-**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) oder [**PeerGroupRegisterEvent-Funktion**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) auf und übergibt ein Ereignishand handle an die Peerinfrastruktur, die zuvor durch einen Aufruf von [**CreateEvent erstellt wurde.**](graphing-reference-links.md) Die Peerinfrastruktur verwendet das Handle, um einer Anwendung zu signalisieren, dass ein Peerereignis aufgetreten ist.

Die Anwendung übergibt auch eine Reihe von [**PEER \_ \_ \_ GRAPH-EREIGNISREGISTRIERUNGs-**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) oder [**PEER GROUP EVENT \_ \_ \_ REGISTRATION-Strukturen,**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) die der Peerinfrastruktur die spezifischen Peerereignisse angeben, für die die Anwendung eine Benachrichtigung angibt. Die Anwendung muss auch genau angeben, wie viele Strukturen übergeben werden.

## <a name="peer-graphing-events"></a>Peer Graphing Events

Eine Peer Graphing-Anwendung kann sich registrieren, um Benachrichtigungen für neun Peerdiagrammereignisse zu erhalten. Jedem Ereignisnamen wird PEER **\_ GRAPH EVENT \_ \_ vorangeformt,** z. B. PEER GRAPH STATUS **\_ \_ \_ CHANGED**. Sofern nicht anders angegeben, werden Informationen zu einer Änderung mit [**peerGraphGetEventData abgerufen.**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)

-   **PEER \_ GRAPH \_ EVENT \_ STATUS \_ CHANGED** gibt an, dass der Status eines Diagramms geändert wird, z. B. wenn ein Knoten mit einem Diagramm synchronisiert wurde.
-   **PEER \_ GRAPH \_ EVENT \_ PROPERTY \_ CHANGED** gibt an, dass eine Eigenschaft eines Diagramms oder einer Gruppe geändert wird, z. B. der Angezeigte Name eines Graphen geändert wurde.
    > [!Note]  
    > Die Anwendung muss [**PeerGraphGetProperties aufrufen,**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) um die geänderten Informationen zu erhalten.

     

-   **PEER \_ GRAPH \_ EVENT \_ RECORD \_ CHANGED** gibt an, dass ein Datensatz geändert wird, z. B. ein Datensatz gelöscht wird.
-   **PEER \_ GRAPH \_ EVENT \_ DIRECT \_ CONNECTION** gibt an, dass eine direkte Verbindung geändert wird, z. B. ein Knoten verbunden wurde.
-   **PEER \_ GRAPH \_ EVENT \_ NEIGHBOR \_ CONNECTION** gibt an, dass eine Verbindung mit einem benachbarten Knoten geändert wird, z. B. wenn ein Knoten verbunden wurde.
-   **PEER \_ GRAPH \_ EVENT \_ INCOMING \_ DATA** gibt an, dass Daten von einer direkten oder benachbarten Verbindung empfangen wurden.
-   **PEER \_ GRAPH \_ EVENT CONNECTION REQUIRED \_ \_ gibt** an, dass die Graphinginfrastruktur eine neue Verbindung erfordert.
    > [!Note]  
    > Ein Aufruf von [**PeerGraphConnect stellt**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) eine Verbindung mit einem neuen Knoten her. Ein Aufruf von [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) gibt keine Daten zurück.

     

-   **PEER \_ GRAPH \_ EVENT \_ NODE \_ CHANGED** gibt an, dass Informationen zum Vorhandensein von Knoten geändert werden, z. B. eine IP-Adresse geändert wurde.
-   **PEER \_ GRAPH \_ EVENT \_ SYNCHRONIZED gibt** an, dass ein bestimmter Datensatztyp synchronisiert wird.

Nachdem eine Anwendung eine Benachrichtigung erhalten hat, dass ein Peerereignis aufgetreten ist, ruft die Anwendung [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)auf und übergibt das Peerereignishand handle, das von [**PeerGraphRegisterEvent zurückgegeben wird.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) Die Peerinfrastruktur gibt einen Zeiger auf eine [**PEER \_ GRAPH EVENT \_ \_ DATA-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) zurück, die die angeforderten Daten enthält. Diese Funktion sollte aufgerufen werden, bis **PEER S NO EVENT \_ \_ \_ \_ DATA** zurückgegeben wird.

Nachdem eine Anwendung keine Peerereignisbenachrichtigung erfordert, ruft die Anwendung entweder [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)auf und übergibt das Peerereignishand handle, das von [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) zurückgegeben wurde, wenn die Anwendung registriert wurde.

## <a name="handling-graph-connection-referrals"></a>Behandeln Graph Verbindungsempfehlungen

Wenn [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) aufgerufen wird, wird der verbindende Peer über das asynchrone **PEER GRAPH EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION-Ereignis** über Erfolg oder Fehler benachrichtigt. Wenn die Verbindung aufgrund eines bestimmten Netzwerkproblemes (z. B. einer falsch konfigurierten Firewall) fehlgeschlagen ist, wird das **PEER GRAPH EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION-Ereignis** ausgelöst, bei dem der Verbindungsstatus auf PEER CONNECTION FAILED festgelegt **\_ \_ ist.**

Wenn ein Peer jedoch eine Empfehlung empfängt, wenn er versucht, eine Verbindung mit einem ausgelastet knoten herzustellen, wird die **PEER GRAPH EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION** auf dem verbindenden Peer ausgelöst, und der Verbindungsstatus ist auf PEERVERBINDUNG FEHLGESCHLAGEN **\_ \_ festgelegt.** Der verbindende Peer kann auf einen anderen Knoten verwiesen werden, der selbst ausgelastet ist und eine Empfehlung sendet, und das gleiche Ereignis und der gleiche Status werden auf dem verbindenden Peer ausgelöst. Diese Kette von Empfehlungen, die zu peer **\_ connection \_ failed-Ereignisstatus** führen, kann fortgesetzt werden, bis die maximale Anzahl von Verbindungsversuchen erschöpft ist. Der Peer verfügt nicht über einen Mechanismus, um den Unterschied zwischen einem vollständigen Verbindungsversuch und der Verbindungsempfehlung zu bestimmen.

Um dieses Problem zu beheben, sollten Entwickler erwägen, die Änderungsereignisse des Peerdiagramms zu verwenden, um zu bestimmen, ob der Verbindungsversuch erfolgreich war. Wenn das Ereignis nicht innerhalb eines bestimmten Zeitraumes empfangen wird, kann die Anwendung davon ausgehen, dass auf den verbindenden Peer verwiesen wird und dass die Peeranwendung den Verbindungsversuch als Fehler betrachten sollte.

## <a name="peer-grouping-events"></a>Peer Grouping Events

Eine Peergruppenanwendung kann sich registrieren, um Benachrichtigungen für acht Peerereignisse zu erhalten. Jedem Ereignisnamen wird **PEER \_ GROUP EVENT \_ \_ vorangeformt,** z. B. PEER GROUP EVENT STATUS **\_ \_ \_ \_ CHANGED**. Sofern nicht anders angegeben, werden Informationen zu einer Änderung mit [**peerGroupGetEventData abgerufen.**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)

-   **PEER \_ GROUP \_ EVENT STATUS CHANGED \_ \_ gibt** an, dass sich der Gruppenstatus geändert hat. Es sind zwei Statuswerte möglich: **PEER \_ GROUP STATUS \_ \_ LISTENING**, was angibt, dass die Gruppe keine Verbindungen hat und auf neue Mitglieder wartet, und **PEER GROUP STATUS HAS \_ \_ \_ CONNECTIONS**, was angibt, dass die Gruppe über mindestens eine Verbindung verfügt. Dieser Statuswert kann durch Aufrufen von [**PeerGroupGetStatus ermittelt werden,**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) nachdem dieses Ereignis ausgelöst wurde.
-   **PEER \_ GROUP \_ EVENT PROPERTY CHANGED \_ \_ gibt** an, dass die Gruppeneigenschaften vom Gruppenersteller geändert oder aktualisiert wurden.
-   **PEER \_ GROUP \_ EVENT RECORD CHANGED \_ \_ gibt** an, dass ein Datensatzvorgang ausgeführt wurde. Dieses Ereignis wird ausgelöst, wenn ein Peer, der teil der Gruppe ist, einen Datensatz veröffentlicht, aktualisiert oder löscht. Dieses Ereignis wird beispielsweise ausgelöst, wenn eine Chatanwendung eine Chatnachricht sendet.
-   **PEER \_ GROUP \_ EVENT MEMBER CHANGED \_ \_ gibt** an, dass sich der Status eines Mitglieds innerhalb der Gruppe geändert hat. Zu den Statusänderungen gehören:
    -   **PEER \_ MEMBER \_ CONNECTED**. Ein Peer wurde mit der Gruppe verbunden.
    -   **PEER \_ MEMBER \_ DISCONNECTED**. Ein Peer wurde von der Gruppe getrennt.
    -   **PEER \_ MEMBER \_ JOINED**. Neue Mitgliedschaftsinformationen wurden für einen Peer veröffentlicht.
    -   **PEER \_ MEMBER \_ AKTUALISIERT.** Ein Peer wurde mit neuen Informationen aktualisiert, z. B. einer neuen IP-Adresse.
-   **PEER \_ GROUP \_ EVENT \_ NEIGHBOR \_ CONNECTION**. Peers, die an benachbarten Verbindungen innerhalb der Gruppe teilnehmen, müssen sich für dieses Ereignis registrieren. Beachten Sie, dass die Registrierung für dieses Ereignis den Peer nicht zum Empfangen von Daten aktiviert. Die Registrierung für dieses Ereignis stellt nur dann eine Benachrichtigung sicher, wenn eine Anforderung für eine Nachbarverbindung empfangen wird.
-   **PEER \_ GROUP \_ EVENT \_ DIRECT \_ CONNECTION**. Peers, die an direkten Verbindungen innerhalb der Gruppe teilnehmen, müssen sich für dieses Ereignis registrieren. Beachten Sie, dass die Registrierung für dieses Ereignis den Peer nicht zum Empfangen von Daten aktiviert. Die Registrierung für dieses Ereignis stellt nur dann eine Benachrichtigung sicher, wenn eine Anforderung für eine direkte Verbindung empfangen wird.
-   **PEER \_ GROUP \_ EVENT \_ INCOMING \_ DATA**. Peers, die Daten über eine benachbarte oder direkte Verbindung empfangen, müssen sich für dieses Ereignis registrieren. Wenn dieses Ereignis ausgelöst wird, können die vom anderen beteiligten Peer übertragenen nicht transparenten Daten durch Aufrufen von [**PeerGroupGetEventData ermittelt werden.**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) Beachten Sie, dass der Peer zuvor für **PEER GROUP EVENT DIRECT \_ \_ \_ \_ CONNECTION** oder PEER GROUP EVENT NEIGHBOR CONNECTION registriert sein muss, um dieses **Ereignis zu \_ \_ \_ \_ empfangen.**
-   **PEER \_ FEHLER BEI \_ DER \_ \_ GRUPPENEREIGNISVERBINDUNG.** Eine Verbindung ist aus irgendeinem Grund fehlgeschlagen. Wenn dieses Ereignis ausgelöst wird, werden keine Daten bereitgestellt, und [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) sollte nicht aufgerufen werden.

Nachdem eine Anwendung eine Benachrichtigung empfangen hat, dass ein Peerereignis aufgetreten ist (mit Ausnahme von **PEER GROUP EVENT CONNECTION \_ \_ \_ \_ FAILED),** ruft die Anwendung [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)auf und übergibt das peerereignishand handle, das von [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)zurückgegeben wird. Die Peerinfrastruktur gibt einen Zeiger auf eine [**PEER \_ GROUP EVENT \_ \_ DATA-Struktur**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) zurück, die die angeforderten Daten enthält. Diese Funktion muss aufgerufen werden, bis **PEER S NO EVENT \_ \_ \_ \_ DATA** zurückgegeben wird. Wenn eine Anwendung keine Benachrichtigung mehr für ein Peerereignis erfordert, muss [**peerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent)aufgerufen werden, um das Peerereignishand handle zu übergeben, das von **PeerGroupRegisterEvent** zurückgegeben wird, wenn die Anwendung für das bestimmte Ereignis registriert wurde.

## <a name="example-of-registering-for-peer-graphing-events"></a>Beispiel für die Registrierung für Peer graphing-Ereignisse

Das folgende Codebeispiel zeigt, wie Sie sich bei den Peer Graphing-Ereignissen registrieren.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it can be called for only
//           the events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents()
{
    HPEEREVENT  g_hPeerEvent = NULL;        // The one PeerEvent handle
    HANDLE      g_hEvent = NULL;            // Handle signaled by Graphing when we have an event
    HRESULT hr = S_OK;
    PEER_GRAPH_EVENT_REGISTRATION regs[] = {
        { PEER_GRAPH_EVENT_RECORD_CHANGED, 0 },
        { PEER_GRAPH_EVENT_NODE_CHANGED,   0 },
        { PEER_GRAPH_EVENT_STATUS_CHANGED, 0 },
        { PEER_GRAPH_EVENT_DIRECT_CONNECTION, 0 },
        { PEER_GRAPH_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        wprintf(L"CreateEvent call failed.\n");
        hr = E_OUTOFMEMORY;
    }
    else
    {
        hr = PeerGraphRegisterEvent(g_hGraph, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
        if (FAILED(hr))
        {
           wprintf(L"PeerGraphRegisterEvent call failed.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            wprintf(L"Could not set up event callback.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    return hr;
}
```



 

 



