---
title: Single-Threaded und Multithread-Kommunikation
description: Single-Threaded und Multithread-Kommunikation
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309692"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Single-Threaded und Multithread-Kommunikation

Ein Client oder Server, der sowohl Single Thread-als auch Multithreadapartments unterstützt, verfügt über ein Multithreadapartment, das alle als frei Thread initialisierten Threads und eine oder mehrere Single Thread-Apartments enthält. Schnittstellen Zeiger müssen zwischen den Apartments gemarshallt werden, können aber ohne Marshalling in einem Apartment verwendet werden. Aufrufe von Objekten in einem Single Thread-Apartment werden durch com synchronisiert. Aufrufe von Objekten im Multithread-Apartment werden nicht durch com synchronisiert.

Alle Informationen zu Single Thread-Apartments gelten für die Threads, die als Apartment Modell gekennzeichnet sind, und alle Informationen zu multithreadwohnungen gelten für alle Threads, die als "frei Thread" gekennzeichnet sind. Apartment Thread Regeln gelten für die Kommunikation zwischen den Apartments und erfordern, dass Schnittstellen Zeiger zwischen Apartments mit Aufrufen von [**comarshalinterthreadinterfaceinstream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) und [**cogetinterfaceandreleasestream gemarshallt**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream)werden, wie in [Single Thread-Apartments](single-threaded-apartments.md)beschrieben.

> [!Note]  
> Einige besondere Überlegungen gelten beim Umgang mit Prozess internen Servern. Weitere Informationen finden Sie unter [Prozess interne Server Threading Probleme](in-process-server-threading-issues.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen über mehrere Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Auswählen des Threading Modells](choosing-the-threading-model.md)
</dt> <dt>

[Multithread-Apartments](multithreaded-apartments.md)
</dt> <dt>

[Threading Probleme im Prozess internen Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Single Thread-Apartments](single-threaded-apartments.md)
</dt> </dl>

 

 




