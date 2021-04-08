---
title: Verwenden von Bindungs Handles und Senden von RPC-Aufrufen
description: Ein häufiger Fehler bei RPC-Programmierern besteht darin, alle Ausnahmen zu behandeln.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728849"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a>Verwenden von Bindungs Handles und Senden von RPC-Aufrufen

Ein häufiger Fehler bei RPC-Programmierern besteht darin, alle Ausnahmen zu behandeln. Viele Programmierer strukturieren ihre Ausnahme Handles wie folgt:

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

Das Problem mit diesem Handler besteht darin, dass alle Fehler, einschließlich der Fehler im Client Programm, abgefangen werden. Das Abfangen von Fehlern im Client Programm erschwert das Debuggen. Die richtige Methode zum Strukturieren eines Ausnahme Handlers ist Folgendes:

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

Dieser Ausnahmehandler hat den Vorteil, dass ein bestimmter Bereich von Fehlern durch ermöglicht wird. Diese Fehler werden vom Server nie zurückgegeben, da Sie auf ein Client seitiges Problem hindeuten.

Außerdem wird empfohlen, die **\[** [strengen Kontext \_ handle \_](/windows/desktop/Midl/strict-context-handle) **\]** -und **\[** [ \_ typstrict- \_ Kontext \_ handle](/windows/desktop/Midl/type-strict-context-handle)- **\]** Attribute zu verwenden, um sicherzustellen, dass die RPC-Laufzeit ein Kontext Handle für eine Schnittstelle erstellt, die nur als Argument an Methoden dieser Schnittstelle weitergeleitet werden kann. Dadurch werden Server Fehler verhindert, die auftreten, wenn Kontext Handles geöffnet und zwischen verschiedenen Schnittstellen, die innerhalb desselben Prozesses vorhanden sind, übermittelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Strict- \_ Kontext \_ handle](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[Typ \_ Strict- \_ Kontext \_ handle](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 