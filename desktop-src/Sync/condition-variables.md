---
description: Bedingungs Variablen sind Synchronisierungs primitive, mit denen Threads warten können, bis eine bestimmte Bedingung eintritt. Bedingungs Variablen sind Benutzermodus-Objekte, die nicht Prozess übergreifend freigegeben werden können.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Bedingungs Variablen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368892"
---
# <a name="condition-variables"></a>Bedingungs Variablen

Bedingungs Variablen sind Synchronisierungs primitive, mit denen Threads warten können, bis eine bestimmte Bedingung eintritt. Bedingungs Variablen sind Benutzermodus-Objekte, die nicht Prozess übergreifend freigegeben werden können.

Mit Bedingungs Variablen können Threads eine Sperre atomisch freigeben und in den Ruhezustand wechseln. Sie können mit kritischen Abschnitten oder SRW-Sperren (Slim Reader/Writer) verwendet werden. Bedingungs Variablen unterstützen Vorgänge, die wartende Threads "reaktivieren" oder "alle reaktivieren". Nachdem ein Thread aktiviert wurde, erhält er die Sperre erneut, die er freigegeben hat, als der Thread in den Ruhezustand wechselt.

Beachten Sie, dass der Aufrufer eine Bedingungs **\_ Variablen** Struktur zuordnen und diese initialisieren muss, indem [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) aufgerufen wird (um die Struktur dynamisch zu initialisieren), oder die Konstante Bedingungs **\_ Variable \_ Init** der Struktur Variablen zuzuweisen (um die Struktur statisch zu initialisieren).

**Windows Server 2003 und Windows XP:** Bedingungs Variablen werden nicht unterstützt.

Es folgen die Bedingungs Variablen Funktionen.



| Bedingungs Variablen Funktion                                        | BESCHREIBUNG                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Initialisiert eine Bedingungs Variable.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Gibt für die angegebene Bedingungs Variable aus und gibt den angegebenen kritischen Abschnitt als atomarischen Vorgang frei. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Gibt für die angegebene Bedingungs Variable aus und gibt die angegebene SRW-Sperre als atomarischen Vorgang frei.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Aktiviert alle Threads, die auf die angegebene Bedingungs Variable warten.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Aktiviert einen einzelnen Thread, der auf die angegebene Bedingungs Variable wartet.                                             |



 

Der folgende Pseudo Code veranschaulicht das typische Verwendungs Muster von Bedingungs Variablen.

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

Beispielsweise würde die Funktion in einer Implementierung einer Reader-/Schreibsperre `TestPredicate` überprüfen, ob die aktuelle Sperranforderung mit den vorhandenen Besitzern kompatibel ist. Wenn dies der Fall ist, erhalten Sie die Sperre. andernfalls der Standbymodus. Ein ausführlicheres Beispiel finden Sie unter [verwenden](using-condition-variables.md)von Bedingungs Variablen.

Bedingungs Variablen unterliegen falschen aufwecken (die nicht mit einem expliziten Aktivierungs Modus verknüpft sind) und gestohlenen aufwecken (ein anderer Thread wird vor dem aufwachten Thread verwaltet). Daher sollten Sie ein Prädikat (in der Regel in einer **while** -Schleife) nach dem zurückkehren eines Ruhe Zustands erneut überprüfen.

Sie können andere Threads mithilfe von [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) oder [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) entweder innerhalb oder außerhalb der der Bedingungs Variablen zugeordneten Sperre aktivieren. Es ist in der Regel besser, die Sperre freizugeben, bevor andere Threads aktiviert werden, um die Anzahl von Kontext Schaltern zu verringern.

Häufig ist es praktisch, mehr als eine Bedingungs Variable mit derselben Sperre zu verwenden. Beispielsweise kann eine Implementierung einer Reader-/Writer-Sperre einen einzelnen kritischen Abschnitt verwenden, aber separate Bedingungs Variablen für Reader und Writer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Bedingungs Variablen](using-condition-variables.md)
</dt> </dl>

 

 
