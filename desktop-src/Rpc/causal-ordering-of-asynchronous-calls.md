---
title: Kausale Reihenfolge von asynchronen Aufrufen
description: In einer asynchronen RPC-Anwendung ist es möglich, dass ein Client Thread einen zweiten asynchronen Aufruf für ein Bindungs handle ausführt, bevor ein früherer Aufruf für dieses Handle abgeschlossen wurde.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036883"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Kausale Reihenfolge von asynchronen Aufrufen

In einer asynchronen RPC-Anwendung ist es möglich, dass ein Client Thread einen zweiten asynchronen Aufruf für ein Bindungs handle ausführt, bevor ein früherer Aufruf für dieses Handle abgeschlossen wurde. Diese Situation wird von der RPC-Lauf Zeit Bibliothek wie folgt behandelt:

-   Der asynchrone RPC-Mechanismus gewährleistet, dass asynchrone Aufrufe, die für denselben Bindungs Handle im gleichen Thread auf derselben Sicherheitsebene erfolgen, in der Reihenfolge verteilt werden, in der Sie vorgenommen wurden. Die tatsächliche Ausführung der Aufrufe kann nicht in der richtigen Reihenfolge erfolgen.
-   Wie bei synchronen Aufrufen werden asynchrone Remote Prozedur Aufrufe von unterschiedlichen Clientthreads gleichzeitig ausgeführt.
-   Wenn ein asynchroner Aufruf von einer Client Anwendung von einem oder mehreren synchronen Aufrufen gefolgt wird, kann der asynchrone Aufruf ausgeführt werden, während die synchronen Aufrufe ausgeführt werden. Unabhängig vom Status des asynchronen Aufrufs werden die synchronen Aufrufe in der Reihenfolge ausgeführt, in der Sie vom Server empfangen werden.
-   Wenn eine Client Anwendung eine nicht kausale Reihenfolge für ein bestimmtes Bindungs handle auswählt, wird die Serialisierung für dieses Handle deaktiviert. Anwendungen ermöglichen eine nicht kausale Reihenfolge durch Aufrufen von [**rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) , wobei der *Option* -Parameter auf RPC \_ C \_ opt \_ Binding \_ nicht kausal und der *OptionValue* -Parameter auf **true** festgelegt ist. Weitere Informationen finden Sie unter [Bindungs Options Konstanten](binding-option-constants.md).

 

 




