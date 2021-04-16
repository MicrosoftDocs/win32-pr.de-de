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
# <a name="enumerating-symbol-modules"></a>Auflisten von Symbol Modulen

Im folgenden Code werden die Module aufgelistet, die von der [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) -oder der [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion geladen wurden. Die [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) -Funktion erfordert eine Rückruffunktion, die für jedes geladene Modul einmal aufgerufen wird. In diesem Beispiel ist EnumModules eine Implementierung der Rückruffunktion. Im Beispiel wird davon ausgegangen, dass Sie den Symbol Handler initialisiert haben, indem Sie den Code zum [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)verwenden.


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



 

 



