---
title: Server Kontext-Lauf-ab-Routine
description: Wenn die Kommunikation unterbrochen wird, während der Server im Auftrag des Clients den Kontext beibehält, ist möglicherweise eine cleanuproutine erforderlich, um den Zustand des Servers im Auftrag eines bestimmten Clients zu bereinigen.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037407"
---
# <a name="server-context-run-down-routine"></a>Server Kontext-Lauf-ab-Routine

Wenn die Kommunikation unterbrochen wird, während der Server im Auftrag des Clients den Kontext beibehält, ist möglicherweise eine cleanuproutine erforderlich, um den Zustand des Servers im Auftrag eines bestimmten Clients zu bereinigen. Diese cleanuproutine wird als *Kontext-Lauf Routine Routine* bezeichnet. Wenn eine Verbindung unterbrochen wird, wird diese Routine vom Serverstub und der Lauf Zeit Bibliothek für jedes Kontext Handle aufgerufen, das vom Client geöffnet wurde.

Die Kontext-Lauf Zeit Routine ist erforderlich und wird implizit deklariert und benannt, wenn Sie das \[ **Kontext \_ handle** - \] Attribut auf eine Typdefinition anwenden. Der Server Ruft die Kontext-run-down-Routine nicht auf, wenn das \[ **Kontext \_ handle** - \] Attribut direkt auf einen Parameter angewendet wurde.

Die Syntax der Kontext-laufbetrieb Routine ist:

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

Beachten Sie, dass der Typname den Namen der Kontext-run-down-Routine bestimmt.

Das folgende Code Fragment stellt eine Beispiel-Kontext-Lauf Routine Routine dar. , die die im Beispiel verwendete remoteclose-Prozedur in der [Schnittstellen Entwicklung mithilfe von Kontext Handles](interface-development-using-context-handles.md), der [Server Entwicklung mithilfe von Kontext](server-development-using-context-handles.md)Handles und der [Client Entwicklung mithilfe von Kontext Handles](client-development-using-context-handles.md)aufruft. Diese Prozedur schließt das Datei Handle, gibt den der Datei zugeordneten Arbeitsspeicher frei und weist dem Kontext Handle den Wert **null** zu. Das Zuweisen von **null** ist das Ergebnis des Aufrufs der Funktion remoteclose und ist in einem-Lauf Fall Szenario nicht erforderlich. Die RPC-Laufzeit bereinigt den Status, unabhängig davon, ob das Kontext Handle auf **null** festgelegt ist.

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

 

 




