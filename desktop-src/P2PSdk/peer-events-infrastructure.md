---
description: Die Peer Infrastruktur verwendet Ereignisse, um Anwendungen über Änderungen zu benachrichtigen, die in einem Peer Netzwerk aufgetreten sind, z. b. ein Knoten, der einem Diagramm hinzugefügt oder daraus entfernt wird.
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: Peer Ereignis Infrastruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6347ad6a7dd0cf2fae4a0aa623bfda48ab0aa9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363475"
---
# <a name="peer-events-infrastructure"></a>Peer Ereignis Infrastruktur

Die Peer Infrastruktur verwendet Ereignisse, um Anwendungen über Änderungen zu benachrichtigen, die in einem Peer Netzwerk aufgetreten sind, z. b. ein Knoten, der einem Diagramm hinzugefügt oder daraus entfernt wird. Die Infrastrukturen der Peer-und Peer Gruppierung verwenden die Infrastruktur der Peer Ereignisse.

## <a name="receiving-peer-event-notification"></a>Empfangen von Peer Ereignis Benachrichtigungen

Ein Peer kann sich registrieren, um eine Benachrichtigung zu erhalten, wenn sich ein Attribut eines Diagramms oder einer Gruppe ändert oder ein bestimmtes Peer Ereignis auftritt. Eine Peer Anwendung ruft die [**peergraphregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) -Funktion oder die [**peergroupregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) -Funktion auf und übergibt ein Ereignis Handle an die Peer Infrastruktur, die zuvor durch einen Aufruf von " [**kreateevent**](graphing-reference-links.md)" erstellt wurde. Die Peer Infrastruktur verwendet das Handle, um einer Anwendung zu signalisieren, dass ein Peer Ereignis aufgetreten ist.

Die Anwendung übergibt auch eine Reihe von [**Peer \_ Graph \_ - \_ Ereignisregistrierungs**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) -oder [**Peer \_ Gruppen- \_ Ereignis \_ Registrierungs**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) Strukturen, die der Peer Infrastruktur die spezifischen Peer Ereignisse anzeigen, für die die Anwendung eine Benachrichtigung anfordert. Die Anwendung muss auch genau angeben, wie viele Strukturen übermittelt werden.

## <a name="peer-graphing-events"></a>Peer graphingereignisse

Eine Peer graphanwendung kann sich registrieren, um eine Benachrichtigung für 9 Peer Graph-Ereignisse zu erhalten. Jedem Ereignis Namen wird ein **Peer Graph- \_ \_ \_ Ereignis** vorangestellt, z. b. der **Status des Peer \_ Diagramms \_ \_**. Sofern nicht anders angegeben, werden die Informationen zu einer Änderung mithilfe von " [**Peer Diagramm geteventdata**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)" abgerufen.

-   **Peer \_ Der Graph- \_ Ereignis \_ Status wurde \_ geändert** und zeigt an, dass der Status eines Diagramms geändert wird, z. b. Wenn ein Knoten mit einem Diagramm synchronisiert wurde.
-   **Peer \_ \_ \_ \_ Geänderte Diagramm Ereignis Eigenschaft** gibt an, dass eine Eigenschaft eines Diagramms oder einer Gruppe geändert wird, z. b. wenn sich der Anzeige Name eines Diagramms geändert hat.
    > [!Note]  
    > Die Anwendung muss " [**Peer graphgetproperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) " aufrufen, um die geänderten Informationen zu erhalten.

     

-   **Peer \_ Diagramm \_ Ereignis \_ Daten Satz \_ geändert** gibt an, dass ein Datensatz geändert wird, z. b. Wenn ein Datensatz gelöscht wird.
-   **Peer \_ Die \_ direkte Graph-Ereignis \_ \_ Verbindung** gibt an, dass eine direkte Verbindung geändert wird, z. b. Wenn ein Knoten eine Verbindung hergestellt hat.
-   **Peer \_ Eine Graph- \_ Ereignis \_ Nachbar \_ Verbindung** gibt an, dass eine Verbindung mit einem Nachbar Knoten geändert wird, z. b. Wenn ein Knoten eine Verbindung hergestellt hat.
-   **Peer \_ \_ \_ Eingehende \_ Daten des Diagramm Ereignisses** zeigen an, dass Daten von einer direkten oder benachbarten Verbindung empfangen wurden.
-   **Peer \_ Graph- \_ Ereignis \_ Verbindung \_ erforderlich** gibt an, dass die graphinginfrastruktur eine neue Verbindung erfordert.
    > [!Note]  
    > Bei einem [**Peer-graphconnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) -Befehl wird eine Verbindung mit einem neuen Knoten hergestellt. Ein Aufrufen von " [**Peer Diagramm geteventdata**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) " gibt keine Daten zurück.

     

