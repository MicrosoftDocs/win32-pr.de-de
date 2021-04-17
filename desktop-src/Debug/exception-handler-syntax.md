---
description: Die \_ \_ \_ \_ Schlüsselwörter try und außer werden verwendet, um einen Frame basierten Ausnahmehandler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Ausnahme Handlers.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Exception-Handler-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522875"
---
# <a name="exception-handler-syntax"></a>Exception-Handler-Syntax

Die Schlüsselwörter **\_ \_ try** und **\_ \_ außer** werden verwendet, um einen Frame basierten Ausnahmehandler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Ausnahme Handlers.


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



Beachten Sie, dass der **\_ \_ try** -Block und der Ausnahmehandlerblock geschweifte Klammern ( {} ) erfordern. Das Verwenden einer **goto** -Anweisung zum Springen in den Text eines **\_ \_ try** -Blocks oder in einen Ausnahmehandlerblock ist nicht zulässig. Diese Regel gilt sowohl für Ausnahmehandler als auch für Beendigungs Handler.

Der **\_ \_ try** -Block enthält den überwachten Code Körper, den der Ausnahmehandler schützt. Eine Funktion kann über eine beliebige Anzahl von Ausnahme Handlern verfügen, und diese Ausnahme behandlungsanweisungen können in derselben Funktion oder in verschiedenen Funktionen geschachtelt werden. Wenn im **\_ \_ try** -Block eine Ausnahme auftritt, übernimmt das System die Steuerung und beginnt die Suche nach einem Ausnahmehandler. Eine ausführliche Beschreibung dieser Suche finden Sie unter [Ausnahmebehandlung](exception-handling.md).

Der Ausnahmehandler empfängt nur Ausnahmen, die innerhalb eines einzelnen Threads auftreten. Dies bedeutet, dass bei einem **\_ \_ try** -Block, der einen Aufrufen der Funktion " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " oder " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " enthält, Ausnahmen, die im neuen Prozess oder Thread auftreten, nicht an diesen Handler weitergeleitet werden.

Das System wertet den Filter Ausdruck jedes Ausnahme Handlers aus, der den Code schützt, in dem die Ausnahme aufgetreten ist, bis entweder die Ausnahme behandelt wird oder keine Handler mehr vorhanden sind. Ein Filter Ausdruck muss als einer der drei folgenden Werte ausgewertet werden.



| Wert                              | Bedeutung                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ausnahme \_ Ausführungs \_ Handler**    | Das System überträgt die Steuerung an den Ausnahmehandler, und die Ausführung wird im Stapel Rahmen fortgesetzt, in dem der Handler gefunden wird.                                                                                       |
| **Ausnahme \_ Suche fortsetzen \_**    | Das System sucht weiterhin nach einem Handler.                                                                                                                                                                          |
| **Ausnahme \_ Ausführung fortsetzen \_** | Das System beendet die Suche nach einem Handler und gibt die Steuerung an die Stelle zurück, an der die Ausnahme aufgetreten ist. Wenn die Ausnahme nicht fort setzbar ist, führt dies zu einer Ausnahme Ausnahme, die **\_ nicht fort setzbar \_** ist. |



 

Der Filter Ausdruck wird im Kontext der Funktion ausgewertet, in der sich der Ausnahmehandler befindet, auch wenn die Ausnahme möglicherweise in einer anderen Funktion aufgetreten ist. Dies bedeutet, dass der Filter Ausdruck auf die lokalen Variablen der Funktion zugreifen kann. Ebenso kann der Ausnahmehandlerblock auf die lokalen Variablen der Funktion zugreifen, in der er sich befindet.

Weitere Beispiele finden Sie unter [Verwenden eines Ausnahme Handlers](using-an-exception-handler.md).

Weitere Informationen zu Filter Ausdrücken und Filterfunktionen finden Sie unter [Frame basierte Ausnahmebehandlung](frame-based-exception-handling.md).

 

 
