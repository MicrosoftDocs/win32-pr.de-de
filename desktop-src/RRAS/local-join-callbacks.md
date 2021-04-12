---
title: Lokale joinrückrufe
description: Nachdem der Multicast-Gruppen-Manager von IGMP benachrichtigt wurde, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicast-Gruppen-Manager den pmgm- \_ \_ Rückruf Rückruf \_ Rückruf auf das Routing Protokoll auf, der die Schnittstelle besitzt, sofern vorhanden.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471549"
---
# <a name="local-join-callbacks"></a><span data-ttu-id="81ae0-103">Lokale joinrückrufe</span><span class="sxs-lookup"><span data-stu-id="81ae0-103">Local Join Callbacks</span></span>

<span data-ttu-id="81ae0-104">Nachdem der Multicast-Gruppen-Manager von IGMP benachrichtigt wurde, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicast-Gruppen-Manager den [**pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) Rückruf Rückruf auf das Routing Protokoll auf, der die Schnittstelle besitzt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="81ae0-104">After the multicast group manager is notified by IGMP that new receivers are present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback to the routing protocol that owns the interface if one exists.</span></span> <span data-ttu-id="81ae0-105">Dieser Rückruf benachrichtigt das Routing Protokoll über die Änderung.</span><span class="sxs-lookup"><span data-stu-id="81ae0-105">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="81ae0-106">Dieser Rückruf und der [**lokale pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) Rückruf werden verwendet, um die Weiterleitung zwischen IGMP und Routing Protokollen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="81ae0-106">This callback and the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




