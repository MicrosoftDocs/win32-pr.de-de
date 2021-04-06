---
title: RPF-Warnungs Rückrufe
description: Nachdem der Multicast-Gruppen-Manager eine Benachrichtigung über ein Paket von einer neuen Quelle oder einem Paket erhalten hat, das für eine neue Gruppe bestimmt ist, sucht der Multicast-Gruppen-Manager in der Multicast Ansicht der Routing Tabelle die Route zur Quelle.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714664"
---
# <a name="rpf-alert-callbacks"></a><span data-ttu-id="2739c-103">RPF-Warnungs Rückrufe</span><span class="sxs-lookup"><span data-stu-id="2739c-103">RPF Alert Callbacks</span></span>

<span data-ttu-id="2739c-104">Nachdem der Multicast-Gruppen-Manager eine Benachrichtigung über ein Paket von einer neuen Quelle oder einem Paket erhalten hat, das für eine neue Gruppe bestimmt ist, sucht der Multicast-Gruppen-Manager in der Multicast Ansicht der Routing Tabelle die Route zur Quelle.</span><span class="sxs-lookup"><span data-stu-id="2739c-104">After the multicast group manager receives notification of a packet from a new source or of a packet that is destined for a new group, the multicast group manager looks up the route to the source in the multicast view of the routing table.</span></span> <span data-ttu-id="2739c-105">Der Multicast-Gruppen-Manager ruft dann den [**pmgm \_ RPF- \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) Rückruf für das Protokoll auf, das die Schnittstelle besitzt, auf der die Daten eingetroffen sind.</span><span class="sxs-lookup"><span data-stu-id="2739c-105">The multicast group manager then invokes the [**PMGM\_RPF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) callback to the protocol that owns the interface the data arrived on.</span></span>

<span data-ttu-id="2739c-106">Nachdem dieser Rückruf aufgerufen wurde, kann das Routing Protokoll die eingehende Schnittstelle ändern, wenn das Routing Protokoll die Daten für die Gruppe auf einer anderen Schnittstelle empfangen muss.</span><span class="sxs-lookup"><span data-stu-id="2739c-106">After this callback is invoked, the routing protocol can change the incoming interface if the routing protocol must receive the data for the group on a different interface.</span></span>

 

 




