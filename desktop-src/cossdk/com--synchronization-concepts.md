---
description: Im Allgemeinen ist die Synchronisierung nicht erforderlich, wenn Sie über ein Single Thread-Apartment (STA) verfügen, da das Apartment die Synchronisierung für Sie bereitstellt.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Com+-Synchronisierungs Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748880"
---
# <a name="com-synchronization-concepts"></a>Com+-Synchronisierungs Konzepte

Im Allgemeinen ist die Synchronisierung nicht erforderlich, wenn Sie über ein Single Thread-Apartment (STA) verfügen, da das Apartment die Synchronisierung für Sie bereitstellt. Die Synchronisierung wird wichtig, wenn Sie über ein Multithread-Apartment (MTA) und ein Freethread-Objekt verfügen. In der Vergangenheit mussten frei Thread Objekte Sperren behandeln. Sie können die Verwendung von Sperren ausschließen, indem Sie das Synchronisierungs Attribut für eine Komponente festlegen.

Die Synchronisierung verfügt über die folgenden Eigenschaften:

-   Ermöglicht einem Aufrufer, die Komponente gleichzeitig einzugeben.
-   Verhindert, dass der Flow Prozess übergreifend oder Computer übergreifend ist.
-   Fließt von Komponente zu Komponente innerhalb eines Prozesses.
-   Ermöglicht den erneuten eintreten desselben Aufrufers.

Im Gegensatz zu-Apartments umfassen Aktivitäten Kontexte zwischen mehreren Prozessen und Hosts. Durch die Synchronisierung wird bestimmt, welche Aktivität ein Objekt enthält. -Objekte können sich in einer der folgenden Aktivitäten befinden:

-   Aktivität des Erstellers
-   Neue Aktivität
-   Keine Aktivität

Com+ stellt Parallelität durch eine Reihe von Sperren für jede Aktivität sicher. Wenn ein Aufrufer versucht, eine synchronisierte COM+-Komponente einzugeben, die bereits von einem anderen Aufrufer verwendet wird, wird der Aufruf blockiert, bis die Sperre aufgehoben wird. Bei diesem blockierenden Verhalten tritt kein Timeout auf, und es kann nicht konfiguriert werden, dass ein Timeout auftritt. Wenn die Sperre nicht verwendet wird, wird die Sperre abgerufen, und der-Befehl wird verarbeitet. Nach Abschluss der Ausführung wird die Sperre für den nächsten Aufrufer freigegeben. Um Deadlocks zu verhindern, verwaltet com+ den Zugriff auf alle Objekte über Aktivitäten hinweg durch eine Reihe von im Netzwerk verketteten aufrufen.

Com+ bietet die folgenden Synchronisierungs Einstellungen:

-   Disabled
-   Nicht unterstützt
-   Unterstützt
-   Erforderlich
-   Requires New

> [!Note]  
> Einige Synchronisierungs Einstellungen funktionieren in Verbindung mit anderen COM+-Komponenten Einstellungen. Beispielsweise ist eine Synchronisierung erforderlich, wenn der [com+-Just-in-time (JIT)-Aktivierungs](com--just-in-time-activation.md) Dienst aktiviert ist. JIT ist erforderlich, wenn Sie Transaktionen aktivieren. Daher muss die com+- [Transaktionsverarbeitung](com--transactions.md) ebenfalls synchronisiert werden. Daher müssen Klassen mit der Einstellung "JIT = true" auch die Einstellung "Synchronisierung = erforderlich" oder "Synchronisierung = Requirements SNEW" aufweisen.

 

Anweisungen zum Festlegen von Synchronisierungs Optionen mithilfe des Verwaltungs Programms Komponenten Dienste finden Sie unter [Festlegen des Synchronisierungs Attributs](setting-the-synchronization-attribute.md).

Weitere Informationen zum Festlegen von Synchronisierungs Optionen mithilfe der com+-Verwaltungs Bibliothek finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Synchronisierungs Tasks](com--synchronization-tasks.md)
</dt> </dl>

 

 



