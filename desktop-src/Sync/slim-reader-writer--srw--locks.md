---
description: SRW-Sperren (Slim Reader/Writer) ermöglichen es den Threads eines einzelnen Prozesses, auf freigegebene Ressourcen zuzugreifen. Sie sind für die Geschwindigkeit optimiert und belegen sehr wenig Arbeitsspeicher.
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: SRW-Sperren (Slim Reader/Writer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d76d956e1425531eae43b0daa6817002a92bc
ms.sourcegitcommit: 663239b4560bfd5314e86901c65805c9bbcab07d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "106349743"
---
# <a name="slim-readerwriter-srw-locks"></a>SRW-Sperren (Slim Reader/Writer)

SRW-Sperren (Slim Reader/Writer) ermöglichen es den Threads eines einzelnen Prozesses, auf freigegebene Ressourcen zuzugreifen. Sie sind für die Geschwindigkeit optimiert und belegen sehr wenig Arbeitsspeicher. Schlanke Lese-/Schreibsperren können nicht Prozess übergreifend gemeinsam verwendet werden.

Lesethreads lesen Daten aus einer freigegebenen Ressource, während Writer-Threads Daten in eine freigegebene Ressource schreiben. Wenn mehrere Threads Lese-und Schreibvorgänge unter Verwendung einer freigegebenen Ressource ausführen, können exklusive Sperren, wie z. b. ein kritischer Abschnitt oder Mutex, zu einem Engpass werden, wenn die Lesethreads fortlaufend ausgeführt werden, Schreibvorgänge jedoch selten

SRW-Sperren bieten zwei Modi, in denen Threads auf eine freigegebene Ressource zugreifen können:

-   Der Modus "frei **gegeben**", der freigegebenen schreibgeschützten Zugriff auf mehrere Lesethreads gewährt, sodass Sie Daten aus der gemeinsam genutzten Ressource gleichzeitig lesen können. Wenn Lesevorgänge Schreibvorgänge überschreiten, erhöht diese Parallelität die Leistung und den Durchsatz im Vergleich zu kritischen Abschnitten.
    > [!NOTE]
    > SRW-Sperren im Modus "freigegeben" sollten nicht rekursiv abgerufen werden, da dies zu Deadlocks führen kann, wenn Sie mit exklusiver Übernahme kombiniert werden

-   **Exklusiver Modus**, der Lese-/Schreibzugriff auf einen Schreib Thread gleichzeitig gewährt. Wenn die Sperre im exklusiven Modus abgerufen wurde, kann kein anderer Thread auf die freigegebene Ressource zugreifen, bis der Writer die Sperre freigibt.
    > [!NOTE]
    > SRW-Sperren im exklusiven Modus können nicht rekursiv abgerufen werden. Wenn ein Thread versucht, eine Sperre abzurufen, die er bereits enthält, schlägt dieser Versuch fehl (für [**tryacquiresrwlockexclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)) oder Deadlock (für [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)).

Eine einzelne SRW-Sperre kann in beiden Modi abgerufen werden. Lesethreads können Sie im Modus "freigegeben" abrufen, während Writer-Threads Sie im exklusiven Modus abrufen können. Es gibt keine Garantie für die Reihenfolge, in der Threads, die den Besitz anfordern, den Besitz erhalten. SRW-Sperren sind weder fair noch FIFO.

Eine SRW-Sperre ist die Größe eines Zeigers. Der Vorteil besteht darin, dass es schnell ist, den Sperr Status zu aktualisieren. Der Nachteil ist, dass nur wenige Zustandsinformationen gespeichert werden können, sodass SRW-Sperren nicht die falsche rekursive Verwendung im freigegebenen Modus erkennen. Außerdem kann ein Thread, der eine SRW-Sperre im freigegebenen Modus besitzt, nicht den Besitz der Sperre auf den exklusiven Modus aktualisieren.

Der Aufrufer muss eine SRWLOCK-Struktur zuordnen und initialisieren, indem er entweder [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) aufruft (um die Struktur dynamisch zu initialisieren), oder die Konstante **SRWLOCK \_ Init** der Struktur Variablen zuweisen (um die Struktur statisch zu initialisieren).

Sie können [Application Verifier](/windows-hardware/drivers/devtest/application-verifier) verwenden, um die rekursive Verwendung von SRW-Sperren zu suchen.

Im folgenden finden Sie die SRW-Sperr Funktionen.

| SRW-Sperrfunktion                                                | BESCHREIBUNG                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | Ruft eine SRW-Sperre im exklusiven Modus ab.                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | Ruft eine SRW-Sperre im freigegebenen Modus ab.                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | Initialisieren Sie eine SRW-Sperre.                                                                                                                           |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | Gibt eine SRW-Sperre frei, die im exklusiven Modus geöffnet wurde.                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | Gibt eine SRW-Sperre frei, die im freigegebenen Modus geöffnet wurde.                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | Gibt für die angegebene Bedingungs Variable den Ruhezustand an und gibt die angegebene Sperre als atomarischen Vorgang frei.                                                |
| [**Tryacquiresrwlockexclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | Versucht, eine SRW-Sperre (Slim Reader/Writer) im exklusiven Modus zu erhalten. Wenn der Aufruf erfolgreich ist, übernimmt der aufrufende Thread den Besitz der Sperre. |
| [**Tryacquiresrwlockshared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | Versucht, eine SRW-Sperre (Slim Reader/Writer) im freigegebenen Modus zu erhalten. Wenn der Aufruf erfolgreich ist, übernimmt der aufrufende Thread den Besitz der Sperre.    |

 
