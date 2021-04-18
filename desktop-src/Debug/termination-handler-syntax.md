---
description: Die \_ \_ \_ \_ Schlüsselwörter try und schließlich werden verwendet, um einen Beendigungs Handler zu erstellen. Das folgende Beispiel zeigt die Struktur eines Beendigungs Handlers.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Termination-Handler-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344831"
---
# <a name="termination-handler-syntax"></a><span data-ttu-id="02888-104">Termination-Handler-Syntax</span><span class="sxs-lookup"><span data-stu-id="02888-104">Termination-Handler Syntax</span></span>

<span data-ttu-id="02888-105">Die Schlüsselwörter **\_ \_ try** und **\_ \_ schließlich** werden verwendet, um einen Beendigungs Handler zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02888-105">The **\_\_try** and **\_\_finally** keywords are used to construct a termination handler.</span></span> <span data-ttu-id="02888-106">Das folgende Beispiel zeigt die Struktur eines Beendigungs Handlers.</span><span class="sxs-lookup"><span data-stu-id="02888-106">The following example shows the structure of a termination handler.</span></span>


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



<span data-ttu-id="02888-107">Beispiele finden Sie unter [Verwenden eines Beendigungs Handlers](using-a-termination-handler.md).</span><span class="sxs-lookup"><span data-stu-id="02888-107">For examples, see [Using a Termination Handler](using-a-termination-handler.md).</span></span>

<span data-ttu-id="02888-108">Wie beim Ausnahmehandler erfordern sowohl der **\_ \_ try** -Block als auch **\_ \_ der-Block** geschweifte Klammern ( {} ), und die Verwendung einer **goto** -Anweisung zum Springen in beide Blöcke ist unzulässig.</span><span class="sxs-lookup"><span data-stu-id="02888-108">As with the exception handler, both the **\_\_try** block and the **\_\_finally** block require braces ({}), and using a **goto** statement to jump into either block is not permitted.</span></span>

<span data-ttu-id="02888-109">Der **\_ \_ try** -Block enthält den überwachten Code Körper, der durch den Beendigungs Handler geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="02888-109">The **\_\_try** block contains the guarded body of code that is protected by the termination handler.</span></span> <span data-ttu-id="02888-110">Eine Funktion kann über eine beliebige Anzahl von Beendigungs Handlern verfügen, und diese Beendigungs Verarbeitungsblöcke können innerhalb derselben Funktion oder in verschiedenen Funktionen geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="02888-110">A function can have any number of termination handlers, and these termination-handling blocks can be nested within the same function or in different functions.</span></span>

<span data-ttu-id="02888-111">Der Block wird ausgeführt, wenn die Ablauf Steuerung den **\_ \_ try** -Block **\_ \_** verlässt.</span><span class="sxs-lookup"><span data-stu-id="02888-111">The **\_\_finally** block is executed whenever the flow of control leaves the **\_\_try** block.</span></span> <span data-ttu-id="02888-112">Der Block wird jedoch nicht ausgeführt, wenn Sie eine der folgenden Funktionen im **\_ \_ try** **\_ \_ -Block** aufzurufen: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)oder **Abbruch**.</span><span class="sxs-lookup"><span data-stu-id="02888-112">However, the **\_\_finally** block is not executed if you call any of the following functions within the **\_\_try** block: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), or **abort**.</span></span>

<span data-ttu-id="02888-113">Der **\_ \_ schließlich** -Block wird im Kontext der Funktion ausgeführt, in der sich der Beendigungs Handler befindet.</span><span class="sxs-lookup"><span data-stu-id="02888-113">The **\_\_finally** block is executed in the context of the function in which the termination handler is located.</span></span> <span data-ttu-id="02888-114">Dies bedeutet, dass der **\_ \_ schließlich** -Block auf die lokalen Variablen der Funktion zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="02888-114">This means that the **\_\_finally** block can access that function's local variables.</span></span> <span data-ttu-id="02888-115">Die Ausführung des **\_ \_ letzten Blocks kann** auf eine der folgenden Weise beendet werden.</span><span class="sxs-lookup"><span data-stu-id="02888-115">Execution of the **\_\_finally** block can terminate by any of the following means.</span></span>

-   <span data-ttu-id="02888-116">Ausführung der letzten Anweisung im Block und Fortsetzung der nächsten Anweisung</span><span class="sxs-lookup"><span data-stu-id="02888-116">Execution of the last statement in the block and continuation to the next instruction</span></span>
-   <span data-ttu-id="02888-117">Verwendung einer Control-Anweisung ("**Return**", " **break**", " **Continue**" oder " **goto**")</span><span class="sxs-lookup"><span data-stu-id="02888-117">Use of a control statement (**return**, **break**, **continue**, or **goto**)</span></span>
-   <span data-ttu-id="02888-118">Verwendung von **longjmp** oder einem Sprung zu einem Ausnahmehandler</span><span class="sxs-lookup"><span data-stu-id="02888-118">Use of **longjmp** or a jump to an exception handler</span></span>

