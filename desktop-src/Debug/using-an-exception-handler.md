---
description: Die folgenden Beispiele veranschaulichen die Verwendung eines Ausnahme Handlers.
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: Verwenden eines Ausnahme Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dbe7ec23ddd5372cecfe85ae8348092d91cfff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346852"
---
# <a name="using-an-exception-handler"></a><span data-ttu-id="df562-103">Verwenden eines Ausnahme Handlers</span><span class="sxs-lookup"><span data-stu-id="df562-103">Using an Exception Handler</span></span>

<span data-ttu-id="df562-104">Die folgenden Beispiele veranschaulichen die Verwendung eines Ausnahme Handlers.</span><span class="sxs-lookup"><span data-stu-id="df562-104">The following examples demonstrate the use of an exception handler.</span></span>

## <a name="example-1"></a><span data-ttu-id="df562-105">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df562-105">Example 1</span></span>

<span data-ttu-id="df562-106">Im folgenden Code Fragment wird die strukturierte Ausnahmebehandlung verwendet, um zu überprüfen, ob ein Divisions Vorgang für 2 32-Bit-Ganzzahlen einen Fehler aufgrund einer Division durch 0 (null) verursacht.</span><span class="sxs-lookup"><span data-stu-id="df562-106">The following code fragment uses structured exception handling to check whether a division operation on two 32-bit integers will result in an division-by-zero error.</span></span> <span data-ttu-id="df562-107">Wenn dies auftritt, gibt die Funktion **false** zurück – andernfalls wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df562-107">If this occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>


```C++
BOOL SafeDiv(INT32 dividend, INT32 divisor, INT32 *pResult)
{
    __try 
    { 
        *pResult = dividend / divisor; 
    } 
    __except(GetExceptionCode() == EXCEPTION_INT_DIVIDE_BY_ZERO ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
    { 
        return FALSE;
    }
    return TRUE;
} 
```



## <a name="example-2"></a><span data-ttu-id="df562-108">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="df562-108">Example 2</span></span>

<span data-ttu-id="df562-109">Die folgende Beispiel Funktion Ruft die [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) -Funktion auf und verwendet die strukturierte Ausnahmebehandlung, um eine breakpointausnahme zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df562-109">The following example function calls the [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function and uses structured exception handling to check for a breakpoint exception.</span></span> <span data-ttu-id="df562-110">Wenn ein solcher auftritt, gibt die Funktion **false** zurück – andernfalls wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df562-110">If one occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>

<span data-ttu-id="df562-111">Der Filter Ausdruck im Beispiel verwendet die [**GetExceptionCode**](getexceptioncode.md) -Funktion, um den Ausnahmetyp vor dem Ausführen des Handlers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df562-111">The filter expression in the example uses the [**GetExceptionCode**](getexceptioncode.md) function to check the exception type before executing the handler.</span></span> <span data-ttu-id="df562-112">Dies ermöglicht es dem System, die Suche nach einem geeigneten Handler fortzusetzen, wenn ein anderer Ausnahmetyp auftritt.</span><span class="sxs-lookup"><span data-stu-id="df562-112">This enables the system to continue its search for an appropriate handler if some other type of exception occurs.</span></span>

<span data-ttu-id="df562-113">Außerdem unterscheidet sich die Verwendung der **Return** -Anweisung im **\_ \_ try** -Block eines Ausnahme Handlers von der Verwendung von **Return** im **\_ \_ try** -Block eines Beendigungs Handlers, der eine nicht ordnungsgemäße Beendigung des **\_ \_ try** -Blocks bewirkt.</span><span class="sxs-lookup"><span data-stu-id="df562-113">Also, use of the **return** statement in the **\_\_try** block of an exception handler differs from the use of **return** in the **\_\_try** block of a termination handler, which causes an abnormal termination of the **\_\_try** block.</span></span> <span data-ttu-id="df562-114">Dies ist eine gültige Verwendung der Return-Anweisung in einem Ausnahmehandler.</span><span class="sxs-lookup"><span data-stu-id="df562-114">This is an valid use of the return statement in an exception handler.</span></span>


```C++
BOOL CheckForDebugger()
{
    __try 
    {
        DebugBreak();
    }
    __except(GetExceptionCode() == EXCEPTION_BREAKPOINT ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH) 
    {
        // No debugger is attached, so return FALSE 
        // and continue.
        return FALSE;
    }
    return TRUE;
}
```



<span data-ttu-id="df562-115">Gibt nur \_ einen Ausnahme Ausführungs \_ Handler von einem Ausnahme Filter zurück, wenn der Ausnahmetyp erwartet wird und die fehleradressadresse bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="df562-115">Only return EXCEPTION\_EXECUTE\_HANDLER from an exception filter when the exception type is expected and the faulting address is known.</span></span> <span data-ttu-id="df562-116">Sie sollten zulassen, dass der Standard Ausnahmehandler unerwartete Ausnahme Typen und Fehler Adressen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="df562-116">You should allow the default exception handler to process unexpected exception types and faulting addresses.</span></span>

## <a name="example-3"></a><span data-ttu-id="df562-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="df562-117">Example 3</span></span>

<span data-ttu-id="df562-118">Das folgende Beispiel zeigt die Interaktion von schsted Handlern.</span><span class="sxs-lookup"><span data-stu-id="df562-118">The following example shows the interaction of nested handlers.</span></span> <span data-ttu-id="df562-119">Die [**raianexception**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) -Funktion verursacht eine Ausnahme im überwachten Text eines Beendigungs Handlers, der sich innerhalb des überwachten Texts eines Ausnahme Handlers befindet.</span><span class="sxs-lookup"><span data-stu-id="df562-119">The [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) function causes an exception in the guarded body of a termination handler that is inside the guarded body of an exception handler.</span></span> <span data-ttu-id="df562-120">Die Ausnahme bewirkt, dass das System die FilterFunction-Funktion auswertet, deren Rückgabewert wiederum bewirkt, dass der Ausnahmehandler aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="df562-120">The exception causes the system to evaluate the FilterFunction function, whose return value in turn causes the exception handler to be invoked.</span></span> <span data-ttu-id="df562-121">Bevor der Ausnahmehandlerblock ausgeführt wird, wird jedoch der letzte Block des Beendigungs Handlers ausgeführt, da der Steuerungs Fluss den **\_ \_ try** -Block des Beendigungs Handlers verlassen hat. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="df562-121">However, before the exception-handler block is executed, the **\_\_finally** block of the termination handler is executed because the flow of control has left the **\_\_try** block of the termination handler.</span></span>


```C++
DWORD FilterFunction() 
{ 
    printf("1 ");                     // printed first 
    return EXCEPTION_EXECUTE_HANDLER; 
} 
 
VOID main(VOID) 
{ 
    __try 
    { 
        __try 
        { 
            RaiseException( 
                1,                    // exception code 
                0,                    // continuable exception 
                0, NULL);             // no arguments 
        } 
        __finally 
        { 
            printf("2 ");             // this is printed second 
        } 
    } 
    __except ( FilterFunction() ) 
    { 
        printf("3\n");                // this is printed last 
    } 
}
```



 

 
