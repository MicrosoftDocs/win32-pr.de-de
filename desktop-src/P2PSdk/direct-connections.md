---
description: Mithilfe der Infrastrukturen für Peer-und Peer Gruppierung können Anwendungen direkt eine Verbindung mit einem Knoten (graphende) oder einem Element (Gruppierung) herstellen und Daten direkt mit dem Knoten austauschen. Diese Verbindung wird als direkte Verbindung bezeichnet.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Direkte Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e357b3a4ebc765a013de05234bc8fc9be20943d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362481"
---
# <a name="direct-connections"></a>Direkte Verbindungen

Mithilfe der Infrastrukturen für Peer-und Peer Gruppierung können Anwendungen direkt eine Verbindung mit einem Knoten (graphende) oder einem Element (Gruppierung) herstellen und Daten direkt mit dem Knoten austauschen. Diese Verbindung wird als **direkte Verbindung** bezeichnet.

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>Direkte Verbindungen mithilfe der Peer graphinginfrastruktur

Bevor eine direkte Verbindung zwischen zwei Knoten in einem Diagramm hergestellt werden kann, müssen beide Knoten für das **Peer \_ Graph \_ Event \_ Direct \_ Connection** -Ereignis registriert werden. Zum Empfangen von Daten über eine direkte Verbindung müssen die Knoten auch für das **\_ \_ \_ eingehende \_ Daten Ereignis des Peer Graph-Ereignisses** registriert werden.

**Peer \_ Die \_ direkte Graph-Ereignis \_ \_ Verbindung** ist ein Ereignis, das einer Anwendung mitteilt, ob ein direkter Verbindungsversuch erfolgreich ist oder fehlschlägt. Der tatsächliche Erfolg oder Fehlerstatus eines [**peergraphopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) -Aufrufes wird in der [**Peer \_ Graph- \_ Ereignis \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) Struktur zurückgegeben.

Zum Erstellen einer direkten Verbindung Ruft eine Anwendung [**peergraphopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)auf und übergibt dann ein Handle an das Diagramm, einen Zeiger auf die Identität des anderen Knotens, der an der Verbindung teilnimmt, und einen Zeiger auf eine IPv6-Adressstruktur für den teilnehmenden Knoten. Die Knoten Identität und die IPv6-Adresse, die im Aufruf von **peergraphopendirectconnection** angegeben sind, müssen für **das \_ \_ \_ eingehende \_ Daten Ereignis des Peer Graph-Ereignisses** registriert werden, oder Sie können keine Daten empfangen, die von einem aufrufenden Peer gesendet werden. Bei erfolgreicher Ausführung gibt " **Peer Diagramm opendirectconnection** " eine 64-Bit-Verbindungs-ID zurück. Der Peer muss jedoch auf das Ereignis **\_ \_ \_ Direct \_ Connection** -Ereignis der Peer Gruppe warten, bevor die direkte Verbindungs-ID als gültig identifiziert werden kann.

Nachdem eine Verbindung hergestellt und eine gültige Verbindungs-ID bestätigt wurde, kann eine Anwendung [**peergraphsenddata**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) abrufen, um die Daten über die durch die gültige Verbindungs-ID angegebene Verbindung an den teilnehmenden Peer zu senden – wenn der Beteiligte Peer für das **\_ \_ \_ eingehende \_ Daten Ereignis des Peer Graph-Ereignisses** registriert ist. Die nicht transparenten Daten sind als [**Peer \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_data) Struktur in den [**\_ \_ eingehenden \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) des Peer Ereignisses verfügbar, die vom Ereignis **\_ \_ \_ eingehender \_ Daten Ereignis für Peer Graph** -Ereignis zurückgegeben werden.

Wenn keine Verbindung benötigt wird, ruft eine Anwendung " [**Peer Graph closedirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) " mit dem Diagramm Handle und der Verbindungs-ID auf.

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>Direkte Verbindungen mithilfe der Peer Gruppierungs Infrastruktur

Direkte Verbindungen innerhalb der Peer Gruppierungs Infrastruktur werden ähnlich wie bei der Peer-graphinginfrastruktur behandelt.

Bevor eine direkte Verbindung zwischen zwei Mitgliedern einer Gruppe hergestellt werden kann, müssen sich beide Mitglieder für das **\_ \_ Ereignis \_ Direct \_ Connection** -Ereignis der Peer Gruppe registrieren. Wenn ein Gruppenmitglied Daten über eine direkte Verbindung empfangen möchte, muss sich das Gruppenmitglied auch für das **\_ \_ Ereignis \_ eingehende \_ Daten der Peer Gruppe** registrieren.

**Peer \_ Die \_ \_ direkte \_ Verbindung von Gruppen Ereignissen** ist ein Ereignis, bei dem eine Anwendung benachrichtigt wird, ob ein direkter Verbindungsversuch erfolgreich ist oder fehlschlägt. Der tatsächliche Erfolg oder Fehlerstatus eines Aufrufes [**peergroupopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) -Aufrufes wird in der [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) Struktur zurückgegeben.

Zum Erstellen einer direkten Verbindung Ruft eine Anwendung [**peergroupopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)auf und übergibt dann ein Handle an die Gruppe, einen Zeiger auf die Identität des anderen Elements, das an dieser Verbindung beteiligt ist, und einen Zeiger auf eine IPv6-Adressstruktur für das beteiligte Element. Der Member, dessen Identität und IPv6-Adresse im Aufruf von **peergroupopendirectconnection** angegeben werden, muss für das **\_ \_ Ereignis \_ eingehender \_ Daten Ereignis für Peer Gruppen Ereignisse** registriert werden, oder der Member kann keine Daten empfangen, die von einem aufrufenden Peer gesendet werden. " **Peer groupopendirectconnection** " gibt bei erfolgreicher Ausführung eine 64-Bit-Verbindungs-ID zurück. Ein Peer muss jedoch warten, bis das Ereignis " **Peer \_ Graph \_ Event \_ Direct \_ Connection** " ausgelöst wird, bevor die direkte Verbindungs-ID als gültig identifiziert werden kann.

Nachdem eine Verbindung hergestellt und eine gültige Verbindungs-ID bestätigt wurde, kann eine Anwendung [**peergroupsenddata**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) aufrufen, um Daten über eine durch die gültige Verbindungs-ID angegebene Verbindung an den teilnehmenden Peer zu senden –, wenn der Beteiligte Peer für das Ereignis **\_ \_ \_ eingehender \_ Daten Ereignis für Peer Gruppen Ereignisse** registriert ist. Die nicht transparenten Daten sind als [**Peer \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_data) Struktur in den [**\_ \_ eingehenden \_ Daten des Peer Ereignisses**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) verfügbar, die vom **\_ \_ Ereignis \_ eingehender \_ Daten Ereignis für Peer Gruppen Ereignisse** zurückgegeben werden.

Wenn die Verbindung nicht benötigt wird, ruft die Anwendung " [**Peer groupclosedirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) " mit dem Gruppen Handle und der Verbindungs-ID auf.

## <a name="example-of-a-direct-connection-for-graphing"></a>Beispiel für eine direkte Verbindung zum grafisch


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



 

 



