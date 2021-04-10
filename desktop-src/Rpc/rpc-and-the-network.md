---
title: RPC und das Netzwerk
description: In diesem Abschnitt wird erläutert, wie die Netzwerk Zuverlässigkeit bei Verwendung von RPC behandelt wird, und es wird erläutert, wie APIs auf RPC-Ebene in eine Netzwerkaktivität übersetzt werden. Der Abschnitt bezieht sich nur auf die \_ http-Protokoll Sequenzen ncacn IP \_ TCP und ncacn \_ .
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, RPC und das Netzwerk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102095"
---
# <a name="rpc-and-the-network"></a><span data-ttu-id="dba14-105">RPC und das Netzwerk</span><span class="sxs-lookup"><span data-stu-id="dba14-105">RPC and the Network</span></span>

<span data-ttu-id="dba14-106">In diesem Abschnitt wird erläutert, wie die Netzwerk Zuverlässigkeit bei Verwendung von RPC behandelt wird, und es wird erläutert, wie APIs auf RPC-Ebene in eine Netzwerkaktivität übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="dba14-106">This section discusses how to deal with network unreliability when using RPC, and explains how RPC-level APIs translate into network activity.</span></span> <span data-ttu-id="dba14-107">Der Abschnitt bezieht sich nur auf die HTTP-Protokoll Sequenzen [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) und [**ncacn \_**](/windows/desktop/Midl/ncacn-http) .</span><span class="sxs-lookup"><span data-stu-id="dba14-107">The section refers only to the [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) and [**ncacn\_http**](/windows/desktop/Midl/ncacn-http) protocol sequences.</span></span>

<span data-ttu-id="dba14-108">Dieser Abschnitt ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="dba14-108">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="dba14-109">Entwicklung und Bereitstellung im Netzwerk</span><span class="sxs-lookup"><span data-stu-id="dba14-109">Development Versus Deployment in the Network</span></span>](development-versus-deployment-in-the-network.md)
-   [<span data-ttu-id="dba14-110">Verhindern von Client-Side hängen</span><span class="sxs-lookup"><span data-stu-id="dba14-110">Preventing Client-Side Hangs</span></span>](preventing-client-side-hangs.md)
-   [<span data-ttu-id="dba14-111">Verwalten von Netzwerk Verbindungs Sätzen (Zuordnungen)</span><span class="sxs-lookup"><span data-stu-id="dba14-111">Managing Network Connection Sets (Associations)</span></span>](managing-network-connection-sets-associations-.md)
-   [<span data-ttu-id="dba14-112">Cleanup für Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="dba14-112">Idle Connection Cleanup</span></span>](idle-connection-cleanup.md)
-   [<span data-ttu-id="dba14-113">Umgang mit Verbindungsverlust</span><span class="sxs-lookup"><span data-stu-id="dba14-113">Dealing with Loss of Connectivity</span></span>](dealing-with-loss-of-connectivity.md)
-   [<span data-ttu-id="dba14-114">Server seitiges Cleanup</span><span class="sxs-lookup"><span data-stu-id="dba14-114">Server Side Cleanup</span></span>](server-side-cleanup.md)

 

 