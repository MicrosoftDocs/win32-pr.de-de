---
description: Der folgende Code zeigt den Namen, die Adresse und die Größe jedes geladenen Symbols im angegebenen Modul an.
ms.assetid: 6ecdbd1e-406a-453e-9037-707ceb72074a
title: Aufzählen von Symbolen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 041768d46fec2aada74ebef37fdf5ffbb719b7c691a5e037a0f2f0532390d54e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692030"
---
# <a name="enumerating-symbols"></a>Aufzählen von Symbolen

Der folgende Code zeigt den Namen, die Adresse und die Größe jedes geladenen Symbols im angegebenen Modul an. Die [**SymEnumSymbols-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) erfordert eine Rückruffunktion, die einmal für jedes geladene Modul aufgerufen wird. In diesem Beispiel ist EnumSymProc eine Implementierung der Rückruffunktion.


```C++
#include <windows.h>
#include <stdio.h>
#include <dbghelp.h>

BOOL CALLBACK EnumSymProc( 
    PSYMBOL_INFO pSymInfo,   
    ULONG SymbolSize,      
    PVOID UserContext)
{
    UNREFERENCED_PARAMETER(UserContext);
    
    printf("%08X %4u %s\n", 
           pSymInfo->Address, SymbolSize, pSymInfo->Name);
    return TRUE;
}

void main()
{
    HANDLE hProcess = GetCurrentProcess();
    DWORD64 BaseOfDll;
    char *Mask = "*";
    BOOL status;

    status = SymInitialize(hProcess, NULL, FALSE);
    if (status == FALSE)
    {
        return;
    }
    
    BaseOfDll = SymLoadModuleEx(hProcess,
                                NULL,
                                "foo.dll",
                                NULL,
                                0,
                                0,
                                NULL,
                                0);
                                
    if (BaseOfDll == 0)
    {
        SymCleanup(hProcess);
        return;
    }                                
        
    if (SymEnumSymbols(hProcess,     // Process handle from SymInitialize.
                        BaseOfDll,   // Base address of module.
                        Mask,        // Name of symbols to match.
                        EnumSymProc, // Symbol handler procedure.
                        NULL))       // User context.
    {
        // SymEnumSymbols succeeded
    }
    else
    {
        // SymEnumSymbols failed
        printf("SymEnumSymbols failed: %d\n", GetLastError());
    }
    
    SymCleanup(hProcess);
}
```



 

 



