---
description: Die Peer Graphing- und Peer Grouping-Infrastruktur ermöglichen Anwendungen, eine direkte Verbindung mit einem Knoten (Graphing) oder Mitglied (Gruppierung) herzustellen und dann Daten direkt mit dem Knoten zu austauschen. Diese Verbindung wird als direkte Verbindung bezeichnet.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Direkte Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f06fde65cf7597ccbec7f2968dbbf7662b4a6491ae59e6aa66b8baa587dc1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011628"
---
# <a name="direct-connections"></a>Direkte Verbindungen

Die Peer Graphing- und Peer Grouping-Infrastruktur ermöglichen Anwendungen, eine direkte Verbindung mit einem Knoten (Graphing) oder Mitglied (Gruppierung) herzustellen und dann Daten direkt mit dem Knoten zu austauschen. Diese Verbindung wird als direkte **Verbindung bezeichnet.**

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>Direkte Verbindungen mithilfe der Peer graphing-Infrastruktur

Bevor eine direkte Verbindung zwischen zwei Knoten in einem Diagramm hergestellt werden kann, müssen beide Knoten für das **PEER GRAPH EVENT DIRECT \_ \_ \_ \_ CONNECTION-Ereignis registriert** werden. Um Daten über eine direkte Verbindung zu empfangen, müssen die Knoten auch für das **PEER GRAPH EVENT INCOMING \_ \_ \_ \_ DATA-Ereignis registriert** werden.

**PEER \_ GRAPH \_ EVENT \_ DIRECT \_ CONNECTION** ist ein Ereignis, das eine Anwendung benachrichtigt, ob ein direkter Verbindungsversuch erfolgreich ist oder nicht. Der tatsächliche Erfolgs- oder Fehlerstatus eines Aufrufs von [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) wird in der [**PEER GRAPH EVENT \_ \_ \_ DATA-Struktur**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) zurückgegeben.

Um eine direkte Verbindung zu erstellen, ruft eine Anwendung [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)auf und übergibt dann ein Handle an das Diagramm, einen Zeiger auf die Identität des anderen Knotens, der an der Verbindung beteiligt ist, und einen Zeiger auf eine IPv6-Adressstruktur für den beteiligten Knoten. Die Knotenidentität und die IPv6-Adresse, die im Aufruf von **PeerGraphOpenDirectConnection** angegeben werden, müssen für das **PEER GRAPH EVENT INCOMING \_ \_ \_ \_ DATA-Ereignis** registriert werden, oder es können keine Daten empfangen werden, die von einem aufrufenden Peer gesendet werden. Bei erfolgreicher Überprüfung **gibt PeerGraphOpenDirectConnection** eine 64-Bit-Verbindungs-ID zurück. Der Peer muss jedoch auf das PEER **\_ GROUP EVENT DIRECT \_ \_ \_ CONNECTION-Ereignis** warten, bevor die ID der direkten Verbindung als gültig identifiziert werden kann.

Nachdem eine Verbindung hergestellt und eine gültige Verbindungs-ID bestätigt wurde, kann eine Anwendung [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) aufrufen, um die Daten über die durch die gültige Verbindungs-ID angegebene Verbindung an den beteiligten Peer zu senden– wenn der teilnehmende Peer für das **PEER GRAPH EVENT INCOMING \_ \_ \_ \_ DATA-Ereignis** registriert ist. Die nicht transparenten Daten sind als [**\_ PEERDATENstruktur**](/windows/desktop/api/P2P/ns-p2p-peer_data) in den EINGEHENDEN [**\_ PEEREREIGNISDATEN \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) verfügbar, die vom **PEER GRAPH EVENT INCOMING \_ \_ \_ \_ DATA-Ereignis zurückgegeben** werden.

Wenn keine Verbindung erforderlich ist, ruft eine Anwendung [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) mit dem Graphhand handle und der Verbindungs-ID auf.

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>Direkte Verbindungen mithilfe der Peer grouping-Infrastruktur

Direkte Verbindungen innerhalb der Peer grouping Infrastructure werden ähnlich wie die Peer Graphing-Infrastruktur verarbeitet.

