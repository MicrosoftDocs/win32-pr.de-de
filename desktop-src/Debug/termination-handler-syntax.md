---
description: Die \_ \_ Schlüsselwörter try und finally \_ \_ werden verwendet, um einen Beendigungshandler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Beendigungshandlers.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Termination-Handler Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3a6322bbcf86f56a75c62eaba03d50827edcd71a57addf48ef3777c7687796
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984460"
---
# <a name="termination-handler-syntax"></a>Termination-Handler Syntax

Die **\_ \_ Schlüsselwörter try** und **\_ \_ finally** werden verwendet, um einen Beendigungshandler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Beendigungshandlers.


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



Beispiele finden Sie unter [Verwenden eines Beendigungshandlers.](using-a-termination-handler.md)

Wie beim Ausnahmehandler erfordern sowohl der **\_ \_ try-Block** als auch der **\_ \_ finally-Block** geschweifte Klammern (), und die Verwendung einer goto-Anweisung zum Springen in beide Block {} ist nicht zulässig. 

Der **\_ \_ try-Block** enthält den geschützten Codekörper, der durch den Beendigungshandler geschützt wird. Eine Funktion kann eine beliebige Anzahl von Beendigungshandlern haben, und diese Beendigungsbehandlungsblöcke können innerhalb derselben Funktion oder in verschiedenen Funktionen geschachtelt werden.

Der **\_ \_ finally-Block** wird immer dann ausgeführt, wenn der Ablauf der Steuerung den **\_ \_ try-Block verlässt.** Der **\_ \_ finally-Block** wird jedoch nicht ausgeführt, wenn Sie eine der folgenden Funktionen innerhalb des **\_ \_ try-Blocks** aufrufen: [**ExitProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)oder **abbrechen.**

Der **\_ \_ finally-Block** wird im Kontext der Funktion ausgeführt, in der sich der Beendigungshandler befindet. Dies bedeutet, dass **\_ \_ der finally-Block** auf die lokalen Variablen dieser Funktion zugreifen kann. Die Ausführung des **\_ \_ finally-Blocks** kann mit einem der folgenden Mittel beendet werden.

-   Ausführung der letzten Anweisung im -Block und Fortsetzung zur nächsten Anweisung
-   Verwendung einer Steuerelement-Anweisung (**rückgabe**, **break**, **continue** oder **goto**)
-   Verwenden von **longjmp oder** springen zu einem Ausnahmehandler

Wenn die Ausführung des **\_ \_ try-Blocks** aufgrund einer Ausnahme beendet wird, die den Ausnahmebehandlungsblock eines framebasierten Ausnahmehandlers aufruft, wird der **\_ \_ finally-Block** ausgeführt, bevor der Ausnahmebehandlungsblock ausgeführt wird. Entsprechend bewirkt ein Aufruf der C-Laufzeitbibliotheksfunktion **longjmp** aus dem **\_ \_ try-Block** die Ausführung des **\_ \_ finally-Blocks,** bevor die Ausführung am Ziel des **longjmp-Vorgangs fortgesetzt** wird. Wenn **\_ \_ die Try-Blockausführung** aufgrund einer Steuerungs-Anweisung **beendet** wird ( rückgabe , **break**, **continue** oder **goto**), wird der **\_ \_ finally-Block** ausgeführt.

Die [**AbnormalTermination-Funktion**](abnormaltermination.md) kann innerhalb des **\_ \_ finally-Blocks** verwendet werden, um zu bestimmen, ob der **\_ \_ try-Block** sequenziell beendet wurde, d. h., ob er die schließende geschweifte Klammer (}) erreicht hat. Das Verlassen **\_ \_ des try-Blocks** aufgrund eines Aufrufs von **longjmp,** eines Sprungs zu einem Ausnahmehandler oder einer Rückgabe von **,** **break,** **continue** oder **goto-Anweisung** wird als nicht normale Beendigung betrachtet. Beachten Sie, dass ein Fehler beim sequenziellen Beenden dazu führt, dass das System alle Stapelrahmen in umgekehrter Reihenfolge durchsucht, um zu bestimmen, ob Beendigungshandler aufgerufen werden müssen. Dies kann aufgrund der Ausführung von Hunderten von Anweisungen zu Leistungseinbußen führen.

Um eine ungewöhnliche Beendigung des Beendigungshandlers zu vermeiden, sollte die Ausführung bis zum Ende des Blocks fortgesetzt werden. Sie können auch die **\_ \_ leave-Anweisung** ausführen. Die **\_ \_ leave-Anweisung** ermöglicht die sofortige Beendigung des **\_ \_ try-Blocks,** ohne dass dies zu einer ungewöhnlichen Beendigung und leistungsbehafteten Leistung führt. Überprüfen Sie ihre Compilerdokumentation, um zu ermitteln, ob **\_ \_ die leave-Anweisung** unterstützt wird.

Wenn die Ausführung des **\_ \_ finally-Blocks** aufgrund der Rückgabesteuerungs-Anweisung beendet wird, entspricht dies einem  **Goto** zur schließenden geschweiften Klammer in der umschließenden Funktion. Daher gibt die umschließende Funktion zurück.

 

 
