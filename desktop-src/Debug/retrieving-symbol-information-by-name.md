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
# <a name="retrieving-symbol-information-by-name"></a><span data-ttu-id="58d27-103">Abrufen von Symbol Informationen nach Name</span><span class="sxs-lookup"><span data-stu-id="58d27-103">Retrieving Symbol Information by Name</span></span>

<span data-ttu-id="58d27-104">Der folgende Code veranschaulicht, wie die [**symfromname**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="58d27-104">The following code demonstrates how to call the [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) function.</span></span> <span data-ttu-id="58d27-105">Diese Funktion füllt eine [**Symbol \_ Informations**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="58d27-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="58d27-106">Da der Name eine Variable Länge hat, müssen Sie einen Puffer bereitstellen, der groß genug ist, um den am Ende der **Symbol \_ Informations** Struktur gespeicherten Namen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="58d27-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="58d27-107">Außerdem muss der **maxnamelen** -Member auf die Anzahl der für den Namen reservierten Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="58d27-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="58d27-108">In diesem Beispiel ist szsymbolname ein Puffer, in dem der Name des angeforderten Symbols gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="58d27-108">In this example, szSymbolName is a buffer that stores the name of the requested symbol.</span></span> <span data-ttu-id="58d27-109">Im Beispiel wird davon ausgegangen, dass Sie den Symbol Handler initialisiert haben, indem Sie den Code zum [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="58d27-109">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


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



<span data-ttu-id="58d27-110">Wenn eine Anwendung über einen Modul-oder Quell Dateinamen sowie über Zeilennummern Informationen verfügt, kann [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) verwendet werden, um eine virtuelle Code Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="58d27-110">If an application has a module or source file name as well as line number information, it can use [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) to retrieve a virtual code address.</span></span> <span data-ttu-id="58d27-111">Diese Funktion erfordert einen Zeiger auf eine [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) -Struktur, um die Adresse des virtuellen Codes zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="58d27-111">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the virtual code address.</span></span> <span data-ttu-id="58d27-112">Beachten Sie, dass der Symbol Handler Zeilennummern Informationen nur abrufen kann, \_ Wenn \_ die Option für die Verwendung von symopt-Zeilen mithilfe der [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="58d27-112">Note that the symbol handler can retrieve line number information only when SYMOPT\_LOAD\_LINES option is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="58d27-113">Diese Option muss vor dem Laden des Moduls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="58d27-113">This option must be set before loading the module.</span></span> <span data-ttu-id="58d27-114">Der szModuleName-Parameter enthält den Namen des Quell Moduls. Er ist optional und kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="58d27-114">The szModuleName parameter contains the source module name; it is optional and can be **NULL**.</span></span> <span data-ttu-id="58d27-115">Der szFilename-Parameter sollte den Quell Dateinamen enthalten, und der dwlinenumber-Parameter sollte die Zeilennummer enthalten, für die die virtuelle Adresse abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="58d27-115">The szFileName parameter should contain the source file name, and dwLineNumber parameter should contain the line number for which the virtual address will be retrieved.</span></span>


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



 

 



