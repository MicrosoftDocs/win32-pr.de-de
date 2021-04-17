---
description: Die \_ \_ \_ \_ Schlüsselwörter try und außer werden verwendet, um einen Frame basierten Ausnahmehandler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Ausnahme Handlers.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Exception-Handler-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522875"
---
# <a name="exception-handler-syntax"></a><span data-ttu-id="e4a05-104">Exception-Handler-Syntax</span><span class="sxs-lookup"><span data-stu-id="e4a05-104">Exception-Handler Syntax</span></span>

<span data-ttu-id="e4a05-105">Die Schlüsselwörter **\_ \_ try** und **\_ \_ außer** werden verwendet, um einen Frame basierten Ausnahmehandler zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4a05-105">The **\_\_try** and **\_\_except** keywords are used to construct a frame-based exception handler.</span></span> <span data-ttu-id="e4a05-106">Das folgende Beispiel zeigt die Struktur eines Ausnahme Handlers.</span><span class="sxs-lookup"><span data-stu-id="e4a05-106">The following example shows the structure of an exception handler.</span></span>


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



<span data-ttu-id="e4a05-107">Beachten Sie, dass der **\_ \_ try** -Block und der Ausnahmehandlerblock geschweifte Klammern ( {} ) erfordern.</span><span class="sxs-lookup"><span data-stu-id="e4a05-107">Note that the **\_\_try** block and the exception-handler block require braces ({}).</span></span> <span data-ttu-id="e4a05-108">Das Verwenden einer **goto** -Anweisung zum Springen in den Text eines **\_ \_ try** -Blocks oder in einen Ausnahmehandlerblock ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e4a05-108">Using a **goto** statement to jump into the body of a **\_\_try** block or into an exception-handler block is not permitted.</span></span> <span data-ttu-id="e4a05-109">Diese Regel gilt sowohl für Ausnahmehandler als auch für Beendigungs Handler.</span><span class="sxs-lookup"><span data-stu-id="e4a05-109">This rule applies to both exception handlers and termination handlers.</span></span>

