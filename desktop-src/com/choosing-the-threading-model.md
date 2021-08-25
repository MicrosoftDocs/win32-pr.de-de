---
title: Auswählen des Threadingmodells
description: Auswählen des Threadingmodells
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1966a4b000683bb7549ce9c825051324088fd85c41146137443045785b5e0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896510"
---
# <a name="choosing-the-threading-model"></a>Auswählen des Threadingmodells

Die Auswahl des Threadingmodells für ein Objekt hängt von der Funktion des Objekts ab. Ein Objekt, das umfangreiche E/A-Schaltungen übernimmt, unterstützt möglicherweise Freethreading, um clients eine maximale Antwort zu bieten, indem Schnittstellenaufrufe während der E/A-Latenz zugelassen werden. Andererseits kann ein Objekt, das mit dem Benutzer interagiert, Apartmentthreading unterstützen, um eingehende COM-Aufrufe mit seinen Fenstervorgängen zu synchronisieren.

Es ist einfacher, Apartmentthreading in Singlethread-Apartments zu unterstützen, da COM eine Synchronisierung pro Aufruf ermöglicht. Die Unterstützung von Freethreading ist schwieriger, da das Objekt eine Synchronisierung implementieren muss. Die Antwort auf Clients ist jedoch möglicherweise besser, da die Synchronisierung für kleinere Codeabschnitte implementiert werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen zwischen Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Multithread-Apartment](multithreaded-apartments.md)
</dt> <dt>

[Threadingprobleme beim In-Process-Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Singlethread- und Multithreadkommunikation](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Singlethread-Apartment](single-threaded-apartments.md)
</dt> </dl>

 

 




