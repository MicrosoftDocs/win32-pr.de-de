---
description: Eine Synchronisierungsbarriere ermöglicht es mehreren Threads, zu warten, bis alle Threads einen bestimmten Ausführungspunkt erreicht haben, bevor ein Thread fortgesetzt wird.
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: Synchronisierungsbarrieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1247d7ab3b20d4fe89763aea0429d742e8ce1c4d11030088316d4e9f3272556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885982"
---
# <a name="synchronization-barriers"></a>Synchronisierungsbarrieren

Eine Synchronisierungsbarriere ermöglicht es mehreren Threads, zu warten, bis alle Threads einen bestimmten Ausführungspunkt erreicht haben, bevor ein Thread fortgesetzt wird. Synchronisierungsbarrieren können nicht prozessübergreifend gemeinsam genutzt werden.

Synchronisierungsbarrieren sind nützlich für stufenweise Berechnungen, bei denen Threads, die denselben Code parallel ausführen, alle eine Phase abschließen müssen, bevor sie mit der nächsten fortfahren.

Um eine Synchronisierungsbarriere zu erstellen, rufen Sie die [**InitializeSynchronizationBarrier-Funktion**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) auf, und geben Sie eine maximale Anzahl von Threads und die Anzahl an, die ein Thread drehen soll, bevor er blockiert wird. Starten Sie dann die Threads, die die Barriere verwenden. Nachdem jeder Thread seine Arbeit abgeschlossen hat, ruft er [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) auf, um an der Barriere zu warten. Die **EnterSynchronizationBarrier-Funktion** blockiert jeden Thread, bis die Anzahl der in der Barriere blockierten Threads die maximale Threadanzahl für die Barriere erreicht. An diesem Punkt entsperrt **EnterSynchronizationBarrier** alle Threads. Die **EnterSynchronizationBarrier-Funktion** gibt **TRUE** für genau einen der Threads zurück, der in die Barriere gelangt ist, und **gibt FALSE** für alle anderen Threads zurück.

Um eine Synchronisierungsbarriere freizugeben, wenn sie nicht mehr benötigt wird, rufen [**Sie DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)auf. Es ist sicher, diese Funktion sofort nach dem Aufruf von [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) aufzurufen, da diese Funktion sicherstellt, dass alle Threads die Barriere nicht mehr verwenden, bevor sie freigegeben wird.

Wenn eine Synchronisierungsbarriere nie gelöscht wird, können Threads das **FLAG SYNCHRONIZATION \_ BARRIER \_ FLAGS NO \_ \_ DELETE** angeben, wenn sie die Barriere erreichen. Alle Threads, die die Barriere verwenden, müssen dieses Flag angeben. Wenn dies für einen Thread nicht der Fall ist, wird das Flag ignoriert. Dieses Flag bewirkt, dass die Funktion die zusätzliche Arbeit überspringt, die für die Löschsicherheit erforderlich ist, was die Leistung verbessern kann. Beachten Sie, dass das Löschen einer Barriere während dieses Flags zu einem ungültigen Handlezugriff und einem oder mehreren dauerhaft blockierten Threads führen kann.

 

 



