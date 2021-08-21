---
description: Der folgende Code veranschaulicht, wie der Symbolhandler initialisiert wird.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Initialisieren des Symbolhandlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f1da864c4550232d278b6bfb9b2006a6d56956e363dcf4fbd72ed0e6b9685d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956979"
---
# <a name="initializing-the-symbol-handler"></a>Initialisieren des Symbolhandlers

Der folgende Code veranschaulicht, wie der Symbolhandler initialisiert wird. Die [**SymSetOptions-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) überlädt das Laden von Symbolen, bis Symbolinformationen angefordert werden. Der Code lädt die Symbole für jedes Modul im angegebenen Prozess, indem der Wert **TRUE** für den *bInvade-Parameter* der [**SymInitialize-Funktion übergeben**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) wird. (Diese Funktion ruft die [**SymLoadModule64-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) für jedes Modul auf, das der Prozess seinem Adressraum zugeordnet hat.)

Wenn der angegebene Prozess nicht der Prozess ist, der [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)aufgerufen hat, übergibt der Code einen Prozessbezeichner als ersten Parameter von **SymInitialize.**

Die Angabe **von NULL** als zweiter Parameter von [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) gibt an, dass der Symbolhandler den Standardsuchpfad verwenden soll, um Symboldateien zu suchen. Ausführliche Informationen dazu, wie der Symbolhandler Symboldateien sucht oder wie eine Anwendung einen Symbolsuchpfad angeben kann, finden Sie unter [Symbolpfade](symbol-paths.md).


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



