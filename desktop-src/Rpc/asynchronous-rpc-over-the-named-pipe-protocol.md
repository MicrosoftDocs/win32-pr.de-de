---
title: Asynchroner RPC über das Named-Pipe Protokoll
description: Wenn Sie Named Pipes (ncacn \_ NP) als Transportprotokoll verwenden, sollten Sie eine große Anzahl von ausstehenden aufrufen auf dem Server vermeiden.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949039"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a><span data-ttu-id="e6198-103">Asynchroner RPC über das Named-Pipe Protokoll</span><span class="sxs-lookup"><span data-stu-id="e6198-103">Asynchronous RPC over the Named-Pipe Protocol</span></span>

<span data-ttu-id="e6198-104">Wenn Sie Named Pipes ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) als Transportprotokoll verwenden, sollten Sie eine große Anzahl von ausstehenden aufrufen auf dem Server vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e6198-104">If you use named pipes ([**ncacn\_np**](/windows/desktop/Midl/ncacn-np)) as your transport protocol, you should avoid allowing a large number of idle pending calls on the server.</span></span> <span data-ttu-id="e6198-105">Bei Named Pipes weist jeder Client, der auf eine Antwort wartet, eine ausstehende Named Pipe auf dem Server auf, für die jeweils eine bestimmte Menge an Kernel Speicher erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e6198-105">With named pipes, each client waiting for a reply will have a pending named pipe read on the server, each of which requires a certain amount of kernel memory.</span></span>

<span data-ttu-id="e6198-106">Beispielsweise möchten Sie keinen Benachrichtigungs Befehl für eine neue e-Mail-Adresse mit dem Named Pipe-Transport verwenden, da ein solcher aufrufener auch dann aussteht, wenn sich Clients im Leerlauf befinden und der Kernel Speicher erschöpft sein könnte.</span><span class="sxs-lookup"><span data-stu-id="e6198-106">For example, you would not want to use a notification call for new e-mail with the named-pipe transport, because such a call would remain pending even when clients are idle, and kernel memory could be depleted.</span></span> <span data-ttu-id="e6198-107">Beachten Sie, dass dies kein Problem mit den anderen Verbindungs orientierten Protokollen ist, wie z. b. [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).</span><span class="sxs-lookup"><span data-stu-id="e6198-107">Note that this is not a problem with the other connection-oriented protocols, such as [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp).</span></span>

<span data-ttu-id="e6198-108">Da Named Pipes ein Transportprotokoll sind, kann Sie von Ihrer Anwendung verwendet werden, indem [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) als Protokoll in einer Zeichen folgen Bindung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e6198-108">Since named pipes are a transport protocol, your application can use them by specifying [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) as the protocol in a string binding.</span></span> <span data-ttu-id="e6198-109">Weitere Informationen zu Named Pipes finden Sie unter [Named Pipes](/windows/desktop/ipc/named-pipes).</span><span class="sxs-lookup"><span data-stu-id="e6198-109">For more information on named pipes, see [Named Pipes](/windows/desktop/ipc/named-pipes).</span></span> <span data-ttu-id="e6198-110">Ausführliche Informationen zum Erstellen von Zeichen folgen Bindungen finden [Sie unter Verwenden von Zeichen folgen Bindungen](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="e6198-110">For details on creating string bindings, see [Using String Bindings](finding-server-host-systems.md).</span></span>

 

 