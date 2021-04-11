---
description: Der folgende Code veranschaulicht, wie die symfromname-Funktion aufgerufen wird.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Abrufen von Symbol Informationen nach Name
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f5f4477be4f494383c7d9c1ca462f3beb69690
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126428"
---
# <a name="retrieving-symbol-information-by-name"></a>Abrufen von Symbol Informationen nach Name

Der folgende Code veranschaulicht, wie die [**symfromname**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) -Funktion aufgerufen wird. Diese Funktion füllt eine [**Symbol \_ Informations**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Struktur aus. Da der Name eine Variable Länge hat, müssen Sie einen Puffer bereitstellen, der groß genug ist, um den am Ende der **Symbol \_ Informations** Struktur gespeicherten Namen zu speichern. Außerdem muss der **maxnamelen** -Member auf die Anzahl der für den Namen reservierten Bytes festgelegt werden. In diesem Beispiel ist szsymbolname ein Puffer, in dem der Name des angeforderten Symbols gespeichert wird. Im Beispiel wird davon ausgegangen, dass Sie den Symbol Handler initialisiert haben, indem Sie den Code zum [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)verwenden.


```C++
TCHAR szSymbolName[MAX_SYM_NAME];
ULONG64 buffer[(sizeof(SYMBOL_INFO) +
    MAX_SYM_NAME * sizeof(TCHAR) +
    sizeof(ULONG64) - 1) /
    sizeof(ULONG64)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

_tcscpy_s(szSymbolName, MAX_SYM_NAME, TEXT("WinMain"));
pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromName(hProcess, szSymbolName, pSymbol))
{
    // SymFromName returned success
}
else
{
    // SymFromName failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymFromName returned error : %d\n"), error);
}
```



Wenn eine Anwendung über einen Modul-oder Quell Dateinamen sowie über Zeilennummern Informationen verfügt, kann [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) verwendet werden, um eine virtuelle Code Adresse abzurufen. Diese Funktion erfordert einen Zeiger auf eine [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) -Struktur, um die Adresse des virtuellen Codes zu erhalten. Beachten Sie, dass der Symbol Handler Zeilennummern Informationen nur abrufen kann, \_ Wenn \_ die Option für die Verwendung von symopt-Zeilen mithilfe der [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion festgelegt wird Diese Option muss vor dem Laden des Moduls festgelegt werden. Der szModuleName-Parameter enthält den Namen des Quell Moduls. Er ist optional und kann **null** sein. Der szFilename-Parameter sollte den Quell Dateinamen enthalten, und der dwlinenumber-Parameter sollte die Zeilennummer enthalten, für die die virtuelle Adresse abgerufen wird.


```C++
TCHAR  szModuleName[MAX_PATH];
TCHAR  szFileName[MAX_PATH];
DWORD  dwLineNumber;
LONG   lDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
_tcscpy_s(szModuleName, MAX_PATH, TEXT("MyApp"));
_tcscpy_s(szFileName, MAX_PATH, TEXT("main.c"));
dwLineNumber = 248;

if (SymGetLineFromName64(hProcess, szModuleName, szFileName,
    dwLineNumber, &lDisplacement, &line))
{
    // SymGetLineFromName64 returned success
}
else
{
    // SymGetLineFromName64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromName64 returned error : %d\n"), error);
}
```



 

 



