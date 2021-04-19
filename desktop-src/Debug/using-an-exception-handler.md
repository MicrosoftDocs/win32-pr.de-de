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
# <a name="using-an-exception-handler"></a>Verwenden eines Ausnahme Handlers

Die folgenden Beispiele veranschaulichen die Verwendung eines Ausnahme Handlers.

## <a name="example-1"></a>Beispiel 1

Im folgenden Code Fragment wird die strukturierte Ausnahmebehandlung verwendet, um zu überprüfen, ob ein Divisions Vorgang für 2 32-Bit-Ganzzahlen einen Fehler aufgrund einer Division durch 0 (null) verursacht. Wenn dies auftritt, gibt die Funktion **false** zurück – andernfalls wird **true** zurückgegeben.


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



## <a name="example-2"></a>Beispiel 2

Die folgende Beispiel Funktion Ruft die [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) -Funktion auf und verwendet die strukturierte Ausnahmebehandlung, um eine breakpointausnahme zu überprüfen. Wenn ein solcher auftritt, gibt die Funktion **false** zurück – andernfalls wird **true** zurückgegeben.

Der Filter Ausdruck im Beispiel verwendet die [**GetExceptionCode**](getexceptioncode.md) -Funktion, um den Ausnahmetyp vor dem Ausführen des Handlers zu überprüfen. Dies ermöglicht es dem System, die Suche nach einem geeigneten Handler fortzusetzen, wenn ein anderer Ausnahmetyp auftritt.

Außerdem unterscheidet sich die Verwendung der **Return** -Anweisung im **\_ \_ try** -Block eines Ausnahme Handlers von der Verwendung von **Return** im **\_ \_ try** -Block eines Beendigungs Handlers, der eine nicht ordnungsgemäße Beendigung des **\_ \_ try** -Blocks bewirkt. Dies ist eine gültige Verwendung der Return-Anweisung in einem Ausnahmehandler.


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



Gibt nur \_ einen Ausnahme Ausführungs \_ Handler von einem Ausnahme Filter zurück, wenn der Ausnahmetyp erwartet wird und die fehleradressadresse bekannt ist. Sie sollten zulassen, dass der Standard Ausnahmehandler unerwartete Ausnahme Typen und Fehler Adressen verarbeitet.

## <a name="example-3"></a>Beispiel 3

Das folgende Beispiel zeigt die Interaktion von schsted Handlern. Die [**raianexception**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) -Funktion verursacht eine Ausnahme im überwachten Text eines Beendigungs Handlers, der sich innerhalb des überwachten Texts eines Ausnahme Handlers befindet. Die Ausnahme bewirkt, dass das System die FilterFunction-Funktion auswertet, deren Rückgabewert wiederum bewirkt, dass der Ausnahmehandler aufgerufen wird. Bevor der Ausnahmehandlerblock ausgeführt wird, wird jedoch der letzte Block des Beendigungs Handlers ausgeführt, da der Steuerungs Fluss den **\_ \_ try** -Block des Beendigungs Handlers verlassen hat. **\_ \_**


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



 

 
