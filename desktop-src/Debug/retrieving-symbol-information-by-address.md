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
# <a name="retrieving-symbol-information-by-address"></a><span data-ttu-id="99661-103">Abrufen von Symbol Informationen nach Adresse</span><span class="sxs-lookup"><span data-stu-id="99661-103">Retrieving Symbol Information by Address</span></span>

<span data-ttu-id="99661-104">Der folgende Code veranschaulicht, wie die [**symfromaddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="99661-104">The following code demonstrates how to call the [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) function.</span></span> <span data-ttu-id="99661-105">Diese Funktion füllt eine [**Symbol \_ Informations**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="99661-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="99661-106">Da der Name eine Variable Länge hat, müssen Sie einen Puffer bereitstellen, der groß genug ist, um den am Ende der **Symbol \_ Informations** Struktur gespeicherten Namen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="99661-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="99661-107">Außerdem muss der **maxnamelen** -Member auf die Anzahl der für den Namen reservierten Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="99661-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="99661-108">In diesem Beispiel handelt es sich bei *dwaddress* um die Adresse, die einem Symbol zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="99661-108">In this example, *dwAddress* is the address to be mapped to a symbol.</span></span> <span data-ttu-id="99661-109">Die **symfromaddr** -Funktion speichert einen Offset am Anfang des Symbols für die Adresse in *dwverschiebungen*.</span><span class="sxs-lookup"><span data-stu-id="99661-109">The **SymFromAddr** function will store an offset to the beginning of the symbol to the address in *dwDisplacement*.</span></span> <span data-ttu-id="99661-110">Im Beispiel wird davon ausgegangen, dass Sie den Symbol Handler initialisiert haben, indem Sie den Code zum [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="99661-110">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


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



<span data-ttu-id="99661-111">Zum Abrufen der Quell Codezeilen Nummer für eine angegebene Adresse kann eine Anwendung [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)verwenden.</span><span class="sxs-lookup"><span data-stu-id="99661-111">To retrieve the source code line number for a specified address, an application can use [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span></span> <span data-ttu-id="99661-112">Diese Funktion erfordert einen Zeiger auf eine [**imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) -Struktur, um den Quell Dateinamen und die Zeilennummer zu erhalten, die einer angegebenen Code Adresse entsprechen.</span><span class="sxs-lookup"><span data-stu-id="99661-112">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the source file name and line number corresponding to a specified code address.</span></span> <span data-ttu-id="99661-113">Beachten Sie, dass der Symbol Handler Zeilennummern Informationen nur abrufen kann, wenn **symopt- \_ Auslastungs \_ Zeilen** mithilfe der [**symsetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="99661-113">Note that the symbol handler can retrieve line number information only when **SYMOPT\_LOAD\_LINES** is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="99661-114">Diese Option muss vor dem Laden des Moduls festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="99661-114">This option must be set before loading the module.</span></span> <span data-ttu-id="99661-115">Der dwaddress-Parameter enthält die Code Adresse, für die der Quell Dateiname und die Zeilennummer gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="99661-115">The dwAddress parameter contains the code address for which the source file name and line number will be located.</span></span>


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



 

 



