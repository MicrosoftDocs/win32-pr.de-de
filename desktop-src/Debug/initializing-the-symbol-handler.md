---
description: Der folgende Code veranschaulicht, wie der Symbol Handler initialisiert wird.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Initialisieren des Symbol Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958193"
---
# <a name="initializing-the-symbol-handler"></a>Initialisieren des Symbol Handlers

Der folgende Code veranschaulicht, wie der Symbol Handler initialisiert wird. Die [**symset**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion setzt das Laden von Symbolen so lange aus, bis Symbol Informationen angefordert werden. Im Code werden die Symbole für die einzelnen Module im angegebenen Prozess geladen, indem der Wert **true** für den Parameter *binvade* der [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion übergeben wird. (Diese Funktion Ruft die [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) -Funktion für jedes Modul auf, das der Prozess dem Adressraum zugeordnet hat.)

Wenn der angegebene Prozess nicht der Prozess ist, der [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)aufgerufen hat, übergibt der Code eine Prozess-ID als ersten Parameter von **syminitialize**.

Die Angabe von **null** als zweiten Parameter von [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) gibt an, dass der Symbol Handler den Standard Suchpfad verwenden soll, um Symbol Dateien zu suchen. Ausführliche Informationen dazu, wie der Symbol Handler Symbol Dateien sucht oder wie eine Anwendung einen Symbol Suchpfad angeben kann, finden Sie unter [Symbol Pfade](symbol-paths.md).


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



 

 



