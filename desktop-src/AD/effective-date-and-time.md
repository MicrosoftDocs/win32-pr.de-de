---
title: Gültigkeitsdatum und Uhrzeit
description: Das Gültigkeitsdatum und die Uhrzeit sind eine Vermeidungsstrategie, die eine Versions Abweichung und partielle Updates verhindert, indem die effektiven Daten von Informationen zu einem späteren Zeitpunkt verzögert werden, wenn die Änderung eine hohe Wahrscheinlichkeit hat, dass Sie vollständig repliziert wird.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036378"
---
# <a name="effective-date-and-time"></a>Gültigkeitsdatum und Uhrzeit

Das Gültigkeits *Datum und die Uhrzeit* sind eine Vermeidungsstrategie, die eine Versions Abweichung und partielle Updates verhindert, indem die effektiven Daten von Informationen zu einem späteren Zeitpunkt verzögert werden, wenn die Änderung eine hohe Wahrscheinlichkeit hat, dass Sie vollständig repliziert wird. Zum Implementieren von Gültigkeitsdatums Angaben müssen die Anwendungs Objekte einen Gültigkeitsdatum-Zeitstempel enthalten, der ausgefüllt wird, wenn das Objekt erstellt oder geändert wird. Consumer der Objekte überprüfen den Zeitstempel und verzögern die Verwendung der Objekte, bis das Datum und die Uhrzeit erreicht sind.

Wichtige Hinweise:

-   Anwendungen, die diesen Ansatz auswählen, müssen sicherstellen, dass es eine Reihe von anwendbaren Daten gibt, die verwendet werden können, bis die aktualisierten Objekte wirksam werden.
-   Der verteilte Zeit Dienst in Windows NT 4,0 sorgt dafür, dass die Uhren der verbundenen Windows 2000 synchronisiert werden. Es ist jedoch kein Zeit-Dienst perfekt, es gibt also ein kleines Fenster für die Versions Neigung.
-   Wenn Sie ein gutes Gültigkeitsdatum festlegen, werden die Gesamt Replikations Latenz für das betreffende verteilte System vorausgesetzt. Eine gute Faustregel für Gültigkeits Daten in einem stabilen Netzwerk ist die (Uhrzeit des Updates) + (2 \* (durchschnittliche Gesamt Latenz)). Bei einem System, dessen Gesamt Latenz durchschnittlich 4 Stunden beträgt, ist also eine Verzögerung von 8 Stunden angemessen.
-   In einem instabilen Netzwerk ist das Ermitteln eines "guten" Werts für effektive Datumsangaben sehr viel schwieriger, da die Latenz stark variabel sein kann. Das Gültigkeitsdatum ist in einem instabilen Netzwerk in der Kombination mit anderen Vermeidungs-oder Erkennungs Strategien, wie z. b. Prüfsummen oder Konsistenz-GUIDs, die höchste Wirksamkeit Weitere Informationen finden Sie unter [Prüfsummen und Objekt Anzahl](checksums-and-object-counts.md).

 

 




