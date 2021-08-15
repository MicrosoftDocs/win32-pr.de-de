---
description: Bedingungsvariablen sind Synchronisierungsprimitiven, mit denen Threads warten können, bis eine bestimmte Bedingung auftritt. Bedingungsvariablen sind Benutzermodusobjekte, die nicht prozessübergreifend freigegeben werden können.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Bedingungsvariablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d7ee98b4f5c5a65e633f7d1647b6c624840f9740efb639959c1500bec591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886360"
---
# <a name="condition-variables"></a>Bedingungsvariablen

Bedingungsvariablen sind Synchronisierungsprimitiven, mit denen Threads warten können, bis eine bestimmte Bedingung auftritt. Bedingungsvariablen sind Benutzermodusobjekte, die nicht prozessübergreifend freigegeben werden können.

Bedingungsvariablen ermöglichen Threads, atomisch eine Sperre freizugeben und in den Ruhezustand zu gelangen. Sie können mit kritischen Abschnitten oder SRW-Sperren (Reader/Writer) verwendet werden. Bedingungsvariablen unterstützen Vorgänge, die wartende Threads "reaktivieren". Nachdem ein Thread weckt wurde, erhält er die Sperre erneut, die er freigegeben hat, wenn der Thread in den Ruhezustand übergegangen ist.

Beachten Sie, dass der Aufrufer eine **CONDITION \_ VARIABLE-Struktur** zuordnen und initialisieren muss, indem er entweder [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) aufruft (um die Struktur dynamisch zu initialisieren) oder die konstante **CONDITION VARIABLE \_ \_ INIT** der Strukturvariablen zuweist (um die Struktur statisch zu initialisieren).

**Windows Server 2003 und Windows XP:** Bedingungsvariablen werden nicht unterstützt.

Im Folgenden sind die Bedingungsvariablenfunktionen.



| Bedingungsvariablenfunktion                                        | BESCHREIBUNG                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Initialisiert eine Bedingungsvariable.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Standbymodus für die angegebene Bedingungsvariable und Freigabe des angegebenen kritischen Abschnitts als atomarer Vorgang. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Standbymodus für die angegebene Bedingungsvariable und Freigabe der angegebenen SRW-Sperre als atomarer Vorgang.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Aktiviert alle Threads, die auf die angegebene Bedingungsvariable warten.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Aktiviert einen einzelnen Thread, der auf die angegebene Bedingungsvariable wartet.                                             |



 

Der folgende Pseudocode veranschaulicht das typische Verwendungsmuster von Bedingungsvariablen.

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

Beispielsweise würde die Funktion in einer Implementierung einer Reader-/Writersperre `TestPredicate` überprüfen, ob die aktuelle Sperranforderung mit den vorhandenen Besitzern kompatibel ist. Wenn dies der Grund ist, erhalten Sie die Sperre. Andernfalls standby. Ein ausführlicheres Beispiel finden Sie unter [Verwenden von Bedingungsvariablen.](using-condition-variables.md)

Bedingungsvariablen unterliegen falschen Aktivierungen (die nicht einer expliziten Aktivierung zugeordnet sind) und gestohlenen Aktivierungen (ein anderer Thread verwaltet die Ausführung vor dem aufgeweckten Thread). Daher sollten Sie ein Prädikat (in  der Regel in einer while-Schleife) erneut überprüfen, nachdem ein Standbyvorgang zurückgegeben wurde.

Sie können andere Threads mit [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) oder [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) entweder innerhalb oder außerhalb der Sperre reaktivieren, die der Bedingungsvariablen zugeordnet ist. Es ist in der Regel besser, die Sperre freizugeben, bevor Sie andere Threads aufrufen, um die Anzahl der Kontextwechsel zu reduzieren.

Es ist häufig praktisch, mehrere Bedingungsvariablen mit der gleichen Sperre zu verwenden. Beispielsweise kann eine Implementierung einer Reader-/Writersperre einen einzelnen kritischen Abschnitt, aber separate Bedingungsvariablen für Leser und Writer verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Bedingungsvariablen](using-condition-variables.md)
</dt> </dl>

 

 
