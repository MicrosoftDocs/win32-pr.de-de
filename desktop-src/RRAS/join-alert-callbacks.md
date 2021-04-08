---
title: Rückruf für Benachrichtigungs Rückrufe
description: Wenn der Multicast-Gruppen-Manager benachrichtigt wird, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicast-Gruppen-Manager den Rückruf Rückruf für die pmgm- \_ \_ Rückruf Warnung auf \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037178"
---
# <a name="join-alert-callbacks"></a><span data-ttu-id="df0b0-103">Rückruf für Benachrichtigungs Rückrufe</span><span class="sxs-lookup"><span data-stu-id="df0b0-103">Join Alert Callbacks</span></span>

<span data-ttu-id="df0b0-104">Wenn der Multicast-Gruppen-Manager benachrichtigt wird, dass neue Empfänger für eine Gruppe auf einer Schnittstelle vorhanden sind, ruft der Multicast-Gruppen-Manager den Rückruf Rückruf für die [**pmgm- \_ \_ \_ Rückruf Warnung**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) auf.</span><span class="sxs-lookup"><span data-stu-id="df0b0-104">When the multicast group manager is notified that there are new receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback.</span></span> <span data-ttu-id="df0b0-105">Dieser Rückruf benachrichtigt die Routing Protokolle, dass die neuen Hosts den angegebenen Gruppen beigetreten sind.</span><span class="sxs-lookup"><span data-stu-id="df0b0-105">This callback notifies the routing protocols that new hosts have joined the specified groups .</span></span> <span data-ttu-id="df0b0-106">Daher müssen die Routing Protokolle Multicast Daten für die vom Rückruf angegebenen Gruppen anfordern.</span><span class="sxs-lookup"><span data-stu-id="df0b0-106">Therefore, the routing protocols must request multicast data for the groups specified by the callback.</span></span>

<span data-ttu-id="df0b0-107">Der Multicast-Gruppen-Manager verwendet einen vordefinierten Satz von Regeln, die verwendet werden, um zu bestimmen, wann dieser Rückruf aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="df0b0-107">The multicast group manager uses a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="df0b0-108">Dieser Regelsatz basiert sowohl auf dem Typ der vom Client gesendeten joinanforderung als auch auf der Reihenfolge, in der die Joinanforderungen empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="df0b0-108">This set of rules is based on both the type of join request sent by the client and the order the join requests were received in.</span></span>

## <a name="wildcard-join-requests"></a><span data-ttu-id="df0b0-109">Platzhalter-Joinanforderungen</span><span class="sxs-lookup"><span data-stu-id="df0b0-109">Wildcard Join Requests</span></span>

<span data-ttu-id="df0b0-110">Wenn ein Platzhalter Join für eine Gruppe ( \* , g) vom ersten Client empfangen wird, ruft der Multicast-Gruppen-Manager den [**pmgm-Rückruf Rückruf- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) Rückruf für alle anderen registrierten Clients auf.</span><span class="sxs-lookup"><span data-stu-id="df0b0-110">When a wildcard join for a group (\*, g) is received from the first client, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback to all other registered clients.</span></span> <span data-ttu-id="df0b0-111">Wenn ein Platzhalter Join für eine Gruppe vom zweiten Client empfangen wird, ruft der Multicast-Gruppen-Manager diesen Rückruf an den ersten Client an, um der Gruppe beizutreten.</span><span class="sxs-lookup"><span data-stu-id="df0b0-111">When a wildcard join for a group is received from the second client, the multicast group manager invokes this callback to the first client to join the group.</span></span>

## <a name="source-specific-join-requests"></a><span data-ttu-id="df0b0-112">Joinanforderungen Source-Specific</span><span class="sxs-lookup"><span data-stu-id="df0b0-112">Source-Specific Join Requests</span></span>

<span data-ttu-id="df0b0-113">Der Multicast-Gruppen-Manager ruft diesen Rückruf nicht für nachfolgende Joins in der Gruppe auf.</span><span class="sxs-lookup"><span data-stu-id="df0b0-113">The multicast group manager does not invoke this callback for any subsequent joins to the group.</span></span>

<span data-ttu-id="df0b0-114">Wenn ein Quell spezifischer Join für eine Gruppe (n) empfangen wird, ruft der Multicast-Gruppen-Manager den pmgm-Rückruf Rückruf für die [**\_ \_ \_ Rückruf Warnung**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) nur für den Client auf, der die eingehende Schnittstelle für die Quell-s besitzt.</span><span class="sxs-lookup"><span data-stu-id="df0b0-114">When a source-specific join for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