<span data-ttu-id="02888-119">Wenn die Ausführung des **\_ \_ try** -Blocks aufgrund einer Ausnahme beendet wird, die den Ausnahme Behandlungs Block eines Frame basierten Ausnahme Handlers aufruft, wird **der letzte \_ \_** -Block ausgeführt, bevor der Ausnahme Behandlungs Block ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02888-119">If execution of the **\_\_try** block terminates because of an exception that invokes the exception-handling block of a frame-based exception handler, the **\_\_finally** block is executed before the exception-handling block is executed.</span></span> <span data-ttu-id="02888-120">Entsprechend führt ein Aufruf der **longjmp** -C-Lauf Zeit Bibliotheksfunktion aus dem **\_ \_ try** -Block dazu, dass **\_ \_ der letzte Block ausgeführt** wird, bevor die Ausführung am Ziel des **longjmp** -Vorgangs fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="02888-120">Similarly, a call to the **longjmp** C run-time library function from the **\_\_try** block causes execution of the **\_\_finally** block before execution resumes at the target of the **longjmp** operation.</span></span> <span data-ttu-id="02888-121">Wenn die Ausführung des **\_ \_ try** -Blocks aufgrund einer Control-Anweisung (**Return**, **break**, **Continue** oder **goto**) beendet **\_ \_** wird, wird der letzte Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02888-121">If **\_\_try** block execution terminates due to a control statement (**return**, **break**, **continue**, or **goto**), the **\_\_finally** block is executed.</span></span>

<span data-ttu-id="02888-122">Mit der [**abnormalbeendigungs**](abnormaltermination.md) -Funktion kann innerhalb des letzten Blocks bestimmt werden, ob der **\_ \_ try** -Block nacheinander beendet wurde – d. h. ob er die schließende geschweifte Klammer (}) erreicht hat. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="02888-122">The [**AbnormalTermination**](abnormaltermination.md) function can be used within the **\_\_finally** block to determine whether the **\_\_try** block terminated sequentially — that is, whether it reached the closing brace (}).</span></span> <span data-ttu-id="02888-123">Das belassen des **\_ \_ try** -Blocks aufgrund eines Aufrufes **longjmp**, das Springen zu einem Ausnahmehandler oder eine **Return**-, **break**-, **Continue**-oder **goto** -Anweisung wird als nicht ordnungsgemäße Beendigung angesehen.</span><span class="sxs-lookup"><span data-stu-id="02888-123">Leaving the **\_\_try** block because of a call to **longjmp**, a jump to an exception handler, or a **return**, **break**, **continue**, or **goto** statement, is considered an abnormal termination.</span></span> <span data-ttu-id="02888-124">Beachten Sie, dass das System nicht sequenziell beendet wird, sondern alle Stapel Rahmen in umgekehrter Reihenfolge durchsucht, um zu bestimmen, ob Beendigungs Handler aufgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="02888-124">Note that failure to terminate sequentially causes the system to search through all stack frames in reverse order to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="02888-125">Dies kann zu Leistungseinbußen führen, da Hunderte von Anweisungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="02888-125">This can result in performance degradation due to the execution of hundreds of instructions.</span></span>

<span data-ttu-id="02888-126">Um eine ungewöhnliche Beendigung des Beendigungs Handlers zu vermeiden, sollte die Ausführung bis zum Ende des Blocks fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="02888-126">To avoid abnormal termination of the termination handler, execution should continue to the end of the block.</span></span> <span data-ttu-id="02888-127">Sie können auch die **\_ \_ Leave** -Anweisung ausführen.</span><span class="sxs-lookup"><span data-stu-id="02888-127">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="02888-128">Mit der **\_ \_ Leave** -Anweisung kann der **\_ \_ try** -Block sofort beendet werden, ohne dass eine ungewöhnliche Beendigung und die Leistungseinbußen entstehen.</span><span class="sxs-lookup"><span data-stu-id="02888-128">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="02888-129">Überprüfen Sie in der Compilerdokumentation, ob die **\_ \_ Leave** -Anweisung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="02888-129">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

<span data-ttu-id="02888-130">Wenn die **\_ \_ Ausführung des letzten Blocks aufgrund** der **Rückgabe** Steuerungs Anweisung beendet wird, entspricht Sie einer **goto** -Anweisung auf die schließende geschweifte Klammer in der einschließenden Funktion.</span><span class="sxs-lookup"><span data-stu-id="02888-130">If execution of the **\_\_finally** block terminates because of the **return** control statement, it is equivalent to a **goto** to the closing brace in the enclosing function.</span></span> <span data-ttu-id="02888-131">Daher gibt die einschließende Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="02888-131">Therefore, the enclosing function will return.</span></span>

 

 
