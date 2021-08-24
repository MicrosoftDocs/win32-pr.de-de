---
title: Single-Threaded und Multithreadkommunikation
description: Single-Threaded und Multithreadkommunikation
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1096ff2cd5916bf16b00a746c2e6de6ce22008258c6e200c2858c0430cb3f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129832"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Single-Threaded und Multithreadkommunikation

Ein Client oder Server, der Singlethread- und Multithread-Apartments unterstützt, verfügt über ein Multithreadapartment, das alle als Freethreading initialisierten Threads und ein oder mehrere Singlethread-Apartments enthält. Schnittstellenzeiger müssen zwischen Apartments gemarshallt werden, können aber ohne Marshalling innerhalb eines Apartments verwendet werden. Aufrufe von -Objekten in einem Singlethread-Apartment werden von COM synchronisiert. Aufrufe von Objekten im Multithread-Apartment werden von COM nicht synchronisiert.

Alle Informationen zu Singlethread-Apartments gelten für die als Apartmentmodell markierten Threads, und alle Informationen zu Multithread-Apartments gelten für alle Threads, die als Freethreading markiert sind. Apartmentthreadingregeln gelten für die Kommunikation zwischen Apartments und erfordern, dass Schnittstellenzeiger zwischen Apartments mit Aufrufen von [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) und [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream)gemarshallt werden, wie in [Singlethread-Apartment](single-threaded-apartments.md)beschrieben.

> [!Note]  
> Beim Umgang mit In-Process-Servern gelten einige besondere Überlegungen. Weitere Informationen finden Sie unter [In-Process Server Threading Issues](in-process-server-threading-issues.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf Schnittstellen zwischen Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Auswählen des Threadingmodells](choosing-the-threading-model.md)
</dt> <dt>

[Multithread-Apartment](multithreaded-apartments.md)
</dt> <dt>

[Threadingprobleme beim In-Process-Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Singlethread-Apartment](single-threaded-apartments.md)
</dt> </dl>

 

 




