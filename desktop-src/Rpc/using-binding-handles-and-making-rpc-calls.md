---
title: Verwenden von Bindungshandles und Tätigen von RPC-Aufrufen
description: Ein häufiger Fehler bei RPC-Programmierern ist die Behandlung aller Ausnahmen.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1350e29344d09f42417a30fa3d32729d7ddd02247b17f80bccd0ae537c6c8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010808"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a>Verwenden von Bindungshandles und Tätigen von RPC-Aufrufen

Ein häufiger Fehler bei RPC-Programmierern ist die Behandlung aller Ausnahmen. Viele Programmierer strukturieren ihre Ausnahmehandles wie folgt:

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

Das Problem mit diesem Handler ist, dass er alle Fehler abfängt, einschließlich der Fehler im Clientprogramm. Das Abfangen von Fehlern im Clientprogramm erschwert das Debuggen. Die richtige Methode zum Strukturieren eines Ausnahmehandlers ist die folgende:

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

Dieser Ausnahmehandler hat den Vorteil, dass er einen bestimmten Fehlerbereich durchlassen kann. Diese Fehler werden nie vom Server zurückgegeben, da sie auf ein clientseitiges Problem hinweisen.

Darüber hinaus wird die Verwendung des strict-Kontexthandpunkts und der typ strict context **\[** [ \_ \_](/windows/desktop/Midl/strict-context-handle) **\]** **\[** [ \_ \_ \_ handle-Attribute](/windows/desktop/Midl/type-strict-context-handle)empfohlen, um sicherzustellen, dass die RPC-Laufzeit ein Kontexthand handle auf einer Schnittstelle erstellt, die nur als Argument an Methoden dieser Schnittstelle übergeben werden **\]** kann. Dadurch werden Serverfehler verhindert, die auftreten, wenn Kontexthandles geöffnet und zwischen verschiedenen Schnittstellen übergeben werden, die innerhalb desselben Prozesses vorhanden sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Strict \_ Context \_ Handle](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[Type \_ \_ Strict-Kontexthand \_ handle](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 