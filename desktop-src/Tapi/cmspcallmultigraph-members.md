---
description: Cmspcallmultigraph-Member
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Cmspcallmultigraph-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360571"
---
# <a name="cmspcallmultigraph-members"></a><span data-ttu-id="72d51-103">Cmspcallmultigraph-Member</span><span class="sxs-lookup"><span data-stu-id="72d51-103">CMSPCallMultiGraph Members</span></span>

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

<span data-ttu-id="72d51-104">Die Warte Blöcke speichern die Informationen über die Wartezeit, die im Thread Pool registriert ist.</span><span class="sxs-lookup"><span data-stu-id="72d51-104">The wait blocks store the information about the wait registered to the thread pool.</span></span> <span data-ttu-id="72d51-105">Sie enthält die vom [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) -Befehl zurückgegebenen Wait-Handles und einen Zeiger auf die Kontext Struktur.</span><span class="sxs-lookup"><span data-stu-id="72d51-105">It includes the wait handles returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) call and a pointer to the context structure.</span></span> <span data-ttu-id="72d51-106">Jeder Block im Array ist für ein Diagramm in einem der Streamobjekte.</span><span class="sxs-lookup"><span data-stu-id="72d51-106">Each block in the array is for a graph in one of the stream objects.</span></span> <span data-ttu-id="72d51-107">Der Offset eines Blocks in diesem Array entspricht dem Offset des Streams, der das Diagramm besitzt.</span><span class="sxs-lookup"><span data-stu-id="72d51-107">The offset of a block in this array is the same as the offset of the stream that owns the graph.</span></span>

 

 
