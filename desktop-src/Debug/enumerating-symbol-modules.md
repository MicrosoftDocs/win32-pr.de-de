---
description: Im folgenden Code werden die Module aufgelistet, die von der SymLoadModule64-oder der syminitialize-Funktion geladen wurden.
ms.assetid: 8c7fdfaa-d4d3-42d6-ad19-23e8ffda7bf4
title: Auflisten von Symbol Modulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43623a7409116450fccc822bbc0bef1a309fbd2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482726"
---
# <a name="enumerating-symbol-modules"></a><span data-ttu-id="6d6dc-103">Auflisten von Symbol Modulen</span><span class="sxs-lookup"><span data-stu-id="6d6dc-103">Enumerating Symbol Modules</span></span>

<span data-ttu-id="6d6dc-104">Im folgenden Code werden die Module aufgelistet, die von der [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) -oder der [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-104">The following code lists the modules that have been loaded by the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="6d6dc-105">Die [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) -Funktion erfordert eine Rückruffunktion, die für jedes geladene Modul einmal aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-105">The [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) function requires a callback function, which will be called once for each module loaded.</span></span> <span data-ttu-id="6d6dc-106">In diesem Beispiel ist EnumModules eine Implementierung der Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-106">In this example, EnumModules is an implementation of the callback function.</span></span> <span data-ttu-id="6d6dc-107">Im Beispiel wird davon ausgegangen, dass Sie den Symbol Handler initialisiert haben, indem Sie den Code zum [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="6d6dc-107">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
BOOL CALLBACK EnumModules(
    PCTSTR  ModuleName, 
    DWORD64 BaseOfDll,  
    PVOID   UserContext )
{
    UNREFERENCED_PARAMETER(UserContext);
    
    _tprintf(TEXT("%08X %s\n"), BaseOfDll, ModuleName);
    return TRUE;
}


if (SymEnumerateModules64(hProcess, EnumModules, NULL))
{
    // SymEnumerateModules64 returned success
}
else
{
    // SymEnumerateModules64 failed
    error = GetLastError();
    _tprintf(TEXT("SymEnumerateModules64 returned error : %d\n"), error);
}
```



 

 



