---
title: Verarbeiten von asynchronen Aufrufen
description: Die Manager-Routine einer asynchronen Funktion empfängt immer das asynchrone Handle als ersten Parameter. Der Server muss dieses Handle nachverfolgen und zum Senden der Antwort verwenden, wenn der asynchrone Remote Prozedur Aufrufvorgang abgeschlossen ist.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388420"
---
# <a name="handling-asynchronous-calls"></a><span data-ttu-id="243e6-104">Verarbeiten von asynchronen Aufrufen</span><span class="sxs-lookup"><span data-stu-id="243e6-104">Handling Asynchronous Calls</span></span>

<span data-ttu-id="243e6-105">Die Manager-Routine einer asynchronen Funktion empfängt immer das asynchrone Handle als ersten Parameter.</span><span class="sxs-lookup"><span data-stu-id="243e6-105">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="243e6-106">Der Server muss dieses Handle nachverfolgen und zum Senden der Antwort verwenden, wenn der asynchrone Remote Prozedur Aufrufvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="243e6-106">The server must keep track of this handle and use it to send the reply when the asynchronous remote procedure call finishes.</span></span>

<span data-ttu-id="243e6-107">Wenn der Server einen asynchronen RPC abbrechen muss, wird [**rpcasyncabortcallaufgerufen**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span><span class="sxs-lookup"><span data-stu-id="243e6-107">If the server needs to abort an asynchronous RPC, it calls [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span></span> <span data-ttu-id="243e6-108">Diese Funktion führt dieselbe serverseitige Bereinigung wie [**rpcasynccompletecalldurch**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) und gibt einen Ausnahme Code (von der Serveranwendung bereitgestellt) an den Client zurück, mit dem Unterschied, dass er keine Marshalling der out-Argumente ausführt.</span><span class="sxs-lookup"><span data-stu-id="243e6-108">This function performs the same server-side cleanup as [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) and propagates an exception code (provided by the server application) back to the client, except that it does not perform marshalling of the out arguments.</span></span>

<span data-ttu-id="243e6-109">Ein Beispiel für eine asynchrone Prozedur finden Sie unter [Senden der asynchronen Antwort](sending-the-asynchronous-reply.md).</span><span class="sxs-lookup"><span data-stu-id="243e6-109">For an example of an asynchronous procedure, see [Sending the Asynchronous Reply](sending-the-asynchronous-reply.md).</span></span>

 

 




