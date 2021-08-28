---
description: Die \_ \_ Schlüsselwörter try und except \_ \_ werden verwendet, um einen framebasierten Ausnahmehandler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Ausnahmehandlers.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Exception-Handler Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd24b3ffc84a3469c7c8d97ce505a0292ee538ea8f0b9c1d604bf34f65203ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912740"
---
# <a name="exception-handler-syntax"></a>Exception-Handler Syntax

Die **\_ \_ Schlüsselwörter try** und **\_ \_ except** werden verwendet, um einen framebasierten Ausnahmehandler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Ausnahmehandlers.


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



Beachten Sie, **\_ \_ dass der try-Block** und der Ausnahmehandlerblock geschweifte Klammern () {} erfordern. Die Verwendung **einer goto-Anweisung** zum Springen in den Text eines **\_ \_ try-Blocks** oder in einen Ausnahmehandlerblock ist nicht zulässig. Diese Regel gilt sowohl für Ausnahmehandler als auch für Beendigungshandler.

Der **\_ \_ try-Block** enthält den geschützten Codekörper, den der Ausnahmehandler schützt. Eine Funktion kann über eine beliebige Anzahl von Ausnahmehandlern verfügen, und diese Ausnahmebehandlungs-Anweisungen können innerhalb derselben Funktion oder in verschiedenen Funktionen geschachtelt werden. Wenn innerhalb des **\_ \_ try-Blocks** eine Ausnahme auftritt, übernimmt das System die Kontrolle und beginnt mit der Suche nach einem Ausnahmehandler. Eine ausführliche Beschreibung dieser Suche finden Sie unter [Ausnahmebehandlung.](exception-handling.md)

Der Ausnahmehandler empfängt nur Ausnahmen, die innerhalb eines einzelnen Threads auftreten. Dies bedeutet, dass Ausnahmen, die innerhalb des neuen Prozesses oder Threads auftreten, nicht an diesen Handler gesendet werden, wenn ein **\_ \_ try-Block** einen Aufruf der [**CreateProcess-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) oder [**CreateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) enthält.

Das System wertet den Filterausdruck jedes Ausnahmehandlers aus, um den Code zu schützen, in dem die Ausnahme aufgetreten ist, bis entweder die Ausnahme behandelt wird oder keine Handler mehr enthalten sind. Ein Filterausdruck muss als einer der drei folgenden Werte ausgewertet werden.



| Wert                              | Bedeutung                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EXCEPTION \_ EXECUTE \_ HANDLER**    | Das System überträgt die Steuerung an den Ausnahmehandler, und die Ausführung wird in dem Stapelrahmen fortgesetzt, in dem sich der Handler befindet.                                                                                       |
| **EXCEPTION \_ CONTINUE \_ SEARCH**    | Das System sucht weiterhin nach einem Handler.                                                                                                                                                                          |
| **EXCEPTION \_ CONTINUE \_ EXECUTION** | Das System beendet die Suche nach einem Handler und gibt die Steuerung bis zu dem Punkt zurück, an dem die Ausnahme aufgetreten ist. Wenn die Ausnahme nicht inkontinuierbar ist, führt dies zu einer **EXCEPTION \_ NONCONTINUABLE \_ EXCEPTION-Ausnahme.** |



 

Der Filterausdruck wird im Kontext der Funktion ausgewertet, in der sich der Ausnahmehandler befindet, obwohl die Ausnahme möglicherweise in einer anderen Funktion aufgetreten ist. Dies bedeutet, dass der Filterausdruck auf die lokalen Variablen der Funktion zugreifen kann. Auf ähnliche Weise kann der Ausnahmehandlerblock auf die lokalen Variablen der Funktion zugreifen, in der er sich befindet.

Weitere Beispiele finden Sie unter [Verwenden eines Ausnahmehandlers.](using-an-exception-handler.md)

Weitere Informationen zu Filterausdrücken und Filterfunktionen finden Sie unter [Framebasierte Ausnahmebehandlung.](frame-based-exception-handling.md)

 

 
