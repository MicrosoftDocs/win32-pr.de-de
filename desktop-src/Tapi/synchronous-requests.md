---
description: Dienstanbieter-Designer sollten versuchen, die Ausführungszeit synchroner Vorgänge kurz zu halten.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Synchrone Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3684b1fa8ea2bca1b7fb777663f2c4e50ffd36a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360874"
---
# <a name="synchronous-requests"></a>Synchrone Anforderungen

Dienstanbieter-Designer sollten versuchen, die Ausführungszeit synchroner Vorgänge kurz zu halten. Beispielsweise ist ein "offener" Vorgang zur Initialisierungs Zeit aufgerufen, der den Dienstanbieter und TAPI für nachfolgende Vorgänge auf einem Gerät vorbereitet. Ein Dienstanbieter, dessen Implementierung zwischen dem Client Computer und einem dedizierten Server aufgeteilt wird, hat möglicherweise ein angemessenes Vertrauen, dass er mit seinem Remote Server kommunizieren kann. Die Implementierung von "Open" kann einfach Datenstrukturen zuordnen und initialisieren, um das Gerät darzustellen, und die End-to-End-Kommunikation wird so lange verschoben, bis ein echter Vorgang angefordert wird.

Bei allen solchen "optimistischen" Implementierungen eines synchronen Vorgangs können später Ressourcenbeschränkungen oder Remote Kommunikationsfehler auftreten. Im Allgemeinen kann ein "konservativer" Ansatz diese Probleme nicht vollständig verhindern. Dienstanbieter-Designer müssen den besten Kompromiss zwischen Zuverlässigkeit und Leistung auswählen. Ein Fehler dieser Art sollte möglichst ordnungsgemäß behandelt werden. Aus Sicht der TSPI-Geräte sollten Sie auch dann für "Buchhaltungszwecke" gültig bleiben, wenn Sie den Fehlerstatus für einen angeforderten Vorgang zurückgeben.

Das Implementieren eines optimistischen Ansatzes für synchrone Anforderungen sollte nicht auf Kosten der korrekten Semantik für den Vorgang durchgeführt werden. Wenn Sie zum Beispiel "Open" (öffnen) wechseln und ein Gerät mit einer geringen, nicht shardbaren Ressource, wie z. b. Kommunikationsports, konkurrieren müssen, sollte dies wahrscheinlich auch dann der Fall sein, wenn es zeitaufwändig ist.

**TAPI 2. x:** Ein Vorgang, der synchron abgeschlossen wird, führt die gesamte Verarbeitung im Funktions aufrut durch, der von der Anwendung ausgeführt wird. Die Funktion gibt je nach Erfolg oder Fehler unterschiedliche Werte zurück:

-   **Synchroner Erfolg.** Wenn die Anforderung oder der Dienst, der der Funktion entspricht, erfolgreich ausgeführt wurde, gibt die Funktion 0 (null) zurück, was den Erfolg angibt. Alle Werte, die als Ergebnis des Funktions Aufrufes geschrieben werden, sind zuverlässig und können sofort verwendet werden.
-   **Synchroner Fehler.** Wenn die Funktion einen Fehler erkennt und die Anforderung nicht durchgeführt wird, wird eine negative Fehlernummer zurückgegeben, um den Fehler zu identifizieren.

 

 



