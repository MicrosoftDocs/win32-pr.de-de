---
description: Ein Liniengerät kann einen Pool homogener Ressourcen (Kanäle) darstellen, die zum Einrichten von Aufrufen verwendet werden. Auf einem Clientcomputer bietet ein TSP in der Regel Zugriff auf ein oder mehrere Liniengeräte.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Zeilenkonfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d3705854a5bd485dba01452a3885e52c3c2d0baf0d495a65a2db24d75894eeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126250"
---
# <a name="line-configurations"></a>Zeilenkonfigurationen

Ein Liniengerät kann einen Pool homogener Ressourcen (Kanäle) darstellen, die zum Einrichten von Aufrufen verwendet werden. Auf einem Clientcomputer bietet ein TSP in der Regel Zugriff auf ein oder mehrere Liniengeräte.

Hier sind einige Beispiele dafür, wie ein Dienstanbieter verschiedene Konfigurationen modellieren kann:

**Beispiel 1:** Eine einzelne HOCHS-Linie in den computerzentrierten oder telefonzentrierten Verbindungsmodellen. Das unkomplizierteste Modell ist ein Einzeilengerät mit einem Kanal.

**Beispiel 2:** Eine einzelne BRI-ISDN-Linie in den computer- oder telefonzentrierten Verbindungsmodellen. Der Dienstanbieter verfügt über eine Reihe von Optionen, wie er dies modellieren möchte, z. B.:

-   Modellieren Sie die BRI-Linie als Einzeilengerät mit einem Pool aus zwei B-Kanälen, mit dem beide Kanäle kombiniert werden können, um Aufrufe mit 128 KBit/s zu erstellen.
-   Modellieren Sie jeden B-Kanal als separates Liniengerät, und lassen Sie nicht zu, dass beide Kanäle in einem einzelnen Kanal mit 128 KBit/s kombiniert werden.
-   Modellieren Sie die BRI-Verbindung als zwei separate Liniengeräte, die jeweils bis zu zwei Kanäle aus einem gemeinsam genutzten Pool mit zwei B-Kanälen erstellen.
-   Modellieren Sie als drei Liniengeräte, eines für jeden B-Kanal und eines für die Kombination. In den letzten beiden Modellen können Ressourcen unterschiedlichen Liniengeräten zu unterschiedlichen Zeiten zugewiesen werden.

**Beispiel 3:** In Client-/Serversystemen kann ein Pool von Telefonanschlüssen, die an einen Server angefügt sind, von mehreren Clientcomputern über ein lokales Netzwerk gemeinsam genutzt werden. Der Pool kann verwaltet werden, um jeder Clientarbeitsstation eine maximale Anzahl von Liniengeräten (Kontingent) zu zuweisen. Es ist nicht ungewöhnlich, dass die Summe aller Kontingente die Gesamtzahl der Zeilen überschreitet. Darüber hinaus kann ein gegebener Client mit einem Kontingent von 2 erfüllt werden, indem die Ports 1 und 2 gleichzeitig und die Ports 7 und 11 zu einem späteren Zeitpunkt verwendet werden. Der Dienstanbieter für den Pool kann diese Anordnung modellieren, indem er jeder Clientarbeitsstation Zugriff auf zwei Liniengeräte gibt.

Angenommen, die Konfiguration von Dienstanbietern für einen bestimmten Computer ist so, dass dieser bestimmte Dienstanbieter eine **DeviceIDBase von** 3 erhält. Dies bedeutet, dass die (festen) Gerätebezeichner für diesen Client 3 und 4 sind. Wenn die Anwendung später die TAPI 2-Funktion [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) für Gerät 3 und erneut für Gerät 4 aufruft, sollte davon ausgegangen werden können, dass die Gerätefunktionen für jedes dieser Geräte konstant sind, da dies das Gerätemodell ist. Solange die Dienstanbieterkonfiguration des jeweiligen Computers konstant bleibt, bleiben die Geräte-IDs, die auf TSPI-Ebene angezeigt werden, konstant, auch wenn der Server die Portzuordnungen ändert. Für serverbasierte Geräte, die wie in Beispiel 3 beschrieben in einem Pool verwendet werden, gilt dies nur für Liniengeräte mit identischen Gerätefunktionen. Wenn die Dienstanbieterkonfiguration des angegebenen Computers so geändert wird, dass dieser Dienstanbieter eine andere **DeviceIDBase** erhält, ändern sich die Gerätebezeichner entsprechend.

**Beispiel 4:** Switch-to-Host-Link:

-   Um persönliche Telefonie für jeden Desktop zu bieten, könnte der Dienstanbieter die PBX-Linie, die mit dem Computer gekoppelt ist, als Einzeilengerät mit einem Kanal modellieren. Auf jedem Clientcomputer ist ein Liniengerät verfügbar.
-   Jede Station eines Drittanbieters könnte als separates Liniengerät modelliert werden. Dadurch kann die Anwendung Aufrufe an anderen Stationen steuern. Diese Lösung erfordert, dass die Anwendung jede Zeile öffnet, die sie bearbeiten oder überwachen möchte. Dies kann in Ordnung sein, wenn nur eine kleine Anzahl von Zeilen von Interesse ist, kann aber bei einer großen Anzahl von Zeilen viel Mehraufwand verursachen.
-   Die Gruppe aller Stationen von Drittanbietern könnte als Einzeilengerät modelliert werden, dem eine Adresse (Telefonnummer) pro Station zugewiesen ist. Es muss nur ein einzelnes Gerät geöffnet werden, das die Überwachung und Steuerung aller Adressen auf der Linie (alle Stationen) bietet. Um einen Aufruf an einer dieser Stationen zu senden, muss die Anwendung nur die Adresse der Station für den Vorgang angeben, der den Aufruf vor sich hat. Es sind keine zusätzlichen offenen Vorgänge erforderlich. Diese Modellierung impliziert, dass alle Stationen die gleichen Funktionen für Liniengeräte haben, obwohl ihre Adressfunktionen unterschiedlich sein können.

> [!Note]  
> All diese Beispiele sind einfach unterschiedliche Möglichkeiten, wie ein Dienstanbieter die Zuordnung des Liniengeräteverhaltens zu einer physischen Umsetzung implementieren kann.

 

 

 
