---
title: Bereinigung der Namensdienst Einträge
description: Ein Name-Dienst Eintrag sollte Informationen enthalten, die sich nicht häufig ändern.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037295"
---
# <a name="name-service-entry-cleanup"></a><span data-ttu-id="1483e-103">Bereinigung der Namensdienst Einträge</span><span class="sxs-lookup"><span data-stu-id="1483e-103">Name Service Entry Cleanup</span></span>

<span data-ttu-id="1483e-104">Ein Name-Dienst Eintrag sollte Informationen enthalten, die sich nicht häufig ändern.</span><span class="sxs-lookup"><span data-stu-id="1483e-104">A name service entry should contain information that does not change frequently.</span></span> <span data-ttu-id="1483e-105">Schließen Sie aus diesem Grund keine dynamischen Endpunkte in die exportierten Bindungs Handles ein, da Sie bei jedem Aufruf des Servers geändert werden und den Namen des Namens dienstantrags gruppieren.</span><span class="sxs-lookup"><span data-stu-id="1483e-105">For this reason, do not include dynamic endpoints in your exported binding handles because they will change at each invocation of the server and will clutter up your name service entry.</span></span> <span data-ttu-id="1483e-106">Um diese Bindungs Handles zu entfernen, verwenden Sie [**rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span><span class="sxs-lookup"><span data-stu-id="1483e-106">To remove these binding handles, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span></span>

<span data-ttu-id="1483e-107">Eine angemessene Sequenz von Server Vorgängen wäre z. b. wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1483e-107">For example, a reasonable sequence of server operations would be:</span></span>

<span data-ttu-id="1483e-108">Für mehr als einen Transport:</span><span class="sxs-lookup"><span data-stu-id="1483e-108">For more than one transport:</span></span>

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

<span data-ttu-id="1483e-109">So platzieren Sie Bindungen in der Endpunkt Zuordnung:</span><span class="sxs-lookup"><span data-stu-id="1483e-109">To place bindings in the endpoint mapper:</span></span>

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

<span data-ttu-id="1483e-110">So entfernen Sie Endpunkte aus Bindungen:</span><span class="sxs-lookup"><span data-stu-id="1483e-110">To remove endpoints from bindings:</span></span>

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

<span data-ttu-id="1483e-111">So fügen Sie Bindungen zum Namensdienst hinzu:</span><span class="sxs-lookup"><span data-stu-id="1483e-111">To add bindings to the name service:</span></span>

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




