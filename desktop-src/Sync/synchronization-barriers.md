---
description: Eine Synchronisierungs Barriere ermöglicht es mehreren Threads zu warten, bis alle Threads einen bestimmten Ausführungs Zeitpunkt erreicht haben, bevor ein Thread fortgesetzt wird.
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: Synchronisierungs Barrieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4276f0bbc5a10eef391c12cc51ebd475e563bd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217984"
---
# <a name="synchronization-barriers"></a>Synchronisierungs Barrieren

Eine Synchronisierungs Barriere ermöglicht es mehreren Threads zu warten, bis alle Threads einen bestimmten Ausführungs Zeitpunkt erreicht haben, bevor ein Thread fortgesetzt wird. Synchronisierungs Barrieren können nicht Prozess übergreifend gemeinsam genutzt werden.

Synchronisierungs Barrieren sind für Berechnungen in Phasen nützlich, bei denen Threads, die denselben Code parallel ausführen, eine Phase ausführen müssen, bevor Sie mit der nächsten fortfahren.

Rufen Sie zum Erstellen einer Synchronisierungs Barriere die [**initializesynchronizationbarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) -Funktion auf, und geben Sie eine maximale Anzahl von Threads und die Häufigkeit an, mit der ein Thread vor dem blockieren gedreht werden soll. Starten Sie dann die Threads, die die Barriere verwenden werden. Nachdem jeder Thread seine Arbeit beendet hat, ruft er [**entersynchronizationbarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) auf, um auf die Barriere zu warten. Die **entersynchronizationbarrier** -Funktion blockiert jeden Thread so lange, bis die Anzahl der Threads, die in der Barriere blockiert werden, die maximale Thread Anzahl für die Barriere erreicht. zu diesem Zeitpunkt werden von **entersynchronizationbarrier** alle Threads blockiert. Die Funktion " **entersynchronizationbarrier** " gibt für genau einen der Threads, die in die Barriere eingetreten sind, **true** zurück und gibt für alle anderen Threads **false** zurück.

Um eine Synchronisierungs Barriere freizugeben, wenn Sie nicht mehr benötigt wird, wenden Sie sich an das [**Delta-cetesynchronizationbarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier) Es ist sicher, dass diese Funktion sofort nach dem Aufrufen von " [**entersynchronizationbarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) " aufgerufen wird, da diese Funktion sicherstellt, dass alle Threads die Barriere vor der Freigabe nicht mehr verwenden.

Wenn eine Synchronisierungs Barriere nie gelöscht wird, können Threads das Flag für **Synchronisierungs \_ Barriere \_ \_ ohne \_ Löschung** angeben, wenn Sie die Grenze erreichen. Alle Threads, die die Barriere verwenden, müssen dieses Flag angeben. Wenn kein Thread vorhanden ist, wird das Flag ignoriert. Dieses Flag bewirkt, dass die Funktion die zusätzliche Arbeit überspringt, die für die Lösch Sicherheit erforderlich ist, wodurch die Leistung verbessert werden kann. Beachten Sie, dass das Löschen einer Barriere, während dieses Flag wirksam ist, zu einem ungültigen Handle-Zugriff und einem oder mehreren dauerhaft blockierten Threads führen kann.

 

 



