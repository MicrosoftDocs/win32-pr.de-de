---
description: Ein Mutex-Objekt ist ein Synchronisierungs Objekt, dessen Zustand auf "signalisiert" festgelegt ist, wenn es nicht im Besitz eines Threads ist, und nicht signalisiert, wenn es im Besitz ist.
ms.assetid: eca0795a-1fd0-4034-9d61-9416670919cf
title: Mutex-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e84c17ba3e99e888f7d1e9137a7f24a4d78ce2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866616"
---
# <a name="mutex-objects"></a>Mutex-Objekte

Ein *Mutex-Objekt* ist ein Synchronisierungs Objekt, dessen Zustand auf "signalisiert" festgelegt ist, wenn es nicht im Besitz eines Threads ist, und nicht signalisiert, wenn es im Besitz ist. Nur jeweils ein Thread kann ein Mutex-Objekt besitzen, dessen Name von der Tatsache stammt, dass es hilfreich ist, sich gegenseitig ausschließenden Zugriff auf eine freigegebene Ressource zu koordinieren. Um beispielsweise zu verhindern, dass zwei Threads gleichzeitig in den gemeinsam genutzten Speicher schreiben, wartet jeder Thread auf den Besitz eines Mutex-Objekts, bevor der Code ausgeführt wird, der auf den Speicher zugreift. Nach dem Schreiben in den freigegebenen Speicher gibt der Thread das Mutex-Objekt frei.

Ein Thread verwendet die Funktion " [**foratemutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) " oder " [**foratemutexex**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa) ", um ein Mutex-Objekt zu erstellen. Der erstellende Thread kann den unmittelbaren Besitz des Mutex-Objekts anfordern und kann auch einen Namen für das Mutex-Objekt angeben. Es kann auch ein unbenanntes Mutex erstellt werden. Weitere Informationen zu den Namen von Mutex-, Ereignis-, Semaphore-und Timer-Objekten finden Sie unter [prozessübergreifende Synchronisierung](interprocess-synchronization.md).

Threads in anderen Prozessen können ein Handle für ein vorhandenes benanntes Mutex-Objekt öffnen, indem Sie den Namen in einem Aufrufs der [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) -Funktion angeben. Um ein Handle an einen unbenannten Mutex an einen anderen Prozess zu übergeben, verwenden Sie die [**duplialisierandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion oder die über-und untergeordnete handle-Vererbung.

Jeder Thread mit einem Handle für ein Mutex-Objekt kann eine der [Wait-Funktionen](wait-functions.md) verwenden, um den Besitz des Mutex-Objekts anzufordern. Wenn sich das Mutex-Objekt im Besitz eines anderen Threads befindet, blockiert die wait-Funktion den anfordernden Thread, bis der besitzende Thread das Mutex-Objekt mithilfe der [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) -Funktion freigibt. Der Rückgabewert der wait-Funktion gibt an, ob die Funktion aus einem anderen Grund als dem Zustand des Mutex zurückgegeben wurde, der auf signalisiert festgelegt wird.

Wenn mehr als ein Thread auf einen Mutex wartet, wird ein wartender Thread ausgewählt. Nehmen Sie keine Voraussetzung für eine FIFO-Reihenfolge (First in, First Out). Externe Ereignisse wie z. b. kernelmodusapcs können die Warte Reihenfolge ändern.

Nachdem ein Thread den Besitz eines Mutex erlangt hat, kann er denselben Mutex in wiederholten Aufrufen der [Wait-Funktionen](wait-functions.md) angeben, ohne dessen Ausführung zu blockieren. Dadurch wird verhindert, dass ein Thread sich selbst blockiert, während er auf einen Mutex wartet, den er bereits besitzt. Um seinen Besitz unter solchen Umständen freizugeben, muss der Thread [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) einmal für jedes Mal aufgerufen werden, wenn der Mutex die Bedingungen einer wait-Funktion erfüllt hat.

Wenn ein Thread beendet wird, ohne den Besitz eines Mutex-Objekts freizugeben, wird das Mutex-Objekt als abgebrochen betrachtet. Ein wartender Thread kann den Besitz eines abgebrochenen Mutex-Objekts abrufen, aber die wait-Funktion gibt den Vorgang **\_ abgebrochen** zurück, um anzugeben, dass das Mutex-Objekt abgebrochen wird. Ein abgebrochenes Mutex-Objekt gibt an, dass ein Fehler aufgetreten ist und dass sich alle vom Mutex-Objekt geschützten freigegebenen Ressourcen in einem nicht definierten Zustand befinden. Wenn der Thread fortgesetzt wird, als ob das Mutex-Objekt nicht abgebrochen wurde, wird er nicht mehr als abgebrochen betrachtet, nachdem der Thread seinen Besitz freigegeben hat. Dadurch wird das normale Verhalten wieder hergestellt, wenn ein Handle für das Mutex-Objekt später in einer wait-Funktion angegeben wird.

Beachten Sie, dass [wichtige Abschnitts Objekte](critical-section-objects.md) eine Synchronisierung ähnlich der von Mutex-Objekten bereitstellen, mit dem Unterschied, dass wichtige Abschnitts Objekte nur von den Threads eines einzelnen Prozesses verwendet werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Mutex-Objekten](using-mutex-objects.md)
</dt> </dl>

 

 
