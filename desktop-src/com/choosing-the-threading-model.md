---
title: Auswählen des Threading Modells
description: Auswählen des Threading Modells
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388708"
---
# <a name="choosing-the-threading-model"></a>Auswählen des Threading Modells

Die Auswahl des Threading Modells für ein Objekt hängt von der Funktion des Objekts ab. Ein Objekt, das umfangreiche e/a-Vorgänge unterstützt, bietet möglicherweise die Möglichkeit, eine maximale Reaktion an Clients zu ermöglichen, indem Schnittstellen Aufrufe während der e/a-Latenz zugelassen werden Auf der anderen Seite kann ein Objekt, das mit dem Benutzer interagiert, das Apartment Threading unterstützen, um eingehende com-Aufrufe mit seinen Fenster Vorgängen zu synchronisieren.

Es ist einfacher, Apartment Threading in Single Thread-Apartments zu unterstützen, da com die Synchronisierung pro Rückruf bereitstellt. Das unterstützen von kostenlosem Threading ist schwieriger, da das Objekt die Synchronisierung implementieren muss. die Reaktion an Clients ist jedoch möglicherweise besser, da die Synchronisierung für kleinere Code Abschnitte implementiert werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen über mehrere Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Multithread-Apartments](multithreaded-apartments.md)
</dt> <dt>

[Threading Probleme im Prozess internen Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Single Thread-und Multithread-Kommunikation](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Single Thread-Apartments](single-threaded-apartments.md)
</dt> </dl>

 

 




