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
# <a name="direct-connections"></a><span data-ttu-id="ff34a-104">Direkte Verbindungen</span><span class="sxs-lookup"><span data-stu-id="ff34a-104">Direct Connections</span></span>

<span data-ttu-id="ff34a-105">Mithilfe der Infrastrukturen für Peer-und Peer Gruppierung können Anwendungen direkt eine Verbindung mit einem Knoten (graphende) oder einem Element (Gruppierung) herstellen und Daten direkt mit dem Knoten austauschen.</span><span class="sxs-lookup"><span data-stu-id="ff34a-105">The Peer Graphing and Peer Grouping Infrastructures allow applications to connect directly to one node (Graphing) or member (Grouping), and then exchange data directly with the node.</span></span> <span data-ttu-id="ff34a-106">Diese Verbindung wird als **direkte Verbindung** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ff34a-106">This connection is called a **direct connection**.</span></span>

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a><span data-ttu-id="ff34a-107">Direkte Verbindungen mithilfe der Peer graphinginfrastruktur</span><span class="sxs-lookup"><span data-stu-id="ff34a-107">Direct Connections using the Peer Graphing Infrastructure</span></span>

<span data-ttu-id="ff34a-108">Bevor eine direkte Verbindung zwischen zwei Knoten in einem Diagramm hergestellt werden kann, müssen beide Knoten für das **Peer \_ Graph \_ Event \_ Direct \_ Connection** -Ereignis registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ff34a-108">Before a direct connection can be established between two nodes in a graph, both nodes must be registered for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="ff34a-109">Zum Empfangen von Daten über eine direkte Verbindung müssen die Knoten auch für das **\_ \_ \_ eingehende \_ Daten Ereignis des Peer Graph-Ereignisses** registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ff34a-109">To receive data over a direct connection, the nodes must also be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="ff34a-110">**Peer \_ Die \_ direkte Graph-Ereignis \_ \_ Verbindung** ist ein Ereignis, das einer Anwendung mitteilt, ob ein direkter Verbindungsversuch erfolgreich ist oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ff34a-110">**PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="ff34a-111">Der tatsächliche Erfolg oder Fehlerstatus eines [**peergraphopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) -Aufrufes wird in der [**Peer \_ Graph- \_ Ereignis \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff34a-111">The actual success or failure status of a call to [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) is returned in the [**PEER\_GRAPH\_EVENT\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) structure.</span></span>

<span data-ttu-id="ff34a-112">Zum Erstellen einer direkten Verbindung Ruft eine Anwendung [**peergraphopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)auf und übergibt dann ein Handle an das Diagramm, einen Zeiger auf die Identität des anderen Knotens, der an der Verbindung teilnimmt, und einen Zeiger auf eine IPv6-Adressstruktur für den teilnehmenden Knoten.</span><span class="sxs-lookup"><span data-stu-id="ff34a-112">To create a direct connection, an application calls [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), and then passes a handle to the graph, a pointer to the identity of the other node that is participating in the connection, and a pointer to an IPv6 address structure for the participating node.</span></span> <span data-ttu-id="ff34a-113">Die Knoten Identität und die IPv6-Adresse, die im Aufruf von **peergraphopendirectconnection** angegeben sind, müssen für **das \_ \_ \_ eingehende \_ Daten Ereignis des Peer Graph-Ereignisses** registriert werden, oder Sie können keine Daten empfangen, die von einem aufrufenden Peer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff34a-113">The node identity and IPv6 address that are specified in the call to **PeerGraphOpenDirectConnection** must be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event, or it cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="ff34a-114">Bei erfolgreicher Ausführung gibt " **Peer Diagramm opendirectconnection** " eine 64-Bit-Verbindungs-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="ff34a-114">When successful, **PeerGraphOpenDirectConnection** returns a 64-bit connection ID.</span></span> <span data-ttu-id="ff34a-115">Der Peer muss jedoch auf das Ereignis **\_ \_ \_ Direct \_ Connection** -Ereignis der Peer Gruppe warten, bevor die direkte Verbindungs-ID als gültig identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff34a-115">However, the peer must wait for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="ff34a-116">Nachdem eine Verbindung hergestellt und eine gültige Verbindungs-ID bestätigt wurde, kann eine Anwendung [**peergraphsenddata**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) abrufen, um die Daten über die durch die gültige Verbindungs-ID angegebene Verbindung an den teilnehmenden Peer zu senden – wenn der Beteiligte Peer für das **\_ \_ \_ eingehende \_ Daten Ereignis des Peer Graph-Ereignisses** registriert ist.</span><span class="sxs-lookup"><span data-stu-id="ff34a-116">After a connection is made and a valid connection ID is confirmed, an application can call [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) to send the data across the connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="ff34a-117">Die nicht transparenten Daten sind als [**Peer \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_data) Struktur in den [**\_ \_ eingehenden \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) des Peer Ereignisses verfügbar, die vom Ereignis **\_ \_ \_ eingehender \_ Daten Ereignis für Peer Graph** -Ereignis zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff34a-117">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="ff34a-118">Wenn keine Verbindung benötigt wird, ruft eine Anwendung " [**Peer Graph closedirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) " mit dem Diagramm Handle und der Verbindungs-ID auf.</span><span class="sxs-lookup"><span data-stu-id="ff34a-118">When a connection is not needed, an application calls [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) with the graph handle and the connection ID.</span></span>

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a><span data-ttu-id="ff34a-119">Direkte Verbindungen mithilfe der Peer Gruppierungs Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="ff34a-119">Direct Connections using the Peer Grouping Infrastructure</span></span>

