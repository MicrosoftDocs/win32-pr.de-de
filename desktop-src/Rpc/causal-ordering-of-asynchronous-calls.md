---
title: Kausale Reihenfolge asynchroner Aufrufe
description: In einer asynchronen RPC-Anwendung kann ein Clientthread einen zweiten asynchronen Aufruf für ein Bindungshandle vornehmen, bevor ein früherer Aufruf dieses Handles abgeschlossen wurde.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbafc5f9166d28a80d514abd4ebea20ab01ea32f542561e2108feae4a5769458
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932294"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Kausale Reihenfolge asynchroner Aufrufe

In einer asynchronen RPC-Anwendung kann ein Clientthread einen zweiten asynchronen Aufruf für ein Bindungshandle vornehmen, bevor ein früherer Aufruf dieses Handles abgeschlossen wurde. Die RPC-Laufzeitbibliothek behandelt diese Situation wie folgt:

-   Der asynchrone RPC-Mechanismus garantiert, dass asynchrone Aufrufe, die für dasselbe Bindungshandle auf demselben Thread auf der gleichen Sicherheitsebene erfolgen, in der Reihenfolge gesendet werden, in der sie durchgeführt wurden. Die tatsächliche Ausführung der Aufrufe kann nicht in der reihenfolgengeordneten Reihenfolge erfolgen.
-   Wie bei synchronen Aufrufen werden asynchrone Remoteprozeduraufrufe aus verschiedenen Clientthreads gleichzeitig ausgeführt.
-   Wenn einem asynchronen Aufruf einer Clientanwendung ein oder mehrere synchrone Aufrufe folgen, kann der asynchrone Aufruf ausgeführt werden, während die synchronen Aufrufe ausgeführt werden. Unabhängig vom Status des asynchronen Aufrufs werden die synchronen Aufrufe in der Reihenfolge ausgeführt, in der sie vom Server empfangen werden.
-   Wenn eine Clientanwendung die nichtausale Reihenfolge für ein bestimmtes Bindungshandle auswählt, wird die Serialisierung für dieses Handle deaktiviert. Anwendungen ermöglichen die nichtausale Sortierung, indem [**Sie RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) aufrufen, wobei der *Option-Parameter* auf RPC \_ C OPT BINDING \_ \_ \_ NONCAUSAL und der *OptionValue-Parameter* auf **TRUE** festgelegt ist. Weitere Informationen finden Sie unter [Bindungsoptionskonstanten.](binding-option-constants.md)

 

 