-   **Peer \_ Der \_ \_ \_ geänderte Diagramm Ereignis Knoten** zeigt an, dass die Informationen zur Knoten Präsenz geändert werden, z. b. Wenn eine IP-Adresse geändert wurde.
-   **Peer \_ \_ \_ Synchronisierung des Diagramm Ereignisses** gibt an, dass ein bestimmter Daten Recordtyp synchronisiert ist.

Nachdem eine Anwendung eine Benachrichtigung erhalten hat, dass ein Peer Ereignis aufgetreten ist, ruft die Anwendung [**peergraphgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)auf und übergibt das von [**peergraphregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)zurückgegebene Peer Ereignis handle. Die Peer Infrastruktur gibt einen Zeiger auf eine [**Peer \_ Graph- \_ Ereignis \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) Struktur zurück, die die angeforderten Daten enthält. Diese Funktion sollte aufgerufen werden, bis **Peer \_ S \_ keine \_ Ereignis \_ Daten** zurückgibt.

Wenn eine Anwendung keine Peer Ereignis Benachrichtigung erfordert, ruft die Anwendung entweder [**peergraphunregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)auf und übergibt das Peer Ereignis handle, das von [**peergraphregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) zurückgegeben wurde, als die Anwendung registriert ist.

## <a name="handling-graph-connection-referrals"></a>Umgang mit Graph-Verbindungs Referenzen

Wenn [**peergraphconnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) aufgerufen wird, wird der Verbindungs Peer über das asynchrone **Peer \_ Graph- \_ Ereignis Nachbar- \_ \_ Verbindungs** Ereignis über Erfolg oder Fehler benachrichtigt. Wenn bei der Verbindung aufgrund eines bestimmten Netzwerk Problems (z. b. einer falsch konfigurierten Firewall) ein Fehler aufgetreten ist, wird das Ereignis Nachbar-Verbindungs Ereignis des **Peer \_ Diagramms \_ \_ \_** ausgelöst, wobei der Verbindungsstatus auf **Peer \_ Verbindung ist \_ fehlgeschlagen**.

Wenn ein Peer aber einen Verweis erhält, wenn er versucht, eine Verbindung mit einem ausgelasteten Knoten herzustellen, wird die **Peer \_ Graph- \_ \_ Nachbar \_ Verbindung** auf dem Verbindungs Peer ausgelöst, wobei der Verbindungsstatus auf **Peer \_ Verbindung ist \_ fehlgeschlagen** ist. Der Verbindungs Peer kann auf einen anderen Knoten verwiesen werden, der selbst ausgelastet ist und einen Verweis senden kann. das gleiche Ereignis und der gleiche Status werden auf dem Verbindungs Peer ausgelöst. Diese Verweiskette, die zu Fehlern bei der **Peer \_ Verbindungs \_ fehl** Veranstaltung führt, kann fortgesetzt werden, bis die maximale Anzahl von Verbindungs versuchen erschöpft ist. Der Peer verfügt über keinen Mechanismus, um den Unterschied zwischen einem vollen Verbindungsversuch und dem Verbindungs Verweis zu ermitteln.

Um dieses Problem zu beheben, sollten Entwickler in Erwägung gezogen werden, die Peer Graph-Status Änderungs Ereignisse zu verwenden, um zu bestimmen, ob der Verbindungsversuch fehlschlägt. Wenn das Ereignis nicht innerhalb eines bestimmten Zeitraums empfangen wird, kann die Anwendung davon ausgehen, dass auf den Verbindungs-Peer verwiesen wird und dass die Peer Anwendung den Verbindungsversuch als Fehler betrachtet.

## <a name="peer-grouping-events"></a>Peer Gruppierungs Ereignisse

Eine Peer Gruppierungs Anwendung kann sich registrieren, um Benachrichtigungen für 8-Peer-Ereignisse zu empfangen. Jedem Ereignis Namen wird ein **Peer \_ Gruppen \_ Ereignis \_** vorangestellt, z. b. hat sich der **Peer \_ Gruppen \_ Ereignis \_ Status \_ geändert**. Sofern nicht anders angegeben, werden Informationen zu einer Änderung mithilfe von " [**Peer groupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)" abgerufen.

