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
# <a name="causal-ordering-of-asynchronous-calls"></a><span data-ttu-id="ae794-103">Kausale Reihenfolge von asynchronen Aufrufen</span><span class="sxs-lookup"><span data-stu-id="ae794-103">Causal Ordering of Asynchronous Calls</span></span>

<span data-ttu-id="ae794-104">In einer asynchronen RPC-Anwendung ist es möglich, dass ein Client Thread einen zweiten asynchronen Aufruf für ein Bindungs handle ausführt, bevor ein früherer Aufruf für dieses Handle abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ae794-104">In an asynchronous RPC application, it is possible for a client thread to make a second asynchronous call on a binding handle before an earlier call made on that handle has completed.</span></span> <span data-ttu-id="ae794-105">Diese Situation wird von der RPC-Lauf Zeit Bibliothek wie folgt behandelt:</span><span class="sxs-lookup"><span data-stu-id="ae794-105">The RPC run-time library handles this situation as follows:</span></span>

-   <span data-ttu-id="ae794-106">Der asynchrone RPC-Mechanismus gewährleistet, dass asynchrone Aufrufe, die für denselben Bindungs Handle im gleichen Thread auf derselben Sicherheitsebene erfolgen, in der Reihenfolge verteilt werden, in der Sie vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="ae794-106">The asynchronous RPC mechanism guarantees that asynchronous calls made on the same binding handle, on the same thread, at the same security level, are dispatched in the order they were made.</span></span> <span data-ttu-id="ae794-107">Die tatsächliche Ausführung der Aufrufe kann nicht in der richtigen Reihenfolge erfolgen.</span><span class="sxs-lookup"><span data-stu-id="ae794-107">Actual execution of the calls may occur out of order.</span></span>
-   <span data-ttu-id="ae794-108">Wie bei synchronen Aufrufen werden asynchrone Remote Prozedur Aufrufe von unterschiedlichen Clientthreads gleichzeitig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae794-108">As with synchronous calls, asynchronous remote procedure calls from different client threads execute simultaneously.</span></span>
-   <span data-ttu-id="ae794-109">Wenn ein asynchroner Aufruf von einer Client Anwendung von einem oder mehreren synchronen Aufrufen gefolgt wird, kann der asynchrone Aufruf ausgeführt werden, während die synchronen Aufrufe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ae794-109">If an asynchronous call from a client application is followed by one or more synchronous calls, the asynchronous call can execute while the synchronous calls are executing.</span></span> <span data-ttu-id="ae794-110">Unabhängig vom Status des asynchronen Aufrufs werden die synchronen Aufrufe in der Reihenfolge ausgeführt, in der Sie vom Server empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="ae794-110">Regardless of the status of the asynchronous call, the synchronous calls are executed in the order in which they are received by the server.</span></span>
-   <span data-ttu-id="ae794-111">Wenn eine Client Anwendung eine nicht kausale Reihenfolge für ein bestimmtes Bindungs handle auswählt, wird die Serialisierung für dieses Handle deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ae794-111">If a client application selects noncausal ordering for a particular binding handle, it disables serialization for that handle.</span></span> <span data-ttu-id="ae794-112">Anwendungen ermöglichen eine nicht kausale Reihenfolge durch Aufrufen von [**rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) , wobei der *Option* -Parameter auf RPC \_ C \_ opt \_ Binding \_ nicht kausal und der *OptionValue* -Parameter auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ae794-112">Applications enable noncausal ordering by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) with the *Option* parameter set to RPC\_C\_OPT\_BINDING\_NONCAUSAL and the *OptionValue* parameter set to **TRUE**.</span></span> <span data-ttu-id="ae794-113">Weitere Informationen finden Sie unter [Bindungs Options Konstanten](binding-option-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ae794-113">For details, see [Binding Option Constants](binding-option-constants.md).</span></span>

 

 




