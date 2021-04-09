---
description: Ein liniengerät kann einen Pool homogener Ressourcen (Channels) darstellen, die zum Einrichten von Aufrufen verwendet werden. Auf einem Client Computer bietet ein TSP in der Regel Zugriff auf ein oder mehrere Linien Geräte.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Linien Konfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722dab15763822f6535783ecc8bc18e681e13ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863091"
---
# <a name="line-configurations"></a>Linien Konfigurationen

Ein liniengerät kann einen Pool homogener Ressourcen (Channels) darstellen, die zum Einrichten von Aufrufen verwendet werden. Auf einem Client Computer bietet ein TSP in der Regel Zugriff auf ein oder mehrere Linien Geräte.

Im folgenden finden Sie einige Beispiele dafür, wie ein Dienstanbieter verschiedene Konfigurationen modellieren kann:

**Beispiel 1:** Eine einzelne Töpfe-Linie in den Computer zentrierten oder Telefon zentrierten Verbindungs Modellen. Das einfachste Modell ist ein einzeilige Gerät mit einem Kanal.

**Beispiel 2:** Eine einzelne BRI-ISDN-Linie in den Computer zentrierten oder Telefon zentrierten Verbindungs Modellen. Der Dienstanbieter verfügt über eine Reihe von Optionen, um dies zu modellieren, z. b.:

-   Modellieren Sie die BRI-Linie als einzeilige Geräte mit einem Pool von zwei B-Kanälen, der die Kombination beider Kanäle zum Einrichten von 128 Kbit/s-aufrufen ermöglicht.
-   Modellieren Sie jeden B-Channel als separates Geräte Gerät, und lassen Sie nicht zu, dass beide Kanäle zu einem einzelnen 128 Kbit/s-Kanal kombiniert werden.
-   Modellieren Sie die BRI-Verbindung als zwei separate Linien Geräte, die jeweils bis zu zwei Kanäle von einem freigegebenen Pool mit zwei B-Kanälen zeichnen.
-   Modellieren Sie als drei zeilige Geräte, eine für jeden B-Kanal und eine für die Kombination. In den letzten beiden Modellen können Ressourcen zu unterschiedlichen Zeiten anderen Geräte Geräten zugewiesen werden.

**Beispiel 3:** In Client-/Serversystemen kann ein Pool von Telefonanschlüssen, die an einen Server angeschlossen sind, über ein lokales Netzwerk von mehreren Client Computern gemeinsam genutzt werden. Der Pool kann so verwaltet werden, dass jeder Client Arbeitsstation eine maximale Anzahl von Linien Geräten (Kontingent) zugewiesen wird. Es ist nicht ungewöhnlich, dass die Summe aller Kontingente die Gesamtzahl der Zeilen überschreitet. Außerdem kann ein angegebener Client mit einem Kontingent gleich 2 mit den Ports 1 und 2 gleichzeitig und den Ports 7 und 11 zu einem späteren Zeitpunkt erfüllt werden. Der Dienstanbieter für den Pool kann diese Anordnung modellieren, indem jeder Client Arbeitsstation Zugriff auf Geräte mit zwei Zeilen erteilt wird.

Angenommen, die Konfiguration von Dienstanbietern für einen bestimmten Computer ist so, dass dieser bestimmte Dienstanbieter eine **deviceidbase** von 3 erhält. Dies bedeutet, dass die (fixierten) Geräte Bezeichner für diesen Client 3 und 4 sind. Wenn die Anwendung später die TAPI 2-Funktion [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) für Gerät 3 und erneut für Gerät 4 aufruft, sollte davon ausgegangen werden, dass die Gerätefunktionen für jedes dieser Geräte konstant sind, da es sich hierbei um das Gerätemodell handelt. Solange die Dienstanbieter Konfiguration des jeweiligen Computers konstant bleibt, bleiben die Geräte Bezeichner auf der TSPI-Ebene konstant, auch wenn der Server die Port Zuweisungen ändert. Für serverbasierte Geräte, die wie in Beispiel 3 beschrieben in einem Pool zusammengefasst sind, gilt dies nur für Linien Geräte, die über identische Gerätefunktionen verfügen. Wenn die Dienstanbieter Konfiguration des jeweiligen Computers geändert wird, sodass dieser Dienstanbieter eine andere **deviceidbase** erhält, ändern sich die Geräte-IDs entsprechend.

**Beispiel 4:** Link zu Host wechseln:

-   Um persönliche Telefonie für jeden Desktop bereitzustellen, kann der Dienstanbieter die PBX-Verbindung mit dem Computer als Einzel zeilige Geräte mit einem Kanal modellieren. Auf jedem Client Computer ist ein Zeilen Gerät verfügbar.
-   Jede Station eines Drittanbieters könnte als separates liniengerät modelliert werden. Dies ermöglicht es der Anwendung, Aufrufe auf anderen Stationen zu steuern. Diese Lösung erfordert, dass die Anwendung jede Zeile öffnet, die Sie bearbeiten oder überwachen möchten. Dies kann in Ordnung sein, wenn nur eine kleine Anzahl von Zeilen von Interesse ist, aber viel mehr Aufwand verursachen kann, wenn eine große Anzahl von Zeilen beteiligt ist.
-   Der Satz aller Drittanbieter-Stationen könnte als Einzel zeilengerät modelliert werden, dem eine Adresse (Telefonnummer) pro Station zugewiesen ist. Es muss nur ein einzelnes Gerät geöffnet werden, das die Überwachung und Steuerung aller Adressen in der Zeile (alle Stationen) bereitstellt. Um einen Rückruf für eine dieser Stationen durchzuführen, muss die Anwendung nur die Adresse der Station für den Vorgang angeben, der den-Vorgang ausführt. Es sind keine zusätzlichen offenen Vorgänge erforderlich. Diese Modellierung impliziert, dass alle Stationen über die gleichen Gerätefunktionen verfügen, obwohl Ihre Adress Funktionen sich unterscheiden können.

> [!Note]  
> Alle diese Beispiele sind einfach unterschiedliche Möglichkeiten, wie ein Dienstanbieter die Zuordnung von Linien Geräteverhalten in eine physische Realisierung implementieren kann.

 

 

 
