---
title: DNS (Übersicht)
description: DNS ist ein branchenübliches Dienst, der zum Auffinden von Computern in einem IP-basierten Netzwerk (Internet Protocol) verwendet wird.
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470807a5775b022834a3ca2f0ee3f91db8bdd5de
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104219413"
---
# <a name="dns-overview"></a>DNS (Übersicht)

DNS ist ein branchenübliches Dienst, der zum Auffinden von Computern in einem IP-basierten Netzwerk (Internet Protocol) verwendet wird. IP-Netzwerke, wie z. b. die Netzwerke Internet und Windows 2000, basieren auf Zahlen basierten Adressen, wie z. b. 207.46.131.137, um Informationen im gesamten Netzwerk zu überarbeiten. Netzwerk Benutzer basieren auf Zeichen basierten Namen, z. b `www.microsoft.com` .. Daher ist es erforderlich, Zeichen-oder benutzerfreundliche Adressen ( `www.microsoft.com` ) in die Zahlen basierten Adressen (207.46.131.137) zu übersetzen, die das Netzwerk erkennen kann. DNS ist der bevorzugte Dienst in Windows 2000, um nach Ressourcen zu suchen und diese in die entsprechenden IP-Adressen zu übersetzen.

DNS verwendet eine spezialisierte Datenbank mit Ressourcen Einträgen, die in der Regel einfach als RRS bezeichnet werden, um auf Client-namens Auflösungs Abfragen zu reagieren. Vor DNS wurde die Namensauflösung im Internet mit der [*Hosts-Datei*](h-gly.md)erreicht, die manuell erstellte Dateien sind, die Hostnamen mit IP-Adressen verknüpft haben.

Wenn ein neuer Client dem Netzwerk hinzugefügt wurde, musste ein Administrator die Hostdatei manuell aktualisieren und diese Datei dann auf alle anderen Computer im Netzwerk kopieren (replizieren), damit der neue Host vollständig erreicht werden kann. Als das Internet wächst, war diese Form der Namensauflösung deutlich unzureichend. Es war zu viel Verwaltungs intensiv und konnte nicht [*skaliert*](s-gly.md)werden. Die Hostdatei ist jetzt größer, und da Sie einen [*flachen*](f-gly.md) Namespace verwendet hat (siehe [auch](name-space.md)Namespace), konnte Sie nicht partitioniert werden und musste vollständig verteilt werden. Die Lösung war DNS.

-   DNS hat den flachen namens Bereich der Hosts-Datei durch einen [*hierarchischen*](h-gly.md)Namespace ersetzt. Mit einem hierarchischen Namespace können Informationen zu Hostnamen und IP-Adressen partitioniert und verteilt werden. Daher wird die Skalierbarkeit erreicht. In der fiktiven Widgets.Products.Microsoft.com-Domäne kann die Verantwortung für die Namensauflösung beispielsweise so partitioniert werden, dass verschiedene Server die Namensauflösung für verschiedene Teile des Namespace verarbeiten können:
    -   Ein Server kann für die Auflösung des ersten Teils zuständig sein (Microsoft.com) und kann dann die Anforderung zur Namensauflösung an den nächsten DNS-Server in der Hierarchie weiterleiten.
    -   Der nächste DNS-Server kann dafür verantwortlich sein, den nächsten Teil des Namensraums (Produkte) aufzulösen.
    -   Schließlich kann die Anforderung an einen dritten DNS-Server weitergeleitet werden, der für die Auflösung des letzten Teils des Namens (Widgets) zuständig ist.

DNS-Server in jedem Teil des hierarchischen namessourcen müssen eine Datenbank mit Ressourcen Einträgen für Hosts verwalten, aber nur in Ihrem Teil der Hierarchie. Der Server (oder die Server) im Products-Teil von Widgets.Products.Microsoft.com verwaltet RRS nur für die Produkte, die Teil des hierarchischen Namespace sind – nicht für den Microsoft.com-Teil oder den Widgets-Teil des Namespace.

 

 




