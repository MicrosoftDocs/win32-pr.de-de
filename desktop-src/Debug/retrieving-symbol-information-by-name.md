---
description: Der folgende Code veranschaulicht das Aufrufen der SymFromName-Funktion.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Abrufen von Symbolinformationen nach Name
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ec0a04ef2cac9dcd8256f8d00ff59b00bec449cdb4b5661566e7087e782cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076364"
---
# <a name="retrieving-symbol-information-by-name"></a>Abrufen von Symbolinformationen nach Name

Der folgende Code veranschaulicht das Aufrufen der [**SymFromName-Funktion.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) Diese Funktion füllt eine [**SYMBOL \_ INFO-Struktur**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) aus. Da der Name eine variable Länge hat, müssen Sie einen Puffer angeben, der groß genug ist, um den Namen zu speichern, der am Ende der **SYMBOL \_ INFO-Struktur gespeichert** ist. Außerdem muss das **MaxNameLen-Member** auf die Anzahl von Bytes festgelegt werden, die für den Namen reserviert sind. In diesem Beispiel ist szSymbolName ein Puffer, der den Namen des angeforderten Symbols speichert. Im Beispiel wird davon ausgegangen, dass Sie den Symbolhandler mithilfe des Codes in [Initialisieren des Symbolhandlers initialisiert haben.](initializing-the-symbol-handler.md)


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



Wenn eine Anwendung über einen Modul- oder Quelldateinamen sowie Zeilennummerinformationen verfügt, kann sie [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) verwenden, um eine virtuelle Codeadresse abzurufen. Diese Funktion erfordert einen Zeiger auf eine [**IMAGEHLP \_ LINE64-Struktur,**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) um die virtuelle Codeadresse zu empfangen. Beachten Sie, dass der Symbolhandler Zeilennummerinformationen nur abrufen kann, wenn die SYMOPT LOAD LINES-Option mithilfe der \_ \_ [**SymSetOptions-Funktion festgelegt**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) wird. Diese Option muss vor dem Laden des Moduls festgelegt werden. Der szModuleName-Parameter enthält den Namen des Quellmoduls. sie ist optional und kann NULL **sein.** Der szFileName-Parameter sollte den Namen der Quelldatei enthalten, und der dwLineNumber-Parameter sollte die Zeilennummer enthalten, für die die virtuelle Adresse abgerufen wird.


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



 

 



