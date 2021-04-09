---
title: Nächste Hops
description: Routen ist mindestens ein nächster Hop zugeordnet.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036441"
---
# <a name="next-hops"></a>Nächste Hops

Routen ist mindestens ein nächster Hop zugeordnet. Wenn sich das Ziel nicht in einem direkt verbundenen Netzwerk befindet, ist der nächste Hop die Adresse des nächsten Routers (oder Netzwerks) im ausgehenden Netzwerk, der die Daten am besten an das Ziel weiterleiten kann. Die beste Route ist die Route mit den geringsten Kosten, basierend auf der verwendeten Routing Richtlinie. Jeder nächste Hop kann verwendet werden, um Daten auf dem Pfad an das Ziel weiterzuleiten. Alle Routen im Besitz eines Clients nutzen einen gemeinsamen Satz von Einträgen im nächsten Hop, die vom Client hinzugefügt wurden.

Jeder nächste Hop wird durch die Adresse des nächsten Hops und den Schnittstellen Index, der zum Erreichen des nächsten Hops verwendet wird, eindeutig identifiziert.

Wenn der nächste Hop selbst nicht direkt verbunden ist, wird er als "Remote" als nächster Hop gekennzeichnet. In diesem Fall muss die Weiterleitung mithilfe der Netzwerkadresse des nächsten Hops eine weitere Suche durchführen. Diese Suche ist erforderlich, um den "lokalen" nächsten Hop zu finden, mit dem der Remote-Hop und das Ziel erreicht werden.

Ein Eintrag für den nächsten Hop in der Routing Tabelle umfasst Folgendes:

-   Die Netzwerkadresse des nächsten Hops.
-   Der Besitzer des nächsten Hops.
-   Der Bezeichner der ausgehenden Schnittstelle.
-   Der Zustand des nächsten Hops.
-   Dem nächsten Hop zugeordnete Flags
-   Informationen, die für den Besitzer des nächsten Hops privat sind
-   Ein Handle für das Ziel, das dem Remote nächsten Hop entspricht.

 

 




