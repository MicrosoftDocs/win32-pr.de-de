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
# <a name="initializing-the-symbol-handler"></a><span data-ttu-id="e2a57-103">Initialisieren des Symbol Handlers</span><span class="sxs-lookup"><span data-stu-id="e2a57-103">Initializing the Symbol Handler</span></span>

<span data-ttu-id="e2a57-104">Der folgende Code veranschaulicht, wie der Symbol Handler initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e2a57-104">The following code demonstrates how to initialize the symbol handler.</span></span> <span data-ttu-id="e2a57-105">Die [**symset**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion setzt das Laden von Symbolen so lange aus, bis Symbol Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="e2a57-105">The [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function defers symbol loading until symbol information is requested.</span></span> <span data-ttu-id="e2a57-106">Im Code werden die Symbole für die einzelnen Module im angegebenen Prozess geladen, indem der Wert **true** für den Parameter *binvade* der [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e2a57-106">The code loads the symbols for each module in the specified process by passing a value of **TRUE** for the *bInvade* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="e2a57-107">(Diese Funktion Ruft die [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) -Funktion für jedes Modul auf, das der Prozess dem Adressraum zugeordnet hat.)</span><span class="sxs-lookup"><span data-stu-id="e2a57-107">(This function calls the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) function for each module the process has mapped into its address space.)</span></span>

<span data-ttu-id="e2a57-108">Wenn der angegebene Prozess nicht der Prozess ist, der [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)aufgerufen hat, übergibt der Code eine Prozess-ID als ersten Parameter von **syminitialize**.</span><span class="sxs-lookup"><span data-stu-id="e2a57-108">If the specified process is not the process that called [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), the code passes a process identifier as the first parameter of **SymInitialize**.</span></span>

<span data-ttu-id="e2a57-109">Die Angabe von **null** als zweiten Parameter von [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) gibt an, dass der Symbol Handler den Standard Suchpfad verwenden soll, um Symbol Dateien zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e2a57-109">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="e2a57-110">Ausführliche Informationen dazu, wie der Symbol Handler Symbol Dateien sucht oder wie eine Anwendung einen Symbol Suchpfad angeben kann, finden Sie unter [Symbol Pfade](symbol-paths.md).</span><span class="sxs-lookup"><span data-stu-id="e2a57-110">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>


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



 

 



