---
description: Der folgende Code veranschaulicht, wie die symfromaddr-Funktion aufgerufen wird.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Abrufen von Symbol Informationen nach Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ad9d2879dbfd5820c4aa6c2e7563a1575ebe1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126433"
---
# <a name="retrieving-symbol-information-by-address"></a>Abrufen von Symbol Informationen nach Adresse

Der folgende Code veranschaulicht, wie die [**symfromaddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) -Funktion aufgerufen wird. Diese Funktion füllt eine [**Symbol \_ Informations**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Struktur aus. Da der Name eine Variable Länge hat, müssen Sie einen Puffer bereitstellen, der groß genug ist, um den am Ende der **Symbol \_ Informations** Struktur gespeicherten Namen zu speichern. Außerdem muss der **maxnamelen** -Member auf die Anzahl der für den Namen reservierten Bytes festgelegt werden. In diesem Beispiel handelt es sich bei *dwaddress* um die Adresse, die einem Symbol zugeordnet werden soll. Die **symfromaddr** -Funktion speichert einen Offset am Anfang des Symbols für die Adresse in *dwverschiebungen*. Im Beispiel wird davon ausgegangen, dass Sie den Symbol Handler initialisiert haben, indem Sie den Code zum [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)verwenden.


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



Zum Abrufen der Quell Codezeilen Nummer für eine angegebene Adresse kann eine Anwendung [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)verwenden. Diese Funktion erfordert einen Zeiger auf eine [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) -Struktur, um den Quell Dateinamen und die Zeilennummer zu erhalten, die einer angegebenen Code Adresse entsprechen. Beachten Sie, dass der Symbol Handler Zeilennummern Informationen nur abrufen kann, wenn **symopt- \_ Auslastungs \_ Zeilen** mithilfe der [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion festgelegt werden. Diese Option muss vor dem Laden des Moduls festgelegt werden. Der dwaddress-Parameter enthält die Code Adresse, für die der Quell Dateiname und die Zeilennummer gesucht werden.


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



 

 



