---
title: Empfangen der asynchronen Antwort
description: Nachdem die Benachrichtigung gesendet wurde, dass der Server eine Antwort gesendet hat, ruft der Client rpcasynccompletecallcenter mit dem asynchronen Handle auf, damit er die Antwort empfangen kann.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390893"
---
# <a name="receiving-the-asynchronous-reply"></a><span data-ttu-id="ba757-103">Empfangen der asynchronen Antwort</span><span class="sxs-lookup"><span data-stu-id="ba757-103">Receiving the Asynchronous Reply</span></span>

<span data-ttu-id="ba757-104">Nachdem die Benachrichtigung gesendet wurde, dass der Server eine Antwort gesendet hat, ruft der Client [**rpcasynccompletecallcenter**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) mit dem asynchronen Handle auf, damit er die Antwort empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="ba757-104">After it is notified that the server has sent a reply, the client calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) with the asynchronous handle so that it can receive the reply.</span></span> <span data-ttu-id="ba757-105">Wenn **rpcasynccompletecallcenter** erfolgreich abgeschlossen wurde, verweist der *Antwort* Parameter auf einen Puffer, der den Rückgabewert der Remote Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="ba757-105">When **RpcAsyncCompleteCall** has completed successfully, the *Reply* parameter points to a buffer that contains the return value of the remote function.</span></span> <span data-ttu-id="ba757-106">Alle Puffer, die vom Client Programm als \[ [**out**](/windows/desktop/Midl/out-idl) \] oder \[ [**in**](/windows/desktop/Midl/in)bereit  gestellt werden, \] enthalten die Out-Parameter für die asynchrone Remote Funktion, die gültige Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba757-106">Any buffers supplied by the client program as \[[**out**](/windows/desktop/Midl/out-idl)\] or \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to the asynchronous remote function contain valid data.</span></span> <span data-ttu-id="ba757-107">Wenn der Client **rpcasynccompletecallaufruft** , bevor der Server die Antwort gesendet hat, schlägt dieser Aufruf fehl, und es wird ein Wert von RPC \_ S \_ Async- \_ Aufruf \_ Ausstehend zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba757-107">If the client calls **RpcAsyncCompleteCall** before the server has sent the reply, that call will fail and return a value of RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="ba757-108">Wenn Ihr Client Programm e/a-Abschlussports oder-Ereignisse für die Benachrichtigung verwendet, muss es [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) zum Freigeben des Ports oder Handles aufruft, wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ba757-108">If your client program uses I/O completion ports or events for notification, it must call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to release the port or handle when it no longer needs them.</span></span>

 

 