---
title: Informationen zum Routing Table Manager Version 1
description: Der Routing Tabellen-Manager ist ein zentrales Repository mit Routing Informationen für alle Routing Protokolle, die unter Routing-und RAS-Dienst (RRAS) betrieben werden.
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- RRAS für den Routing-und RAS-Dienst, Routing-Tabellen-Manager Version 1
- RRAS für den Routing-und RAS-Dienst, Routing Table Manager Version 1, beschrieben
- Routing Tabellen-Manager, Version 1, RRAS
- Routing Table Manager Version 1 RRAS, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037085"
---
# <a name="about-routing-table-manager-version-1"></a><span data-ttu-id="c81f0-107">Informationen zum Routing Table Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="c81f0-107">About Routing Table Manager Version 1</span></span>

<span data-ttu-id="c81f0-108">**Windows Server 2003:** Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c81f0-108">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c81f0-109">Neue Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.</span><span class="sxs-lookup"><span data-stu-id="c81f0-109">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="c81f0-110">Der Routing Tabellen-Manager ist ein zentrales Repository mit Routing Informationen für alle Routing Protokolle, die unter Routing-und RAS-Dienst (RRAS) betrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c81f0-110">The routing table manager is a central repository of routing information for all routing protocols that operate under Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="c81f0-111">Der Routing Tabellen-Manager bietet Routing Informationen für alle interessierten Komponenten, z. b. Routing Protokolle, Verwaltungs-Agents und Überwachungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="c81f0-111">The routing table manager provides routing information to all interested components, such as routing protocols, management agents, and monitoring agents.</span></span> <span data-ttu-id="c81f0-112">Der Routing Tabellen-Manager bestimmt außerdem die beste Route zu jedem Zielnetzwerk, das den Routing Protokollen bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c81f0-112">The routing table manager also determines the best route to each destination network known to the routing protocols.</span></span> <span data-ttu-id="c81f0-113">Diese Route wird anhand von Routing Protokoll Prioritäten und Metriken, die den Routen zugeordnet sind, bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c81f0-113">It determines this route based on routing protocol priorities and on metrics associated with the routes.</span></span> <span data-ttu-id="c81f0-114">Beachten Sie, dass der Administrator Routing Protokoll Prioritäten konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="c81f0-114">Note that the administrator is able to configure routing protocol priorities.</span></span> <span data-ttu-id="c81f0-115">Der Routing Tabellen-Manager übergibt dann die Best-Route-Informationen an die Weiterleitungen und zurück zu den Routing Protokollen.</span><span class="sxs-lookup"><span data-stu-id="c81f0-115">The routing table manager then passes the best-route information on to the forwarders and back to the routing protocols.</span></span>

<span data-ttu-id="c81f0-116">Jedes Routing Protokoll ruft [**rtmregisterclient**](rtmregisterclient.md) auf, um sich beim Routing Tabellen-Manager zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c81f0-116">Each routing protocol calls [**RtmRegisterClient**](rtmregisterclient.md) to register with the routing table manager.</span></span> <span data-ttu-id="c81f0-117">**Rtmregisterclient** gibt ein Handle zurück, das vom Routing Protokoll verwendet wird, um Routen Einträge hinzuzufügen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c81f0-117">**RtmRegisterClient** returns a handle that is used by the routing protocol to add or delete route entries.</span></span> <span data-ttu-id="c81f0-118">**Rtmregisterclient** ermöglicht auch dem Routing Protokoll das Registrieren eines Ereignis Objekts beim Routing Tabellen-Manager.</span><span class="sxs-lookup"><span data-stu-id="c81f0-118">**RtmRegisterClient** also allows the routing protocol to register an event object with the routing table manager.</span></span> <span data-ttu-id="c81f0-119">Der Routing-Tabellen-Manager signalisiert diesem Ereignis Objekt, das Routing Protokoll über Änderungen an den Informationen über die beste Route zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c81f0-119">The routing table manager signals this event object to notify the routing protocol of changes in best-route information.</span></span> <span data-ttu-id="c81f0-120">Alle anderen Komponenten können mithilfe der Routen Enumeration Informationen abrufen, die im Routing Tabellen-Manager gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c81f0-120">All other components can obtain information stored in the routing table manager through route enumeration.</span></span>

 

 




