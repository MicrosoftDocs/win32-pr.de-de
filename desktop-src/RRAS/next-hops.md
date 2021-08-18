---
title: Nächste Hops
description: Routen sind mindestens ein nächster Hop zugeordnet.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a8d73a0d553773537ca2efd67457498ff9710cf9e7834d6952fcf2a81c5c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790100"
---
# <a name="next-hops"></a>Nächste Hops

Routen sind mindestens ein nächster Hop zugeordnet. Wenn sich das Ziel nicht in einem direkt verbundenen Netzwerk befindet, ist der nächste Hop die Adresse des nächsten Routers (oder Netzwerks) im ausgehenden Netzwerk, mit dem Daten am besten an das Ziel geroutet werden können. Die beste Route ist die Route mit den geringsten Kosten, basierend auf der verwendeten Routingrichtlinie. Mit jedem nächsten Hop können Daten auf dem Pfad zum Ziel weitergeleitet werden. Alle Routen im Besitz eines Clients verwenden einen gemeinsamen Satz von Einträgen für den nächsten Hop, die vom Client hinzugefügt wurden.

Jeder nächste Hop wird eindeutig durch die Adresse des nächsten Hops und den Schnittstellenindex identifiziert, der zum Erreichen des nächsten Hops verwendet wird.

Wenn der nächste Hop selbst nicht direkt verbunden ist, wird er als "Remote" des nächsten Hops markiert. In diesem Fall muss die Forwarder-Anwendung eine weitere Suche mithilfe der Netzwerkadresse des nächsten Hops durchführen. Diese Suche ist erforderlich, um den "lokalen" nächsten Hop zu finden, der verwendet wird, um den nächsten Remotehop und das Ziel zu erreichen.

Ein Eintrag für den nächsten Hop in der Routingtabelle enthält Folgendes:

-   Die Netzwerkadresse des nächsten Hops
-   Der Besitzer des nächsten Hops
-   Der Bezeichner der ausgehenden Schnittstelle
-   Der Status des nächsten Hops
-   Flags, die dem nächsten Hop zugeordnet sind
-   Informationen, die für den Besitzer des nächsten Hops privat sind
-   Ein Handle für das Ziel, das dem nächsten Remotehop entspricht

 

 




