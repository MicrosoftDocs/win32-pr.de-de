---
description: Dienstanbieter-Designer sollten versuchen, die Ausführungszeit von synchronen Vorgängen kurz zu halten.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Synchrone Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e399fcef1ffba574305b70aee05d7430bcd84746458198b3d33ed6bb0848747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760687"
---
# <a name="synchronous-requests"></a>Synchrone Anforderungen

Dienstanbieter-Designer sollten versuchen, die Ausführungszeit von synchronen Vorgängen kurz zu halten. Beispielsweise gibt es einen "Open"-Vorgang, der zur Initialisierungszeit aufgerufen wird und den Dienstanbieter und TAPI für nachfolgende Vorgänge auf einem Gerät vorbereitet. Ein Dienstanbieter, dessen Implementierung auf den Clientcomputer und einen dedizierten Server aufgeteilt ist, kann sich sicher sein, dass er mit seinem Remoteserver kommunizieren kann. Die Implementierung von "Open" kann datenstrukturen einfach zuordnen und initialisieren, um das Gerät darzustellen und zurückzugeben, wodurch die End-to-End-Kommunikation verschoben wird, bis ein echter Vorgang angefordert wird.

Bei einer solchen "optimistischen" Implementierung eines synchronen Vorgangs können später Ressourceneinschränkungen oder Remotekommunikationsfehler auftreten. Im Allgemeinen kann selbst ein "konservativer" Ansatz diese Probleme nicht vollständig verhindern. Dienstanbieter-Designer müssen den besten Kompromiss zwischen Zuverlässigkeit und Leistung auswählen. Ein Fehler dieser Art sollte nach Möglichkeit ordnungsgemäß behandelt werden. Aus Sicht von TSPI-Geräten sollten sie für "Buchhaltungszwecke" gültig bleiben, auch wenn sie den Fehlerstatus für einen angeforderten Vorgang zurückgeben.

Die Implementierung eines optimistischen Ansatzes für synchrone Anforderungen sollte nicht auf Kosten der richtigen Semantik für den Vorgang erfolgen. Kehren Sie zum Beispiel "Öffnen" zurück. Wenn das Öffnen eines Geräts um eine gebundene, nicht löschbare Ressource wie Kommunikationsports konkurrieren und reservieren muss, sollte dies wahrscheinlich auch dann erfolgen, wenn es zeitaufwändig ist.

**TAPI 2.x:** Ein Vorgang, der synchron abgeschlossen wird, führt die gesamte Verarbeitung im Funktionsaufruf durch, der von der Anwendung ausgeführt wird. Die Funktion gibt je nach Erfolg oder Fehler unterschiedliche Werte zurück:

-   **Synchroner Erfolg.** Wenn die Anforderung oder der Dienst, der der Funktion entspricht, erfolgreich ausgeführt wurde, gibt die Funktion 0 (null) zurück, was auf den Erfolg hinweist. Alle Werte, die als Ergebnis des Funktionsaufrufs geschrieben werden, sind zuverlässig und können sofort verwendet werden.
-   **Synchroner Fehler.** Wenn die Funktion einen Fehler erkennt und die Anforderung nicht ausgeführt wird, wird eine negative Fehlernummer zurückgegeben, um den Fehler zu identifizieren.

 

 



