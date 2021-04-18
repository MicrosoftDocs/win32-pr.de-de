---
description: Die \_ \_ \_ \_ Schlüsselwörter try und schließlich werden verwendet, um einen Beendigungs Handler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Beendigungs Handlers.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Termination-Handler-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344831"
---
# <a name="termination-handler-syntax"></a>Termination-Handler-Syntax

Die Schlüsselwörter **\_ \_ try** und **\_ \_ schließlich** werden verwendet, um einen Beendigungs Handler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Beendigungs Handlers.


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



Beispiele finden Sie unter [Verwenden eines Beendigungs Handlers](using-a-termination-handler.md).

Wie beim Ausnahmehandler erfordern sowohl der **\_ \_ try** -Block als auch **\_ \_ der-Block** geschweifte Klammern ( {} ), und die Verwendung einer **goto** -Anweisung zum Springen in beide Blöcke ist unzulässig.

Der **\_ \_ try** -Block enthält den überwachten Code Körper, der durch den Beendigungs Handler geschützt wird. Eine Funktion kann über eine beliebige Anzahl von Beendigungs Handlern verfügen, und diese Beendigungs Verarbeitungsblöcke können innerhalb derselben Funktion oder in verschiedenen Funktionen geschachtelt werden.

Der Block wird ausgeführt, wenn die Ablauf Steuerung den **\_ \_ try** -Block **\_ \_** verlässt. Der Block wird jedoch nicht ausgeführt, wenn Sie eine der folgenden Funktionen im **\_ \_ try** **\_ \_ -Block** aufzurufen: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)oder **Abbruch**.

Der **\_ \_ schließlich** -Block wird im Kontext der Funktion ausgeführt, in der sich der Beendigungs Handler befindet. Dies bedeutet, dass der **\_ \_ schließlich** -Block auf die lokalen Variablen der Funktion zugreifen kann. Die Ausführung des **\_ \_ letzten Blocks kann** auf eine der folgenden Weise beendet werden.

-   Ausführung der letzten Anweisung im Block und Fortsetzung der nächsten Anweisung
-   Verwendung einer Control-Anweisung ("**Return**", " **break**", " **Continue**" oder " **goto**")
-   Verwendung von **longjmp** oder einem Sprung zu einem Ausnahmehandler

Wenn die Ausführung des **\_ \_ try** -Blocks aufgrund einer Ausnahme beendet wird, die den Ausnahme Behandlungs Block eines Frame basierten Ausnahme Handlers aufruft, wird **der letzte \_ \_** -Block ausgeführt, bevor der Ausnahme Behandlungs Block ausgeführt wird. Entsprechend führt ein Aufruf der **longjmp** -C-Lauf Zeit Bibliotheksfunktion aus dem **\_ \_ try** -Block dazu, dass **\_ \_ der letzte Block ausgeführt** wird, bevor die Ausführung am Ziel des **longjmp** -Vorgangs fortgesetzt wird. Wenn die Ausführung des **\_ \_ try** -Blocks aufgrund einer Control-Anweisung (**Return**, **break**, **Continue** oder **goto**) beendet **\_ \_** wird, wird der letzte Block ausgeführt.

Mit der [**abnormalbeendigungs**](abnormaltermination.md) -Funktion kann innerhalb des letzten Blocks bestimmt werden, ob der **\_ \_ try** -Block nacheinander beendet wurde – d. h. ob er die schließende geschweifte Klammer (}) erreicht hat. **\_ \_** Das belassen des **\_ \_ try** -Blocks aufgrund eines Aufrufes **longjmp**, das Springen zu einem Ausnahmehandler oder eine **Return**-, **break**-, **Continue**-oder **goto** -Anweisung wird als nicht ordnungsgemäße Beendigung angesehen. Beachten Sie, dass das System nicht sequenziell beendet wird, sondern alle Stapel Rahmen in umgekehrter Reihenfolge durchsucht, um zu bestimmen, ob Beendigungs Handler aufgerufen werden müssen. Dies kann zu Leistungseinbußen führen, da Hunderte von Anweisungen ausgeführt werden.

Um eine ungewöhnliche Beendigung des Beendigungs Handlers zu vermeiden, sollte die Ausführung bis zum Ende des Blocks fortgesetzt werden. Sie können auch die **\_ \_ Leave** -Anweisung ausführen. Mit der **\_ \_ Leave** -Anweisung kann der **\_ \_ try** -Block sofort beendet werden, ohne dass eine ungewöhnliche Beendigung und die Leistungseinbußen entstehen. Überprüfen Sie in der Compilerdokumentation, ob die **\_ \_ Leave** -Anweisung unterstützt wird.

Wenn die **\_ \_ Ausführung des letzten Blocks aufgrund** der **Rückgabe** Steuerungs Anweisung beendet wird, entspricht Sie einer **goto** -Anweisung auf die schließende geschweifte Klammer in der einschließenden Funktion. Daher gibt die einschließende Funktion zurück.

 

 