<span data-ttu-id="e4a05-110">Der **\_ \_ try** -Block enthält den überwachten Code Körper, den der Ausnahmehandler schützt.</span><span class="sxs-lookup"><span data-stu-id="e4a05-110">The **\_\_try** block contains the guarded body of code that the exception handler protects.</span></span> <span data-ttu-id="e4a05-111">Eine Funktion kann über eine beliebige Anzahl von Ausnahme Handlern verfügen, und diese Ausnahme behandlungsanweisungen können in derselben Funktion oder in verschiedenen Funktionen geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="e4a05-111">A function can have any number of exception handlers, and these exception-handling statements can be nested within the same function or in different functions.</span></span> <span data-ttu-id="e4a05-112">Wenn im **\_ \_ try** -Block eine Ausnahme auftritt, übernimmt das System die Steuerung und beginnt die Suche nach einem Ausnahmehandler.</span><span class="sxs-lookup"><span data-stu-id="e4a05-112">If an exception occurs within the **\_\_try** block, the system takes control and begins the search for an exception handler.</span></span> <span data-ttu-id="e4a05-113">Eine ausführliche Beschreibung dieser Suche finden Sie unter [Ausnahmebehandlung](exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e4a05-113">For a detailed description of this search, see [Exception Handling](exception-handling.md).</span></span>

<span data-ttu-id="e4a05-114">Der Ausnahmehandler empfängt nur Ausnahmen, die innerhalb eines einzelnen Threads auftreten.</span><span class="sxs-lookup"><span data-stu-id="e4a05-114">The exception handler receives only exceptions that occur within a single thread.</span></span> <span data-ttu-id="e4a05-115">Dies bedeutet, dass bei einem **\_ \_ try** -Block, der einen Aufrufen der Funktion " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " oder " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " enthält, Ausnahmen, die im neuen Prozess oder Thread auftreten, nicht an diesen Handler weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="e4a05-115">This means that if a **\_\_try** block contains a call to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) or [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function, exceptions that occur within the new process or thread are not dispatched to this handler.</span></span>

<span data-ttu-id="e4a05-116">Das System wertet den Filter Ausdruck jedes Ausnahme Handlers aus, der den Code schützt, in dem die Ausnahme aufgetreten ist, bis entweder die Ausnahme behandelt wird oder keine Handler mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e4a05-116">The system evaluates the filter expression of each exception handler guarding the code in which the exception occurred until either the exception is handled or there are no more handlers.</span></span> <span data-ttu-id="e4a05-117">Ein Filter Ausdruck muss als einer der drei folgenden Werte ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="e4a05-117">A filter expression must be evaluated as one of the three following values.</span></span>



| <span data-ttu-id="e4a05-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e4a05-118">Value</span></span>                              | <span data-ttu-id="e4a05-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e4a05-119">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a05-120">**Ausnahme \_ Ausführungs \_ Handler**</span><span class="sxs-lookup"><span data-stu-id="e4a05-120">**EXCEPTION\_EXECUTE\_HANDLER**</span></span>    | <span data-ttu-id="e4a05-121">Das System überträgt die Steuerung an den Ausnahmehandler, und die Ausführung wird im Stapel Rahmen fortgesetzt, in dem der Handler gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e4a05-121">The system transfers control to the exception handler, and execution continues in the stack frame in which the handler is found.</span></span>                                                                                       |
| <span data-ttu-id="e4a05-122">**Ausnahme \_ Suche fortsetzen \_**</span><span class="sxs-lookup"><span data-stu-id="e4a05-122">**EXCEPTION\_CONTINUE\_SEARCH**</span></span>    | <span data-ttu-id="e4a05-123">Das System sucht weiterhin nach einem Handler.</span><span class="sxs-lookup"><span data-stu-id="e4a05-123">The system continues to search for a handler.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="e4a05-124">**Ausnahme \_ Ausführung fortsetzen \_**</span><span class="sxs-lookup"><span data-stu-id="e4a05-124">**EXCEPTION\_CONTINUE\_EXECUTION**</span></span> | <span data-ttu-id="e4a05-125">Das System beendet die Suche nach einem Handler und gibt die Steuerung an die Stelle zurück, an der die Ausnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e4a05-125">The system stops its search for a handler and returns control to the point at which the exception occurred.</span></span> <span data-ttu-id="e4a05-126">Wenn die Ausnahme nicht fort setzbar ist, führt dies zu einer Ausnahme Ausnahme, die **\_ nicht fort setzbar \_** ist.</span><span class="sxs-lookup"><span data-stu-id="e4a05-126">If the exception is noncontinuable, this results in an **EXCEPTION\_NONCONTINUABLE\_EXCEPTION** exception.</span></span> |



 

<span data-ttu-id="e4a05-127">Der Filter Ausdruck wird im Kontext der Funktion ausgewertet, in der sich der Ausnahmehandler befindet, auch wenn die Ausnahme möglicherweise in einer anderen Funktion aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e4a05-127">The filter expression is evaluated in the context of the function in which the exception handler is located, even though the exception may have occurred in a different function.</span></span> <span data-ttu-id="e4a05-128">Dies bedeutet, dass der Filter Ausdruck auf die lokalen Variablen der Funktion zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="e4a05-128">This means that the filter expression can access the function's local variables.</span></span> <span data-ttu-id="e4a05-129">Ebenso kann der Ausnahmehandlerblock auf die lokalen Variablen der Funktion zugreifen, in der er sich befindet.</span><span class="sxs-lookup"><span data-stu-id="e4a05-129">Similarly, the exception-handler block can access the local variables of the function in which it is located.</span></span>

<span data-ttu-id="e4a05-130">Weitere Beispiele finden Sie unter [Verwenden eines Ausnahme Handlers](using-an-exception-handler.md).</span><span class="sxs-lookup"><span data-stu-id="e4a05-130">For more examples, see [Using an Exception Handler](using-an-exception-handler.md).</span></span>

<span data-ttu-id="e4a05-131">Weitere Informationen zu Filter Ausdrücken und Filterfunktionen finden Sie unter [Frame basierte Ausnahmebehandlung](frame-based-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e4a05-131">For more information about filter expressions and filter functions, see [Frame-based Exception Handling](frame-based-exception-handling.md).</span></span>

 

 
