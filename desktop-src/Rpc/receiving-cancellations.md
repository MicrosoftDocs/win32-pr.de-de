---
title: Empfangen von Abbrüchen
description: Die Serveranwendung kann rpcservertestcancel mit dem Bindungs Handle des betreffenden Aufrufes aufzurufen, um herauszufinden, ob der Client den Abbruch des asynchronen Aufrufes angefordert hat. RPC S OK wird zurückgegeben, \_ \_ Wenn der Client den Aufruf abgebrochen hat.
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b8b48ef2796dab071ac705edf0ffca5156e235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037331"
---
# <a name="receiving-cancellations"></a><span data-ttu-id="1eecd-104">Empfangen von Abbrüchen</span><span class="sxs-lookup"><span data-stu-id="1eecd-104">Receiving Cancellations</span></span>

<span data-ttu-id="1eecd-105">Die Serveranwendung kann [**rpcservertestcancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) mit dem Bindungs Handle des betreffenden Aufrufes aufzurufen, um herauszufinden, ob der Client den Abbruch des asynchronen Aufrufes angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="1eecd-105">The server application can call [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) with the binding handle of the call in question to find out if the client has requested cancellation of the asynchronous call.</span></span> <span data-ttu-id="1eecd-106">RPC S OK wird zurückgegeben, \_ \_ Wenn der Client den Aufruf abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="1eecd-106">It will return RPC\_S\_OK if the client canceled the call.</span></span>

 

 




