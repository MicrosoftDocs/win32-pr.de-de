---
title: Verwenden von asynchronem RPC mit DCE-Pipes
description: Microsoft RPC unterstützt die Verwendung von DCE-Pipes. Obwohl Sie einen ähnlichen Namen haben, sind DCE-Pipes nicht mit Named Pipes verknüpft. Named Pipes sind ein Transportprotokoll. DCE-Pipes sind eine Protokoll unabhängige Methode der Client/Server-Kommunikation.
ms.assetid: 9de4f6dc-0aa9-446e-b68c-e0d1e247fea7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e9c98f4d4191a064d78cff2c918077f27d676f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036916"
---
# <a name="using-asynchronous-rpc-with-dce-pipes"></a><span data-ttu-id="840fe-106">Verwenden von asynchronem RPC mit DCE-Pipes</span><span class="sxs-lookup"><span data-stu-id="840fe-106">Using Asynchronous RPC with DCE Pipes</span></span>

<span data-ttu-id="840fe-107">Microsoft RPC unterstützt die Verwendung von DCE-Pipes.</span><span class="sxs-lookup"><span data-stu-id="840fe-107">Microsoft RPC supports the use of DCE pipes.</span></span> <span data-ttu-id="840fe-108">Obwohl Sie einen ähnlichen Namen haben, sind DCE-Pipes nicht mit [Named Pipes](asynchronous-rpc-over-the-named-pipe-protocol.md)verknüpft.</span><span class="sxs-lookup"><span data-stu-id="840fe-108">Although they share a similar name, DCE pipes are unrelated to [named pipes](asynchronous-rpc-over-the-named-pipe-protocol.md).</span></span> <span data-ttu-id="840fe-109">Named Pipes sind ein Transportprotokoll.</span><span class="sxs-lookup"><span data-stu-id="840fe-109">Named pipes are a transport protocol.</span></span> <span data-ttu-id="840fe-110">DCE-Pipes sind eine Protokoll unabhängige Methode der Client/Server-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="840fe-110">DCE pipes are a protocol-independent method of client/server communication.</span></span>

<span data-ttu-id="840fe-111">In diesem Abschnitt wird die RPC-Verwendung von asynchronen DCE-Pipes erläutert.</span><span class="sxs-lookup"><span data-stu-id="840fe-111">This section presents a discussion of RPC using asynchronous DCE pipes.</span></span> <span data-ttu-id="840fe-112">Es ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="840fe-112">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="840fe-113">Asynchrone Pipes</span><span class="sxs-lookup"><span data-stu-id="840fe-113">Asynchronous Pipes</span></span>](asynchronous-pipes.md)
-   [<span data-ttu-id="840fe-114">Deklarieren von asynchronen Pipes</span><span class="sxs-lookup"><span data-stu-id="840fe-114">Declaring Asynchronous Pipes</span></span>](declaring-asynchronous-pipes.md)
-   [<span data-ttu-id="840fe-115">Client seitige asynchrone Pipe-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="840fe-115">Client-side Asynchronous Pipe Handling</span></span>](client-side-asynchronous-pipe-handling.md)
-   [<span data-ttu-id="840fe-116">Server seitige asynchrone Pipe-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="840fe-116">Server-side Asynchronous Pipe Handling</span></span>](server-side-asynchronous-pipe-handling.md)

<span data-ttu-id="840fe-117">Eine Beispiel-RPC-Anwendung für eine asynchrone Pipe finden Sie im filerep-Beispiel im Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="840fe-117">For a sample asynchronous pipe RPC application, see the FileRep sample in the Platform Software Development Kit (SDK).</span></span>

 

 




