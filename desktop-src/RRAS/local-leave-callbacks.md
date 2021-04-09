---
title: Lokale Leave-Rückrufe
description: Nachdem der Multicast-Gruppen-Manager von IGMP benachrichtigt wurde, dass für eine Gruppe auf einer Schnittstelle keine weiteren Empfänger vorhanden sind, ruft der Multicast-Gruppen-Manager den lokalen pmgm-Rückruf Rückruf auf \_ \_ \_ das Routing Protokoll für diese Schnittstelle auf, sofern vorhanden. Dieser Rückruf benachrichtigt das Routing Protokoll über die Änderung.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98d32e041b048e15497bc7fe35d17628b9331d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037176"
---
# <a name="local-leave-callbacks"></a><span data-ttu-id="ecaeb-104">Lokale Leave-Rückrufe</span><span class="sxs-lookup"><span data-stu-id="ecaeb-104">Local Leave Callbacks</span></span>

<span data-ttu-id="ecaeb-105">Nachdem der Multicast-Gruppen-Manager von IGMP benachrichtigt wurde, dass für eine Gruppe auf einer Schnittstelle keine weiteren Empfänger vorhanden sind, ruft der Multicast-Gruppen-Manager den [**lokalen pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) Rückruf auf das Routing Protokoll für diese Schnittstelle auf, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ecaeb-105">After the multicast group manager is notified by IGMP that there are no more receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback to the routing protocol on that interface if one exists.</span></span> <span data-ttu-id="ecaeb-106">Dieser Rückruf benachrichtigt das Routing Protokoll über die Änderung.</span><span class="sxs-lookup"><span data-stu-id="ecaeb-106">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="ecaeb-107">Dieser Rückruf und der [**pmgm \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) -Rückruf Rückruf für lokale Joins werden zum Synchronisieren der Weiterleitung zwischen IGMP-und Routing Protokollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ecaeb-107">This callback and the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




