---
title: DNS (Übersicht)
description: DNS ist ein Branchenstandarddienst, mit dem Computer in einem IP-basierten Netzwerk (Internet Protocol) gefunden werden.
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a47874606491c1baf5c52ca7934d7e0c3156a6ab99f9726e6c000d9eb3cb65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967470"
---
# <a name="dns-overview"></a>DNS (Übersicht)

DNS ist ein Branchenstandarddienst, mit dem Computer in einem IP-basierten Netzwerk (Internet Protocol) gefunden werden. IP-Netzwerke wie das Internet und Windows 2000-Netzwerke basieren auf zahlenbasierten Adressen wie 207.46.131.137, um Informationen über das Netzwerk zu verfähren. Netzwerkbenutzer verwenden zeichenbasierte Namen, z. `www.microsoft.com` B. . Daher ist es erforderlich, Zeichen oder benutzerfreundliche Adressen ( ) in die zahlenbasierten Adressen `www.microsoft.com` (207.46.131.137) zu übersetzen, die das Netzwerk erkennen kann. DNS ist der Dienst ihrer Wahl in Windows 2000, um Ressourcen zu suchen und in die entsprechenden IP-Adressen zu übersetzen.

DNS verwendet eine spezielle Datenbank mit Ressourceneinträgen, die häufig einfach als RRs bezeichnet wird, um auf Abfragen zur Clientnamensauflösung zu reagieren. Vor DNS wurde die Namensauflösung im Internet mit der [*Hostdatei*](h-gly.md)erreicht, bei der es sich um manuell erstellte Dateien handelt, die Hostnamen IP-Adressen zugeordnet haben.

Wenn dem Netzwerk ein neuer Client hinzugefügt wurde, musste ein Administrator die Hostdatei manuell aktualisieren und diese Datei dann auf alle anderen Computer im Netzwerk kopieren (replizieren), damit der neue Host von allen erreicht werden konnte. Mit dem Anwächst des Internets reichte diese Form der Namensauflösung eindeutig nicht aus. es war zu verwaltungsintensiv, und es wurde nicht [*skaliert.*](s-gly.md) Die Hostdatei wurde gerade größer, und da sie einen flachen Namensraum [*verwendet*](f-gly.md) hat (siehe auch [Name Space),](name-space.md)konnte sie nicht partitioniert werden und musste vollständig verteilt werden. Die Lösung war DNS.

-   DNS hat den flachen Namensraum der Hostdatei durch einen [*hierarchischen Namensraum ersetzt.*](h-gly.md) Mit einem hierarchischen Namensraum können Informationen zu Hostnamen und IP-Adressen partitioniert und verteilt werden. auf diese Weise wird Skalierbarkeit erreicht. In der fiktiven widgets.products.microsoft.com kann beispielsweise die Verantwortung für die Namensauflösung partitioniert werden, sodass verschiedene Server die Namensauflösung für verschiedene Teile des Namensraums verarbeiten können:
    -   Ein Server kann für die Auflösung des ersten Teils (microsoft.com) verantwortlich sein und dann die Namensauflösungsanforderung an den nächsten DNS-Server in der Hierarchie weiterverenden.
    -   Der nächste DNS-Server kann für die Auflösung des nächsten Teils des Namensraums (Produkte) verantwortlich sein.
    -   Schließlich kann die Anforderung an einen dritten DNS-Server weitergeleitet werden, der für die Auflösung des letzten Teils des Namens (Widgets) zuständig ist.

DNS-Server in jedem Teil des hierarchischen Namensraums müssen eine Datenbank mit Ressourceneinträgen für Hosts verwalten, jedoch nur in ihrem Teil der Hierarchie. Daher verwalten die Server (oder Server) im Produktteil von widgets.products.microsoft.com RRs nur für die Produkte, die Teil des hierarchischen Namensraums sind – nicht für den microsoft.com-Teil oder die Widgets, die Teil des Namensraums sind.

 

 




