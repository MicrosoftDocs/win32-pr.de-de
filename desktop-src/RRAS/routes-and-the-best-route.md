---
title: Routen und die beste Route
description: Eine Route ist "\ 0034; Netzwerkpfad \ 0034;". an ein Ziel, dem bestimmte Kosten zugeordnet sind. Die Kosten werden durch die administrative Präferenz und die Protokoll spezifische Metrik repräsentiert. Routen mit geringeren Kosten werden gegenüber allen anderen Routen bevorzugt.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339450"
---
# <a name="routes-and-the-best-route"></a>Routen und die beste Route

Eine Route ist ein "Netzwerkpfad" zu einem Ziel, dem bestimmte Kosten zugeordnet sind. Die Kosten werden durch die administrative Präferenz und die Protokoll spezifische Metrik repräsentiert. Routen mit geringeren Kosten werden gegenüber allen anderen Routen bevorzugt.

Ein Routen Eintrag in der Routing Tabelle umfasst Folgendes:

-   Ein Handle für das Ziel.
-   Der Besitzer dieser Route.
-   Der Nachbar (Peer), der die Routeninformationen bereitgestellt hat.
-   Flags, die dem Zustand der Route zugeordnet sind
-   Der Route zugeordnete Flags
-   Die bevorzugte und Metrik für die Route
-   Die Liste der Sichten, zu denen die Route gehört.
-   Informationen, die für den Besitzer der Route privat sind
-   Eine Liste der nächsten Hops, die zum Erreichen des Ziels verwendet werden.

In den folgenden Werten wird eine Route in der Routing Tabelle eindeutig identifiziert:

-   Das Zielnetzwerk
-   Der Besitzer der Route.
-   Der Nachbar, der die Route bereitgestellt hat.

## <a name="metrics-and-preference"></a>Metriken und Vorlieben

Jede Route verfügt über eine administrative Präferenz (angegeben durch die Routing Richtlinie) und eine Client abhängige Metrik. Der Routing Tabellen-Manager verwendet diese Informationen, um zu bestimmen, welche Route die bessere Route zu einem Ziel ist. Routen mit niedrigerer Vorliebe sind bessere Routen (eine niedrigste und somit am besten). Wenn zwei Routen die gleiche Einstellung aufweisen, ist die Route mit der niedrigeren Metrik die bessere Route.

Normalerweise wird eine Route durch die bevorzugte Einstellung des Clients bestimmt, der die Route hinzugefügt hat. Allerdings kann für alle Routen, die mithilfe des Netsh.exe Verwaltungs Tools hinzugefügt werden, ein bevorzugter Wert pro Route angegeben werden.

Preference wird normalerweise verwendet, um die Priorität zwischen Clients anzugeben. Ein Administrator kann z. b. OSPF eine niedrigere (bessere) Einstellung als RIP zuweisen. In diesem Fall sind OSPF-Routen für das Weiterleiten von Routen vorzuziehen.

 

 