-   **Peer \_ Der Gruppen \_ Ereignis \_ Status wurde \_ geändert** und zeigt an, dass sich der Gruppen Status geändert hat. Es gibt zwei mögliche Statuswerte: **Peer \_ Gruppen \_ Status \_** Überwachung. Dies deutet darauf hin, dass die Gruppe keine Verbindungen hat und auf neue Mitglieder wartet. der **Peer \_ Gruppen \_ Status weist \_ Verbindungen** auf, was darauf hinweist, dass die Gruppe über mindestens eine Verbindung verfügt. Dieser Statuswert kann abgerufen werden, indem [**peergroupgetstatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) aufgerufen wird, nachdem dieses Ereignis ausgelöst wurde.
-   **Peer \_ \_ \_ \_ Geänderte Gruppen Ereignis Eigenschaft** gibt an, dass die Gruppen Eigenschaften vom Ersteller der Gruppe geändert oder aktualisiert wurden.
-   **Peer \_ Gruppen \_ Ereignis \_ Daten Satz \_ geändert** gibt an, dass ein Datensatz-Vorgang ausgeführt wurde. Dieses Ereignis wird ausgelöst, wenn ein Peer, der Teil der Gruppe ist, einen Datensatz veröffentlicht, aktualisiert oder löscht. Dieses Ereignis wird z. b. ausgelöst, wenn eine Chat-Anwendung eine Chat Nachricht sendet.
-   **Peer \_ Gruppen \_ \_ Ereignismember \_ geändert** gibt an, dass sich der Status eines Mitglieds innerhalb der Gruppe geändert hat. Zu den Status Änderungen gehören:
    -   **Peer \_ Mitglied \_ verbunden**. Ein Peer hat eine Verbindung mit der Gruppe hergestellt.
    -   **Peer \_ Member \_ getrennt**. Ein Peer hat die Verbindung mit der Gruppe getrennt.
    -   **Peer \_ Member \_** verknüpft. Für einen Peer wurden neue Mitgliedschafts Informationen veröffentlicht.
    -   **Peer \_ der Member wurde \_ aktualisiert**. Ein Peer wurde mit neuen Informationen aktualisiert, z. b. einer neuen IP-Adresse.
-   **Peer \_ Gruppieren der \_ Ereignis \_ Nachbar \_ Verbindung**. Peers, die an Nachbar Verbindungen innerhalb der Gruppe teilnehmen, müssen sich für dieses Ereignis registrieren. Beachten Sie, dass die Registrierung für dieses Ereignis den Peer nicht zum Empfangen von Daten ermöglicht. durch die Registrierung für dieses Ereignis wird nur dann eine Benachrichtigung sichergestellt, wenn eine Verbindung mit einer Nachbar Verbindung empfangen wird.
-   **Peer \_ Gruppen \_ Ereignis- \_ direkt \_ Verbindung**. Peers, die an direkten Verbindungen innerhalb der Gruppe teilnehmen, müssen sich für dieses Ereignis registrieren. Beachten Sie, dass die Registrierung für dieses Ereignis den Peer nicht zum Empfangen von Daten ermöglicht. die Registrierung für dieses Ereignis gewährleistet nur eine Benachrichtigung, wenn eine Anforderung für eine direkte Verbindung empfangen wird.
-   **Peer \_ Gruppieren \_ \_ eingehender \_ Daten von Ereignissen**. Peers, die Daten über eine Nachbar-oder Direktverbindung empfangen, müssen sich für dieses Ereignis registrieren. Wenn dieses Ereignis ausgelöst wird, können die nicht transparenten Daten, die vom anderen teilnehmenden Peer übertragen werden, durch Aufrufen von [**peergroupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)abgerufen werden. Beachten Sie, dass für das Empfangen dieses Ereignisses der Peer zuvor für die **Peer \_ Gruppe \_ Ereignis \_ Direct- \_ Verbindung** oder **Peer \_ Group \_ Event NEIGHBOR- \_ \_ Verbindung** registriert sein muss.
-   **Peer \_ Fehler \_ bei der Gruppen Ereignis \_ Verbindung \_**. Eine Verbindung ist aus irgendeinem Grund fehlgeschlagen. Wenn dieses Ereignis ausgelöst wird, werden keine Daten bereitgestellt, und " [**Peer groupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) " sollte nicht aufgerufen werden.

Nachdem eine Anwendung benachrichtigt wurde, dass ein Peer Ereignis aufgetreten ist (mit Ausnahme der **Peer \_ Gruppen- \_ Ereignis \_ Verbindung \_**), ruft die Anwendung [**peergroupgeteventdata**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)auf und übergibt das Peer Ereignis handle, das von [**peergroupregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)zurückgegeben wurde. Die Peer Infrastruktur gibt einen Zeiger auf eine [**Peer \_ Gruppen- \_ Ereignis \_ Daten**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) Struktur zurück, die die angeforderten Daten enthält. Diese Funktion muss aufgerufen werden, bis **Peer \_ S \_ keine \_ Ereignis \_ Daten** zurückgibt. Wenn eine Anwendung keine Benachrichtigung mehr für ein Peer Ereignis benötigt, muss ein-Befehl an [**peergroupunregisterevent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent)gesendet werden. dabei wird das von **peergroupregisterevent** zurückgegebene Peer Ereignis Handle übergeben, wenn die Anwendung für das jeweilige Ereignis registriert ist.

## <a name="example-of-registering-for-peer-graphing-events"></a>Beispiel für das Registrieren von Peer-graphingereignissen

Im folgenden Codebeispiel wird gezeigt, wie Sie sich bei den Peer-graphingereignissen registrieren.


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



 

 



