---
title: Asynchrone Pipes
description: Mithilfe von Pipe-Parametern mit asynchronem RPC können Sie Daten inkrementell übertragen, sobald Sie verfügbar werden, ohne den Client und den Server zu binden.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729432"
---
# <a name="asynchronous-pipes"></a><span data-ttu-id="20369-103">Asynchrone Pipes</span><span class="sxs-lookup"><span data-stu-id="20369-103">Asynchronous Pipes</span></span>

<span data-ttu-id="20369-104">Mithilfe von [Pipe](/windows/desktop/Midl/pipe) -Parametern mit asynchronem RPC können Sie Daten inkrementell übertragen, sobald Sie verfügbar werden, ohne den Client und den Server zu binden.</span><span class="sxs-lookup"><span data-stu-id="20369-104">Using [pipe](/windows/desktop/Midl/pipe) parameters with asynchronous RPC allows you to transmit data incrementally, as it becomes available, without tying up the client and server.</span></span> <span data-ttu-id="20369-105">Dies ist besonders nützlich, wenn Sie über eine große Menge an zu übertragenden Daten verfügen, in Kombination mit einem langsamen Client, einem langsamen Server oder einem langsamen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="20369-105">This is particularly useful when you have a large amount of data to transfer, combined with a slow client, a slow server, or a slow network.</span></span> <span data-ttu-id="20369-106">Wenn Sie eine Pipe in einem asynchronen Funktionsaufruf verwenden, handelt es sich um eine asynchrone Pipe.</span><span class="sxs-lookup"><span data-stu-id="20369-106">If you use a pipe in an asynchronous function call, it is, by definition, an asynchronous pipe.</span></span> <span data-ttu-id="20369-107">Synchrone Pipes werden nicht in Verbindung mit asynchronen Funktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="20369-107">Synchronous pipes are not supported in conjunction with asynchronous functions.</span></span>

<span data-ttu-id="20369-108">Im Gegensatz zu herkömmlichen (synchronen) Pipes, bei denen der Server alle Details zum Senden und empfangen von pipedaten verarbeitet, sind asynchrone Pipes symmetrisch.</span><span class="sxs-lookup"><span data-stu-id="20369-108">Unlike conventional (synchronous) pipes where the server handles all the details of sending and receiving pipe data, asynchronous pipes are symmetrical.</span></span> <span data-ttu-id="20369-109">Das heißt, sowohl der Client als auch der Server können Daten per Push per Push durchlaufen und per Pull über die Pipe abrufen</span><span class="sxs-lookup"><span data-stu-id="20369-109">That is, both the client and the server can push and pull data through the pipe.</span></span>

> [!Note]  
> <span data-ttu-id="20369-110">Pipe-Parameter können nur als Verweis übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="20369-110">Pipe parameters can only be passed by reference.</span></span> <span data-ttu-id="20369-111">Auch wenn die IDL-Datei die [Pipeline](/windows/desktop/Midl/pipe) Parameter anzeigt, die als Wert übergeben werden, akzeptieren die generierten stubwerte nur die Pipeline Parameter als Verweis.</span><span class="sxs-lookup"><span data-stu-id="20369-111">Even if the IDL file shows [pipe](/windows/desktop/Midl/pipe) parameters being passed by value, the generated stubs will accept pipe parameters by reference only.</span></span>

 

<span data-ttu-id="20369-112">In der folgenden Erörterung von asynchronen Pipes wird die Vertrautheit mit dem pipetypkonstruktor angenommen.</span><span class="sxs-lookup"><span data-stu-id="20369-112">In the following discussion of asynchronous pipes, familiarity with the pipe type constructor is assumed.</span></span> <span data-ttu-id="20369-113">Weitere Informationen zu den in diesen Themen beschriebenen Pipe-Prozeduren finden Sie unter [Pipes](pipes.md).</span><span class="sxs-lookup"><span data-stu-id="20369-113">For more information on the pipe procedures described in these topics, see [Pipes](pipes.md).</span></span>

 

 