<span data-ttu-id="ff34a-120">Direkte Verbindungen innerhalb der Peer Gruppierungs Infrastruktur werden ähnlich wie bei der Peer-graphinginfrastruktur behandelt.</span><span class="sxs-lookup"><span data-stu-id="ff34a-120">Direct connections within the Peer Grouping Infrastructure are handled similar to the Peer Graphing Infrastructure.</span></span>

<span data-ttu-id="ff34a-121">Bevor eine direkte Verbindung zwischen zwei Mitgliedern einer Gruppe hergestellt werden kann, müssen sich beide Mitglieder für das **\_ \_ Ereignis \_ Direct \_ Connection** -Ereignis der Peer Gruppe registrieren.</span><span class="sxs-lookup"><span data-stu-id="ff34a-121">Before a direct connection can be established between two members in a group, both members must register for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="ff34a-122">Wenn ein Gruppenmitglied Daten über eine direkte Verbindung empfangen möchte, muss sich das Gruppenmitglied auch für das **\_ \_ Ereignis \_ eingehende \_ Daten der Peer Gruppe** registrieren.</span><span class="sxs-lookup"><span data-stu-id="ff34a-122">If a group member wants to receive data over a direct connection, the group member must also register for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="ff34a-123">**Peer \_ Die \_ \_ direkte \_ Verbindung von Gruppen Ereignissen** ist ein Ereignis, bei dem eine Anwendung benachrichtigt wird, ob ein direkter Verbindungsversuch erfolgreich ist oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ff34a-123">**PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** is an event that is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="ff34a-124">Der tatsächliche Erfolg oder Fehlerstatus eines Aufrufes [**peergroupopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) -Aufrufes wird in der [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff34a-124">The actual success or failure status of a call to [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) is returned in the [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure.</span></span>

<span data-ttu-id="ff34a-125">Zum Erstellen einer direkten Verbindung Ruft eine Anwendung [**peergroupopendirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)auf und übergibt dann ein Handle an die Gruppe, einen Zeiger auf die Identität des anderen Elements, das an dieser Verbindung beteiligt ist, und einen Zeiger auf eine IPv6-Adressstruktur für das beteiligte Element.</span><span class="sxs-lookup"><span data-stu-id="ff34a-125">To create a direct connection, an application calls [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), and then passes a handle to the group, a pointer to the identity of the other member that will participate in this connection, and a pointer to an IPv6 address structure for the participating member.</span></span> <span data-ttu-id="ff34a-126">Der Member, dessen Identität und IPv6-Adresse im Aufruf von **peergroupopendirectconnection** angegeben werden, muss für das **\_ \_ Ereignis \_ eingehender \_ Daten Ereignis für Peer Gruppen Ereignisse** registriert werden, oder der Member kann keine Daten empfangen, die von einem aufrufenden Peer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff34a-126">The member whose identity and IPv6 address are specified in the call to **PeerGroupOpenDirectConnection** must be registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event, or the member cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="ff34a-127">" **Peer groupopendirectconnection** " gibt bei erfolgreicher Ausführung eine 64-Bit-Verbindungs-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="ff34a-127">**PeerGroupOpenDirectConnection** returns a 64-bit connection ID when successful.</span></span> <span data-ttu-id="ff34a-128">Ein Peer muss jedoch warten, bis das Ereignis " **Peer \_ Graph \_ Event \_ Direct \_ Connection** " ausgelöst wird, bevor die direkte Verbindungs-ID als gültig identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff34a-128">However, a peer must wait for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event to be raised before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="ff34a-129">Nachdem eine Verbindung hergestellt und eine gültige Verbindungs-ID bestätigt wurde, kann eine Anwendung [**peergroupsenddata**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) aufrufen, um Daten über eine durch die gültige Verbindungs-ID angegebene Verbindung an den teilnehmenden Peer zu senden –, wenn der Beteiligte Peer für das Ereignis **\_ \_ \_ eingehender \_ Daten Ereignis für Peer Gruppen Ereignisse** registriert ist.</span><span class="sxs-lookup"><span data-stu-id="ff34a-129">After a connection is made and a valid connection ID is confirmed, then an application can call [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) to send data across a connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="ff34a-130">Die nicht transparenten Daten sind als [**Peer \_ Daten**](/windows/desktop/api/P2P/ns-p2p-peer_data) Struktur in den [**\_ \_ eingehenden \_ Daten des Peer Ereignisses**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) verfügbar, die vom **\_ \_ Ereignis \_ eingehender \_ Daten Ereignis für Peer Gruppen Ereignisse** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff34a-130">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="ff34a-131">Wenn die Verbindung nicht benötigt wird, ruft die Anwendung " [**Peer groupclosedirectconnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) " mit dem Gruppen Handle und der Verbindungs-ID auf.</span><span class="sxs-lookup"><span data-stu-id="ff34a-131">When the connection is not needed, the application calls [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) with the group handle and the connection ID.</span></span>

## <a name="example-of-a-direct-connection-for-graphing"></a><span data-ttu-id="ff34a-132">Beispiel für eine direkte Verbindung zum grafisch</span><span class="sxs-lookup"><span data-stu-id="ff34a-132">Example of a Direct Connection for Graphing</span></span>


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



 

 



