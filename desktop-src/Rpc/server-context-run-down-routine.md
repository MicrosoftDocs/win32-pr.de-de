---
title: Run-down-Routine für Den Serverkontext
description: Wenn die Kommunikation unterbricht, während der Server den Kontext im Auftrag des Clients verwaltet, ist möglicherweise eine Bereinigungsroutine erforderlich, um den vom Server verwalteten Zustand im Namen eines bestimmten Clients zu bereinigt.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3bab4477555e5a304627d026c7471874af50daceb9fe3e4484928c290a55d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035490"
---
# <a name="server-context-run-down-routine"></a>Run-down-Routine für Den Serverkontext

Wenn die Kommunikation unterbricht, während der Server den Kontext im Auftrag des Clients verwaltet, ist möglicherweise eine Bereinigungsroutine erforderlich, um den vom Server verwalteten Zustand im Namen eines bestimmten Clients zu bereinigt. Diese Bereinigungsroutine wird als *Kontext-Run-Down-Routine bezeichnet.* Wenn eine Verbindung unterbricht, rufen der Serverstub und die Laufzeitbibliothek diese Routine auf jedem kontextbasierten Handle auf, das vom Client geöffnet wird.

Die Run-Down-Routine des Kontexts ist erforderlich und wird implizit deklariert und benannt, wenn Sie das Kontexthandpunktattribut auf \[ **\_** \] eine Typdefinition anwenden. Der Server wird die Run-Down-Routine des Kontexts nicht aufrufen, wenn das \[ **Context \_ Handle-Attribut** \] direkt auf einen Parameter angewendet wurde.

Die Routinesyntax für die Kontext run-down ist:

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

Beachten Sie, dass der Typname den Namen der Kontext-Run-Down-Routine bestimmt.

Das folgende Codefragment stellt eine Beispielkontext-Run-Down-Routine vor. , die die RemoteClose-Prozedur aufruft, die im Beispiel unter Schnittstellenentwicklung [mithilfe](interface-development-using-context-handles.md)von Kontexthandles, [Serverentwicklung mit](server-development-using-context-handles.md)Kontexthandles und Cliententwicklung mithilfe von [Kontexthandles verwendet wird.](client-development-using-context-handles.md) Diese Prozedur schließt das Dateihand handle, gibt den der Datei zugeordneten Arbeitsspeicher frei und weist dem Kontexthand handle **NULL** zu. Das Zuweisen **von NULL** ist das Ergebnis des Aufrufs der RemoteClose-Funktion und in einem Run-Down-Szenario nicht erforderlich. Die RPC-Laufzeit bereinigt ihren Zustand unabhängig davon, ob das Kontexthand handle auf **NULL festgelegt ist.**

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




