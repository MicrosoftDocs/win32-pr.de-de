---
title: Weitergeben von Fehlerinformationen
description: Durch die Weitergabe erweiterter Fehlerinformationen können Server, die einen RPC- \_ \_ Fehler oder einen anderen Fehlercode erhalten, die von der RPC-Laufzeit empfangenen Informationen an die Aufrufer weitergeben.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856668"
---
# <a name="propagating-error-information"></a><span data-ttu-id="c4264-103">Weitergeben von Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="c4264-103">Propagating Error Information</span></span>

<span data-ttu-id="c4264-104">Das weitergeben erweiterter Fehlerinformationen ermöglicht Servern, die einen RPC- \_ \_ \* Fehler oder einen anderen Fehlercode erhalten, das Weitergeben der empfangenen Informationen an die Aufrufer durch die RPC-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="c4264-104">Propagating extended error information allows servers that receive an RPC\_S\_\* error, or any other error code for that matter, to allow the RPC run time to propagate the information it received to its callers.</span></span> <span data-ttu-id="c4264-105">Der Server muss beim Auftreten eines schwerwiegenden Fehlers [**rpcraiseexception**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) oder [**rpcasyncabortcallaufgerufen**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) werden.</span><span class="sxs-lookup"><span data-stu-id="c4264-105">All the server must do is call the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) or [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) upon encountering a fatal error.</span></span> <span data-ttu-id="c4264-106">Die RPC-Laufzeit übernimmt ggf. die Verkettung der erweiterten Fehlerinformationen, was den schwerwiegenden Fehler verursacht, um den schwerwiegenden Fehler zu melden, sofern der Fehlercode für **rpcraiseexception** oder **rpcasyncabortcallcenter** mit dem Fehlercode übereinstimmt, der den schwerwiegenden Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="c4264-106">The RPC run time takes care of chaining the extended error information, if any, causing the fatal error to report the fatal error itself, as long as the error code given to **RpcRaiseException** or **RpcAsyncAbortCall** is the same as the error code causing the fatal error.</span></span>

 

 




