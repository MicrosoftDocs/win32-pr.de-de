---
title: Fehler nach Ausnahmen angeben
description: Bei herkömmlichen C-Programmierern werden Fehler häufig über Rückgabewerte oder einen speziellen \out\-Parameter zurückgegeben, der den Fehlercode zurückgibt.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 816f63f9378c3f2338c7bed6f6a9b5f785d3e138e4762c355aa1932887fd14c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928916"
---
# <a name="indicate-errors-by-exceptions"></a>Fehler nach Ausnahmen angeben

Bei herkömmlichen C-Programmierern werden Fehler häufig über Rückgabewerte oder einen speziellen out-Parameter zurückgegeben, \[ \] der den Fehlercode zurückgibt. Dies führt dazu, dass Schnittstellen wie folgt implementiert werden:

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

Das Problem bei diesem Ansatz ist, dass RPC-Rückgabewerte einfach lange ganze Zahlen sind. Sie haben keine besondere Bedeutung als Fehler (beachten Sie, dass der Fehlerstatus [**\_ \_ nicht**](/windows/desktop/Midl/error-status-t) über eine spezielle Semantik auf serverseitiger Seite verfügt), was wichtige Auswirkungen hat.

Erstens wird RPC nicht benachrichtigt, dass der Vorgang fehlgeschlagen ist. es versucht, alle ein-, aus- und \[ out-Argumente zu entmarshalieren. \] \[ \] Die Fehlersemantik von Kontexthandles ist ebenfalls unterschiedlich. Das an den Client zurückgegebene Paket ist im Wesentlichen ein Erfolgspaket, bei dem der Fehlercode tief im Paket liegt. Dies bedeutet auch, dass RPC keine erweiterten Fehlerinformationen verwendet, sodass die Clientsoftware häufig nicht erkennen kann, wo der Aufruf fehlgeschlagen ist.

Das Angeben von Fehlern in RPC-Serverroutinen durch Auslösen von SEH-Ausnahmen (Structured Exception Handling) (nicht C++) ist ein viel besserer Ansatz. Wenn eine SEH-Ausnahme ausgelöst wird, wird die Steuerung direkt zur RPC-Laufzeit ausgeführt. Manchmal tritt ein Fehler tief in einer Routine auf, die nicht ordnungsgemäß bereinigt werden kann, und muss dem Aufrufer einen Fehler anzeigen. Die Routine sollte einen Fehler an ihren Aufrufer zurückgeben, der wiederum einen Fehler an den Aufrufer zurückgeben kann und so weiter. Die letzte Serverroutine im Stapel sollte jedoch eine Ausnahme auslösen, bevor sie zu RPC zurückkehrt, um rpc anzugeben, dass ein Fehler aufgetreten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausnahmebehandlung](exception-handling.md)
</dt> </dl>

 

 