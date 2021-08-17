---
description: Im Allgemeinen ist keine Synchronisierung erforderlich, wenn Sie über ein Singlethread-Apartment (STA) verfügen, da das Apartment die Synchronisierung für Sie bereitstellt.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: COM+-Synchronisierungskonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4153c02a5fcd9a0990459e360d239396e7de30cff22316da70f73002e73d6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129002"
---
# <a name="com-synchronization-concepts"></a>COM+-Synchronisierungskonzepte

Im Allgemeinen ist keine Synchronisierung erforderlich, wenn Sie über ein Singlethread-Apartment (STA) verfügen, da das Apartment die Synchronisierung für Sie bereitstellt. Die Synchronisierung wird wichtig, wenn Sie über ein Multithread-Apartment (MTA) und ein Freethread-Objekt verfügen. In der Vergangenheit mussten Freethread-Objekte sperren. Sie können das Sperren vermeiden, indem Sie das Synchronisierungsattribut für eine Komponente festlegen.

Die Synchronisierung weist die folgenden Eigenschaften auf:

-   Ermöglicht es einem Aufrufer, die Komponente gleichzeitig einzugeben.
-   Verhindert den Prozess- oder computerübergreifenden Fluss.
-   Fließt innerhalb eines Prozesses von Komponente zu Komponente.
-   Ermöglicht die Wiederinvarianz desselben Aufrufers.

Im Gegensatz zu Apartments umfassen Aktivitäten Kontexte aus mehreren Prozessen und Hosts. Die Synchronisierung bestimmt, welche Aktivität ein -Objekt enthält. Objekte können sich in einer der folgenden Aktivitäten befinden:

-   Aktivität des Erstellers
-   Neue Aktivität
-   Keine Aktivität

COM+ stellt die Parallelität durch eine Reihe von Sperren für jede Aktivität sicher. Wenn ein Aufrufer versucht, eine synchronisierte COM+-Komponente einzugeben, die bereits von einem anderen Aufrufer verwendet wird, wird der Aufruf blockiert, bis die Sperre aufgehoben wird. Dieses Blockierungsverhalten führt nicht zu einem Time out und kann nicht für time out konfiguriert werden. Wenn die Sperre nicht verwendet wird, wird die Sperre aktiviert und der Aufruf verarbeitet. Nach Abschluss des Abschlusses wird die Sperre für den nächsten Aufrufer aufgehoben. Um Deadlocks zu verhindern, verwaltet COM+ den Zugriff auf alle Objekte über Aktivitäten hinweg durch eine geschachtelte Reihe von Aufrufen, die im gesamten Netzwerk verkettet sind.

COM+ stellt die folgenden Synchronisierungseinstellungen bereit:

-   Disabled
-   Nicht unterstützt
-   Unterstützt
-   Erforderlich
-   Requires New

> [!Note]  
> Einige Synchronisierungseinstellungen funktionieren in Verbindung mit anderen COM+-Komponenteneinstellungen. Die Synchronisierung ist beispielsweise erforderlich, wenn der [JIT-Aktivierungsdienst (COM+)](com--just-in-time-activation.md) aktiviert ist. JIT ist erforderlich, wenn Sie Transaktionen aktivieren. Daher erfordert die [COM+-Transaktionsverarbeitung](com--transactions.md) auch eine Synchronisierung. Daher müssen Klassen mit der Einstellung JIT=True auch die Einstellung Synchronization=Required oder Synchronization=RequiresNew aufweisen.

 

Anweisungen zum Festlegen von Synchronisierungsoptionen mithilfe des Verwaltungstools "Komponentendienste" finden Sie unter [Festlegen des Synchronisierungsattributs](setting-the-synchronization-attribute.md).

Weitere Informationen zur Verwendung der COM+-Verwaltungsbibliothek zum Festlegen von Synchronisierungsoptionen finden Sie unter [Automatisieren der COM+-Verwaltung.](automating-com--administration.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Synchronisierungsaufgaben](com--synchronization-tasks.md)
</dt> </dl>

 

 



