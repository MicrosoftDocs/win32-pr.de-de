---
title: Warnungs Rückrufe löschen
description: Wenn der Multicast-Gruppen-Manager benachrichtigt wird, dass Empfänger eine Gruppe auf einer Schnittstelle belassen, ruft der Multicast-Gruppen-Manager den pmgm- \_ \_ \_ Rückruf Rückruf Rückruf auf.
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037496"
---
# <a name="prune-alert-callbacks"></a><span data-ttu-id="43610-103">Warnungs Rückrufe löschen</span><span class="sxs-lookup"><span data-stu-id="43610-103">Prune Alert Callbacks</span></span>

<span data-ttu-id="43610-104">Wenn der Multicast-Gruppen-Manager benachrichtigt wird, dass Empfänger eine Gruppe auf einer Schnittstelle belassen, ruft der Multicast-Gruppen-Manager den [**pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) Rückruf Rückruf auf.</span><span class="sxs-lookup"><span data-stu-id="43610-104">When the multicast group manager is notified that receivers are leaving a group on an interface, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback.</span></span> <span data-ttu-id="43610-105">Dieser Rückruf benachrichtigt die Routing Protokolle, dass Clients nicht mehr zur angegebenen Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="43610-105">This callback notifies the routing protocols that clients no longer belong to the specified group.</span></span> <span data-ttu-id="43610-106">Daher müssen die Routing Protokolle die Anforderung von Multicast Daten für die angegebenen Gruppen nicht mehr anfordern.</span><span class="sxs-lookup"><span data-stu-id="43610-106">Therefore, the routing protocols must stop requesting multicast data for the specified groups.</span></span>

<span data-ttu-id="43610-107">Der Multicast-Gruppen-Manager verfügt über einen vordefinierten Satz von Regeln, mit denen bestimmt wird, wann dieser Rückruf aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="43610-107">The multicast group manager has a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="43610-108">Diese Regeln basieren sowohl auf dem Typ der vom Client gesendeten Anforderung zum Löschen von Anforderungen als auch auf der Reihenfolge, in der die Anforderungen für die Anforderung empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="43610-108">These rules are based on both the type of prune request sent by the client and the order the prune requests were received in.</span></span>

## <a name="wildcard-prune-requests"></a><span data-ttu-id="43610-109">Platzhalter zum Löschen von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43610-109">Wildcard Prune Requests</span></span>

<span data-ttu-id="43610-110">Wenn ein Platzhalter für eine Gruppe ( \* , g) empfangen wird und die letzte Schnittstelle für den zweit-bis letzten Client entfernt wird (d. h. wenn nur Schnittstellen für einen einzelnen Client verbleiben), ruft der Multicast-Gruppen-Manager den [**pmgm- \_ \_ \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) Rückruf Rückruf für den verbleibenden Client auf.</span><span class="sxs-lookup"><span data-stu-id="43610-110">When a wildcard prune for a group (\*, g) is received and the final interface is being removed for the second-to-last client (that is, when interfaces for only a single client remain), the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback to that remaining client.</span></span> <span data-ttu-id="43610-111">Nachdem die endgültige Schnittstelle für den letzten Client entfernt wurde (d. h., wenn keine anderen Schnittstellen verbleiben), wird dieser Rückruf für alle anderen Clients aufgerufen, die beim Multicast-Gruppen-Manager registriert sind.</span><span class="sxs-lookup"><span data-stu-id="43610-111">After the final interface is removed for the last client (that is, when no other interfaces remain), then this callback is invoked for all the other clients that are registered with the multicast group manager.</span></span>

## <a name="source-specific-prune-requests"></a><span data-ttu-id="43610-112">Source-Specific Anforderungen löschen</span><span class="sxs-lookup"><span data-stu-id="43610-112">Source-Specific Prune Requests</span></span>

<span data-ttu-id="43610-113">Wenn eine Quell spezifische Sicherung für eine Gruppe (n) empfangen wird, ruft der Multicast-Gruppen-Manager den pmgm-Rückruf Rückruf Rückruf nur für den Client auf, der die eingehende Schnittstelle für die Quelle s besitzt. [**\_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)</span><span class="sxs-lookup"><span data-stu-id="43610-113">When a source-specific prune for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