Bevor eine direkte Verbindung zwischen zwei Mitgliedern in einer Gruppe hergestellt werden kann, müssen sich beide Mitglieder für das **PEER GROUP EVENT DIRECT \_ \_ \_ \_ CONNECTION-Ereignis** registrieren. Wenn ein Gruppenmitglied Daten über eine direkte Verbindung empfangen möchte, muss sich das Gruppenmitglied auch für das **PEER GROUP EVENT INCOMING \_ \_ \_ \_ DATA-Ereignis** registrieren.

**PEER \_ GROUP \_ EVENT \_ DIRECT \_ CONNECTION** ist ein Ereignis, das eine Anwendung benachrichtigt, ob ein direkter Verbindungsversuch erfolgreich ist oder nicht. Der tatsächliche Erfolgs- oder Fehlerstatus eines Aufrufs von [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) wird in der PEER_GROUP_EVENT_DATA [**zurückgegeben.**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)

Um eine direkte Verbindung zu erstellen, ruft eine Anwendung [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)auf und übergibt dann ein Handle an die Gruppe, einen Zeiger auf die Identität des anderen Mitglieds, das an dieser Verbindung beteiligt ist, und einen Zeiger auf eine IPv6-Adressstruktur für das teilnehmende Mitglied. Der Member, dessen Identität und IPv6-Adresse im Aufruf von **PeerGroupOpenDirectConnection** angegeben sind, muss für das **PEER GROUP EVENT INCOMING \_ \_ \_ \_ DATA-Ereignis** registriert werden, oder der Member kann keine Daten empfangen, die von einem aufrufenden Peer gesendet werden. **PeerGroupOpenDirectConnection gibt** bei Erfolgreicher eine 64-Bit-Verbindungs-ID zurück. Ein Peer muss jedoch warten, bis das **PEER GRAPH EVENT DIRECT \_ \_ \_ \_ CONNECTION-Ereignis** ausgelöst wird, bevor die ID der direkten Verbindung als gültig identifiziert werden kann.

Nachdem eine Verbindung hergestellt und eine gültige Verbindungs-ID bestätigt wurde, kann eine Anwendung [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) aufrufen, um Daten über eine Verbindung zu senden, die von der gültigen Verbindungs-ID an den beteiligten Peer angegeben wird– wenn der teilnehmende Peer für das **PEER GROUP EVENT INCOMING \_ \_ \_ \_ DATA-Ereignis** registriert ist. Die nicht transparenten Daten sind als [**\_ PEERDATENstruktur**](/windows/desktop/api/P2P/ns-p2p-peer_data) in den [**EINGEHENDEN \_ PEEREREIGNISDATEN \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) verfügbar, die vom **PEER GROUP EVENT INCOMING \_ \_ \_ \_ DATA-Ereignis zurückgegeben** werden.

Wenn die Verbindung nicht benötigt wird, ruft die Anwendung [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) mit dem Gruppenhand handle und der Verbindungs-ID auf.

## <a name="example-of-a-direct-connection-for-graphing"></a>Beispiel für eine direkte Verbindung für graphing


```C++
#include <p2p.h>

#pragma comment(lib, "p2pgraph.lib")

//-----------------------------------------------------------------------------
// Function: CreateDirectConnection
//
// Purpose:  Demonstrate how to create a direct connection.
//
// Arguments:
//           hGraph - the graph in which to create the connection
//           pwzId  - the peer identification string
//
// Returns:  ULONGLONG - the connection id or 0
//

ULONGLONG CreateDirectConnection(HGRAPH hGraph, PCWSTR pwzId)
{
    HRESULT   hr = S_OK;

    ULONGLONG ullConnection = 0; // the connection id to return

    HPEERENUM hPeerEnum = NULL;
 
    hr = PeerGraphEnumNodes(hGraph, pwzId, &hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cItem = 1; // want only one matching result

        PEER_NODE_INFO ** ppNodeInfo = NULL;

        hr = PeerGraphGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNodeInfo);

        if (SUCCEEDED(hr))
        {
            if ((cItem > 0) && (NULL != ppNodeInfo))
            {
                if ((*ppNodeInfo)->cAddresses > 0)
                {
                    hr = PeerGraphOpenDirectConnection(hGraph, pwzId,
                            &(*ppNodeInfo)->pAddresses[0], &ullConnection);
                }
                PeerGraphFreeData(ppNodeInfo);
            }
        }
        PeerGraphEndEnumeration(hPeerEnum);
    }
    return ullConnection;
}

```



 

 



