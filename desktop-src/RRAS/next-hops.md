---
title: Nächste Hops
description: Routen sind mindestens einem nächsten Hop zugeordnet.
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

Routen sind mindestens einem nächsten Hop zugeordnet. Wenn sich das Ziel nicht in einem direkt verbundenen Netzwerk befindet, ist der nächste Hop die Adresse des nächsten Routers (oder Netzwerks) im ausgehenden Netzwerk, der Daten am besten an das Ziel weiterleiten kann. Die beste Route ist die Route mit den geringsten Kosten, basierend auf der verwendeten Routingrichtlinie. Jeder nächste Hop kann verwendet werden, um Daten auf dem Pfad an das Ziel weiterzuleiten. Alle Routen, die sich im Besitz eines Clients befinden, nutzen einen gemeinsamen Satz von Next-Hop-Einträgen, die vom Client hinzugefügt wurden.

Jeder nächste Hop wird durch die Adresse des nächsten Hops und den Schnittstellenindex, der zum Erreichen des nächsten Hops verwendet wird, eindeutig identifiziert.

Wenn der nächste Hop selbst nicht direkt verbunden ist, wird er als "remote" nächster Hop markiert. In diesem Fall muss die Weiterleitung eine weitere Suche unter Verwendung der Netzwerkadresse des nächsten Hops ausführen. Diese Suche ist erforderlich, um den "lokalen" nächsten Hop zu finden, der verwendet wird, um den nächsten Remotehop und das Ziel zu erreichen.

Ein Eintrag des nächsten Hops in der Routingtabelle enthält Folgendes:

-   Die Netzwerkadresse des nächsten Hops
-   Der Besitzer des nächsten Hops
-   Der Bezeichner der ausgehenden Schnittstelle
-   Der Status des nächsten Hops
-   Flags, die dem nächsten Hop zugeordnet sind
-   Informationen, die für den Besitzer des nächsten Hops privat sind
-   Ein Handle für das Ziel, das dem nächsten Remotehop entspricht

 

 




