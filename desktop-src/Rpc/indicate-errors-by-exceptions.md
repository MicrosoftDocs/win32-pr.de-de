---
title: Fehler durch Ausnahmen anzeigen
description: Bei herkömmlichen C-Programmierern werden Fehler häufig durch Rückgabewerte oder einen speziellen "\ out \"-Parameter zurückgegeben, der den Fehlercode zurückgibt.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858374"
---
# <a name="indicate-errors-by-exceptions"></a>Fehler durch Ausnahmen anzeigen

Bei herkömmlichen C-Programmierern werden Fehler häufig durch Rückgabewerte oder einen speziellen out-Parameter zurückgegeben, \[ \] der den Fehlercode zurückgibt. Dies führt dazu, dass die Schnittstellen folgendermaßen implementiert werden:

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

Das Problem bei diesem Ansatz besteht darin, dass RPC-Rückgabewerte einfach lange ganze Zahlen sind. Sie haben keine besondere Bedeutung als Fehler (Beachten Sie, dass [**Fehler \_ Status \_ t**](/windows/desktop/Midl/error-status-t) keine besondere Semantik auf der Serverseite aufweist), was wichtige Implikationen bringt.

Erstens wird RPC nicht benachrichtigt, dass der Vorgang fehlgeschlagen ist. Es wird versucht, alle \[ in-, out \] -und \[ out- \] Argumente zu entmarshalling. Die Fehler Semantik von Kontext Handles unterscheidet sich ebenfalls. Das Paket, das an den Client zurückgegeben wird, ist im Wesentlichen ein Erfolgs Paket, wobei der Fehlercode tief im Paket verborgen ist. Dies bedeutet auch, dass RPC keine erweiterten Fehlerinformationen verwendet, sodass Client Software häufig nicht erkennen kann, wo der Aufruf fehlgeschlagen ist.

Die Angabe von Fehlern in RPC-Server Routinen durch Auslösen von SEH-Ausnahmen (strukturierte Ausnahmebehandlung) (nicht C++) ist ein viel besseres Konzept. Wenn eine SEH-Ausnahme ausgelöst wird, wird die Steuerung direkt an die RPC-Laufzeit weitergeleitet. Manchmal tritt ein Fehler in einer Routine auf, die nicht ordnungsgemäß bereinigt werden kann, und es muss ein Fehler für den Aufrufer angezeigt werden. Die Routine sollte einen Fehler an den Aufrufer zurückgeben, der wiederum einen Fehler an den Aufrufer zurückgeben kann usw. Allerdings sollte die letzte Server Routine auf dem Stapel eine Ausnahme auslösen, bevor Sie zu RPC zurückkehrt, um RPC anzuzeigen, dass ein Fehler aufgetreten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausnahmebehandlung](exception-handling.md)
</dt> </dl>

 

 