---
title: Änderungen an der besten Route zu einem Netzwerk
description: Eine Änderung in einem der folgenden Werte für die beste Route zu einem bestimmten Zielnetzwerk bewirkt, dass der Routing Tabellen-Manager eine Benachrichtigungs Meldung generiert, die an jeden registrierten Client und an die Weiterleitungen gesendet wird.
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339428"
---
# <a name="changes-to-the-best-route-to-a-network"></a><span data-ttu-id="fb5d9-103">Änderungen an der besten Route zu einem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="fb5d9-103">Changes to the Best Route to a Network</span></span>

<span data-ttu-id="fb5d9-104">**Windows Server 2003:** Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb5d9-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="fb5d9-105">Neue Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.</span><span class="sxs-lookup"><span data-stu-id="fb5d9-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="fb5d9-106">Eine Änderung in den folgenden Werten für die beste Route zu einem bestimmten Zielnetzwerk bewirkt, dass der Routing Tabellen-Manager eine Benachrichtigungs Meldung generiert, die an jeden registrierten Client und an die Weiterleitungen gesendet wird:</span><span class="sxs-lookup"><span data-stu-id="fb5d9-106">A change in any of the following values for the best route to a given destination network causes the routing table manager to generate a notification message sent to each registered client and to the forwarders:</span></span>

-   <span data-ttu-id="fb5d9-107">Protokoll Bezeichner</span><span class="sxs-lookup"><span data-stu-id="fb5d9-107">Protocol identifier</span></span>
-   <span data-ttu-id="fb5d9-108">Schnittstellen Index</span><span class="sxs-lookup"><span data-stu-id="fb5d9-108">Interface index</span></span>
-   <span data-ttu-id="fb5d9-109">Adresse des Routers für den nächsten Hop</span><span class="sxs-lookup"><span data-stu-id="fb5d9-109">Address of next-hop router</span></span>
-   <span data-ttu-id="fb5d9-110">Protokoll Familien spezifische Daten, die Routingmetriken enthalten</span><span class="sxs-lookup"><span data-stu-id="fb5d9-110">Protocol family-specific data that includes route metrics</span></span>

<span data-ttu-id="fb5d9-111">Eine Änderung an der Protokoll Kennung, dem Schnittstellen Index oder der Routeradresse für den nächsten Hop tritt auf, wenn ein neuer, besserer Routen Eintrag hinzugefügt wird oder wenn der aktuelle beste Routen Eintrag gelöscht oder entfernt wird und eine andere Route als neue beste Route verlässt.</span><span class="sxs-lookup"><span data-stu-id="fb5d9-111">A change in protocol identifier, interface index, or next-hop router address occurs when a new, better-route entry is added, or when the current best-route entry is deleted or aged out, and leaves another route as the new best route.</span></span>

 

 




