---
description: SrW-Sperren (Reader Reader/Writer) ermöglichen es den Threads eines einzelnen Prozesses, auf freigegebene Ressourcen zuzugreifen. Sie sind für Geschwindigkeit optimiert und belegen nur sehr wenig Arbeitsspeicher.
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: SRW-Sperren (Slim Reader/Writer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc478d5f9bbfec1268f65b3e4a7f562b9bdca3d2df21f4570a52782eec9f028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959980"
---
# <a name="slim-readerwriter-srw-locks"></a>SRW-Sperren (Slim Reader/Writer)

SrW-Sperren (Reader Reader/Writer) ermöglichen es den Threads eines einzelnen Prozesses, auf freigegebene Ressourcen zuzugreifen. Sie sind für Geschwindigkeit optimiert und belegen nur sehr wenig Arbeitsspeicher. Reader-Writer-Sperren können nicht prozessübergreifend freigegeben werden.

Leserthreads lesen Daten aus einer freigegebenen Ressource, während Writerthreads Daten in eine freigegebene Ressource schreiben. Wenn mehrere Threads mit einer freigegebenen Ressource lesen und schreiben, können exklusive Sperren wie ein kritischer Abschnitt oder Mutex zu einem Engpass werden, wenn die Readerthreads kontinuierlich ausgeführt werden, Schreibvorgänge jedoch selten sind.

SRW-Sperren bieten zwei Modi, in denen Threads auf eine freigegebene Ressource zugreifen können:

-   **Freigegebener Modus,** der freigegebenen schreibgeschützten Zugriff auf mehrere Readerthreads gewährt, wodurch daten gleichzeitig aus der freigegebenen Ressource gelesen werden können. Wenn Lesevorgänge Schreibvorgänge überschreiten, erhöht diese Parallelität die Leistung und den Durchsatz im Vergleich zu kritischen Abschnitten.
    > [!NOTE]
    > SRW-Sperren im freigegebenen Modus sollten nicht rekursiv erworben werden, da dies zu Deadlocks führen kann, wenn sie mit dem exklusiven Erwerb kombiniert werden.

-   **Exklusiver Modus,** der Lese-/Schreibzugriff auf jeweils einen Writerthread gewährt. Wenn die Sperre im exklusiven Modus eingerichtet wurde, kann kein anderer Thread auf die freigegebene Ressource zugreifen, bis der Writer die Sperre freigibt.
    > [!NOTE]
    > SRW-Sperren im exklusiven Modus können nicht rekursiv bezogen werden. Wenn ein Thread versucht, eine Sperre zu erhalten, die er bereits enthält, schlägt dieser Versuch fehl (für [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)) oder deadlock (für [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)).

In beiden Modi kann eine einzelne SRW-Sperre eingerichtet werden. Readerthreads können sie im freigegebenen Modus abrufen, während Writerthreads sie im exklusiven Modus abrufen können. Es gibt keine Garantie für die Reihenfolge, in der Threads, die den Besitz anfordern, der Besitz gewährt wird. SRW-Sperren sind weder fair noch FIFO.

Eine SRW-Sperre ist die Größe eines Zeigers. Der Vorteil besteht darin, dass der Sperrzustand schnell aktualisiert werden kann. Der Nachteil ist, dass nur sehr wenige Zustandsinformationen gespeichert werden können, sodass SRW-Sperren keine falsche rekursive Verwendung im freigegebenen Modus erkennen. Darüber hinaus kann ein Thread, der eine SRW-Sperre im freigegebenen Modus besitzt, seinen Besitz der Sperre nicht auf den exklusiven Modus aktualisieren.

Der Aufrufer muss eine SRWLOCK-Struktur zuordnen und initialisieren, indem er entweder [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) aufruft (um die Struktur dynamisch zu initialisieren) oder die konstante **SRWLOCK \_ INIT** der Strukturvariablen zuweist (um die Struktur statisch zu initialisieren).

Sie können [Application Verifier](/windows-hardware/drivers/devtest/application-verifier) verwenden, um rekursive (reentrant) Verwendung von SRW-Sperren zu finden.

Im Folgenden finden Sie die SRW-Sperrfunktionen.

| SRW-Sperrfunktion                                                | Beschreibung                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | Erwirbt eine SRW-Sperre im exklusiven Modus.                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | Erwirbt eine SRW-Sperre im freigegebenen Modus.                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | Initialisieren sie eine SRW-Sperre.                                                                                                                           |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | Gibt eine SRW-Sperre frei, die im exklusiven Modus geöffnet wurde.                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | Gibt eine SRW-Sperre frei, die im freigegebenen Modus geöffnet wurde.                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | Standbymodus für die angegebene Bedingungsvariable und Freigabe der angegebenen Sperre als atomarer Vorgang.                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | Versucht, eine SRW-Sperre (Reader/Writer) im exklusiven Modus zu erhalten. Wenn der Aufruf erfolgreich ist, übernimmt der aufrufende Thread den Besitz der Sperre. |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | Versucht, eine SRW-Sperre (Reader/Writer) im freigegebenen Modus zu erhalten. Wenn der Aufruf erfolgreich ist, übernimmt der aufrufende Thread den Besitz der Sperre.    |

 
