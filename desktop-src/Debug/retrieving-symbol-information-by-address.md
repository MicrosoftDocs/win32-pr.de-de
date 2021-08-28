---
description: Der folgende Code veranschaulicht, wie die SymFromAddr-Funktion aufgerufen wird.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Abrufen von Symbolinformationen nach Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484327117e66826402dc97abb09f58813e528599c69bd97054528f5cfe89aba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076384"
---
# <a name="retrieving-symbol-information-by-address"></a>Abrufen von Symbolinformationen nach Adresse

Der folgende Code veranschaulicht, wie die [**SymFromAddr-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) aufgerufen wird. Diese Funktion füllt eine [**SYMBOL \_ INFO-Struktur**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) aus. Da der Name eine variable Länge aufweist, müssen Sie einen Puffer angeben, der groß genug ist, um den Namen zu speichern, der am Ende der **SYMBOL \_ INFO-Struktur** gespeichert ist. Außerdem muss der **MaxNameLen-Member** auf die Anzahl von Bytes festgelegt werden, die für den Namen reserviert sind. In diesem Beispiel ist *dwAddress* die Adresse, die einem Symbol zugeordnet werden soll. Die **SymFromAddr-Funktion** speichert einen Offset am Anfang des Symbols in der Adresse in *dwDisplacement.* Im Beispiel wird davon ausgegangen, dass Sie den Symbolhandler mithilfe des Codes in [Initialisieren des Symbolhandlers initialisiert](initializing-the-symbol-handler.md)haben.


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



Um die Quellcodezeilennummer für eine angegebene Adresse abzurufen, kann eine Anwendung [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)verwenden. Diese Funktion erfordert einen Zeiger auf eine [**IMAGEHLP \_ LINE64-Struktur,**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) um den Quelldateinamen und die Zeilennummer zu erhalten, die einer angegebenen Codeadresse entsprechen. Beachten Sie, dass der Symbolhandler Zeilennummerninformationen nur abrufen kann, wenn **SYMOPT \_ LOAD \_ LINES** mithilfe der [**Funktion SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) festgelegt wird. Diese Option muss vor dem Laden des Moduls festgelegt werden. Der dwAddress-Parameter enthält die Codeadresse, für die sich der Quelldateiname und die Zeilennummer befinden.


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



