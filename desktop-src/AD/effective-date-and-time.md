---
title: Datum und Uhrzeit des Gültigkeitsdatums
description: Das Effektive Datum und die effektive Uhrzeit ist eine Strategie zur Vermeidung von Versionsabweichungen und Teilaktualisierungen, indem die effektiven Daten der Informationen auf einen bestimmten Zeitpunkt in der Zukunft zurückgesetzt werden, wenn die Änderung eine hohe Wahrscheinlichkeit hat, vollständig repliziert zu werden.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d95c80627c878bbc9d8cb6ac16436e6dae3e12cf262e797724cd5053f371ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695363"
---
# <a name="effective-date-and-time"></a>Datum und Uhrzeit des Gültigkeitsdatums

*Das Effektive Datum und* die effektive Uhrzeit ist eine Strategie zur Vermeidung von Versionsabweichungen und Teilaktualisierungen, indem die effektiven Daten der Informationen auf einen bestimmten Zeitpunkt in der Zukunft zurückgesetzt werden, wenn die Änderung eine hohe Wahrscheinlichkeit hat, vollständig repliziert zu werden. Um effektive Datumsangaben zu implementieren, müssen die Anwendungsobjekte einen effektiven Datumszeitstempel enthalten, der beim Erstellen oder Ändern des Objekts ausgefüllt wird. Consumer der Objekte überprüfen den Zeitstempel und ziehen die Verwendung der Objekte zurück, bis das Datum und die Uhrzeit erreicht sind.

Wichtige Hinweise:

-   Anwendungen, die diesen Ansatz wählen, müssen sicherstellen, dass es eine Reihe von anwendbaren Daten gibt, die verwendet werden müssen, bis die aktualisierten Objekte wirksam werden.
-   Der verteilte Zeitdienst in Windows NT 4.0 hält die Uhren der verbundenen Windows 2000 synchronisiert. Kein Zeitdienst ist jedoch perfekt, sodass es ein kleines Fenster für Versionsschiefe gibt.
-   Das Festlegen eines guten Gültigkeitsdatums setzt voraus, dass Sie über die gesamte Replikationslatenz für das betreffende verteilte System informiert sind. In einem stabilen Netzwerk ist eine gute Faustregel für effektive Datumsangaben (Zeitpunkt des Updates) + (2 \* (durchschnittliche Gesamtlatenz)). Für ein System, dessen Gesamtlatenz durchschnittlich 4 Stunden beträgt, ist eine Verzögerung von 8 Stunden also angemessen.
-   In einem instabilen Netzwerk ist die Bestimmung eines "guten" Werts für effektive Datumsangaben wesentlich schwieriger, da die Latenz stark variieren kann. Das Gültigkeitsdatum ist in einem instabilen Netzwerk am "effektivsten", wenn es mit anderen Vermeidungs- oder Erkennungsstrategien wie Prüfsummen oder Konsistenz-GUIDs kombiniert wird. Weitere Informationen finden Sie unter [Prüfsummen und Objektanzahl.](checksums-and-object-counts.md)

 

 




