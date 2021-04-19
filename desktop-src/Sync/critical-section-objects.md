---
description: Ein kritisches Abschnitts Objekt stellt eine Synchronisierung ähnlich der von einem Mutex-Objekt bereit, mit dem Unterschied, dass ein kritischer Abschnitt nur von den Threads eines einzelnen Prozesses verwendet werden kann.
ms.assetid: 2ec11a42-3d12-4d60-9dd7-dc38926d56e1
title: Kritische Abschnittsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcada1f2ddbc6d370445f36a3dbd51c5c9f54bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359187"
---
# <a name="critical-section-objects"></a>Kritische Abschnittsobjekte

Ein *kritisches Abschnitts Objekt* stellt eine Synchronisierung ähnlich der von einem Mutex-Objekt bereit, mit dem Unterschied, dass ein kritischer Abschnitt nur von den Threads eines einzelnen Prozesses verwendet werden kann. Kritische Abschnitts Objekte können nicht Prozess übergreifend gemeinsam verwendet werden.

Ereignis-, Mutex-und Semaphor-Objekte können auch in einer Einzel Prozess Anwendung verwendet werden, aber wichtige Abschnitts Objekte bieten einen etwas schnelleren und effizienteren Mechanismus für die Synchronisierung gegenseitiger Ausschlüsse (eine prozessorspezifische Test-und Set-Anweisung). Ebenso wie ein Mutex-Objekt kann ein kritisches Abschnitts Objekt jeweils nur jeweils einem Thread zugewiesen werden, wodurch es sinnvoll ist, eine freigegebene Ressource vor gleichzeitigem Zugriff zu schützen. Anders als bei einem Mutex-Objekt gibt es keine Möglichkeit, zu erkennen, ob ein kritischer Abschnitt abgebrochen wurde.

Ab Windows Server 2003 mit Service Pack 1 (SP1) rufen Threads, die auf einen kritischen Abschnitt warten, den kritischen Abschnitt nicht auf der Grundlage von First-Come, First-Service ab. Diese Änderung erhöht die Leistung für den meisten Code erheblich. Einige Anwendungen sind jedoch von der FIFO-Reihenfolge (First in, First Out) abhängig und können bei aktuellen Versionen von Windows schlecht oder gar nicht verwendet werden (z. b. Anwendungen, die kritische Abschnitte als Raten Limits verwendet haben). Um sicherzustellen, dass Ihr Code weiterhin ordnungsgemäß funktioniert, müssen Sie möglicherweise eine weitere Synchronisierungs Ebene hinzufügen. Angenommen, Sie verfügen über einen Producer-Thread und einen Consumerthread, der ein kritisches Abschnitts Objekt verwendet, um Ihre Arbeit zu synchronisieren. Erstellen Sie zwei Ereignis Objekte, eines für jeden Thread, mit dem signalisiert wird, dass es für den anderen Thread bereit ist, fortzufahren. Der Consumer-Thread wartet, bis der Producer sein Ereignis signalisiert, bevor er in den kritischen Abschnitt wechselt, und der Producer-Thread wartet, bis der Consumer-Thread sein Ereignis signalisiert, bevor er in den kritischen Abschnitt wechselt. Nachdem jeder Thread den kritischen Abschnitt verlassen hat, signalisiert er dem Ereignis, den anderen Thread freizugeben.

**Windows Server 2003 und Windows XP:** Threads, die auf einen kritischen Abschnitt warten, werden einer Warteschlange hinzugefügt. Sie werden aktiviert und erhalten im Allgemeinen den kritischen Abschnitt in der Reihenfolge, in der Sie der Warteschlange hinzugefügt wurden. Wenn Threads dieser Warteschlange jedoch schnell genug hinzugefügt werden, kann die Leistung beeinträchtigt werden, da die Zeit zum Wecken der einzelnen wartenden Threads benötigt wird.

Der Prozess ist dafür verantwortlich, den von einem kritischen Abschnitt verwendeten Arbeitsspeicher zuzuordnen. Dies erfolgt in der Regel durch einfaches Deklarieren einer Variablen vom Typ **Critical \_ section**. Bevor der Thread des Prozesses ihn verwenden kann, initialisieren Sie den kritischen Abschnitt mithilfe der [**InitializeCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsection) -oder [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) -Funktion.

Ein Thread verwendet die Funktion " [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) " oder " [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) ", um den Besitz eines kritischen Abschnitts anzufordern. Er verwendet die [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) -Funktion, um den Besitz eines kritischen Abschnitts freizugeben. Wenn das Objekt des kritischen Abschnitts momentan einem anderen Thread gehört, wartet " **EnterCriticalSection** " unbegrenzt auf den Besitz. Wenn dagegen ein Mutex-Objekt für den gegenseitigen Ausschluss verwendet wird, akzeptieren die [Wait-Funktionen](wait-functions.md) ein angegebenes Timeout Intervall. Die **TryEnterCriticalSection** -Funktion versucht, einen kritischen Abschnitt einzugeben, ohne den aufrufenden Thread zu blockieren.

Wenn ein Thread im Besitz eines kritischen Abschnitts ist, kann er zusätzliche Aufrufe an " [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) " oder " [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) " durchführen, ohne die Ausführung zu blockieren. Dadurch wird verhindert, dass ein Thread sich selbst blockiert, während er auf einen kritischen Abschnitt wartet, den er bereits besitzt. Um den Besitz freizugeben, muss der Thread [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) einmal für jedes Mal aufgerufen werden, wenn er in den kritischen Abschnitt eingetreten ist. Es gibt keine Garantie für die Reihenfolge, in der wartende Threads den Besitz des kritischen Abschnitts erhalten.

Ein Thread verwendet die [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) -Funktion oder die [**setcriticalsectionspincount**](/windows/win32/api/synchapi/nf-synchapi-setcriticalsectionspincount) -Funktion, um eine Spin-Anzahl für das kritische Abschnitts Objekt anzugeben. Wenn ein Thread versucht, einen wichtigen, gesperrten Abschnitt abzurufen, wechselt der Thread in eine Schleife, prüft, ob die Sperre freigegeben wurde, und wenn die Sperre nicht freigegeben wird, wechselt der Thread in den Standbymodus. Auf Systemen mit einem Prozessor wird die Spin-Anzahl ignoriert, und der kritische Abschnitt Spin count wird auf 0 (null) festgelegt. Wenn der kritische Abschnitt auf Multiprozessorsystemen nicht verfügbar ist, ruft der aufrufende Thread *dwSpinCount* -Zeiten auf, bevor er einen Warte Vorgang für ein Semaphor ausführt, das dem kritischen Abschnitt zugeordnet ist. Wenn der kritische Abschnitt während des drehvorgangs frei wird, vermeidet der aufrufenden Thread den warte Vorgang.

Jeder Thread des Prozesses kann die [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection) -Funktion verwenden, um die Systemressourcen freizugeben, die beim Initialisieren des kritischen Abschnitts Objekts zugeordnet werden. Nachdem diese Funktion aufgerufen wurde, kann das Objekt für den kritischen Abschnitt nicht für die Synchronisierung verwendet werden.

Wenn ein Objekt im Besitz eines kritischen Abschnitts ist, sind die Threads, die auf den Besitz in einem " [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection)"-Befehl warten, nur betroffen. Threads, die nicht warten, können weiterhin ausgeführt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mutex-Objekte](mutex-objects.md)
</dt> <dt>

[Verwenden von kritischen Abschnitts Objekten](using-critical-section-objects.md)
</dt> </dl>

 

 
