---
description: RPC-NDR-Engine
ms.assetid: FD6365A9-6EC2-407D-B397-09A91BF02379
title: RPC-NDR-Engine (Entwickler Hinweise)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39eeb38d99e01dd8ab5683cf0289b3e7e09d45f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344824"
---
# <a name="rpc-ndr-engine-developer-notes"></a><span data-ttu-id="cacba-103">RPC-NDR-Engine (Entwickler Hinweise)</span><span class="sxs-lookup"><span data-stu-id="cacba-103">RPC NDR Engine (Developer Notes)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cacba-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cacba-104">In this section</span></span>

-   [<span data-ttu-id="cacba-105">**Ndrcomplexarraybuffersize**</span><span class="sxs-lookup"><span data-stu-id="cacba-105">**NdrComplexArrayBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarraybuffersize)
-   [<span data-ttu-id="cacba-106">**Ndrcomplexarraymarshall**</span><span class="sxs-lookup"><span data-stu-id="cacba-106">**NdrComplexArrayMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarraymarshall)
-   [<span data-ttu-id="cacba-107">**Ndrcomplexarrayunmarshall**</span><span class="sxs-lookup"><span data-stu-id="cacba-107">**NdrComplexArrayUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarrayunmarshall)
-   [<span data-ttu-id="cacba-108">**Ndrcomplexstructbuffersize**</span><span class="sxs-lookup"><span data-stu-id="cacba-108">**NdrComplexStructBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructbuffersize)
-   [<span data-ttu-id="cacba-109">**Ndrcomplexstructmarshall**</span><span class="sxs-lookup"><span data-stu-id="cacba-109">**NdrComplexStructMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructmarshall)
-   [<span data-ttu-id="cacba-110">**Ndrcomplexstructunmarshall**</span><span class="sxs-lookup"><span data-stu-id="cacba-110">**NdrComplexStructUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructunmarshall)
-   [<span data-ttu-id="cacba-111">**Ndrgetrmantarraybuffersize**</span><span class="sxs-lookup"><span data-stu-id="cacba-111">**NdrComformantArrayBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarraybuffersize)
-   [<span data-ttu-id="cacba-112">**Ndrgetrmantarraymarshall**</span><span class="sxs-lookup"><span data-stu-id="cacba-112">**NdrComformantArrayMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarraymarshall)
-   [<span data-ttu-id="cacba-113">**Ndrsimplestructbuffersize**</span><span class="sxs-lookup"><span data-stu-id="cacba-113">**NdrSimpleStructBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructbuffersize)
-   [<span data-ttu-id="cacba-114">**Ndrsimplestructmarshall**</span><span class="sxs-lookup"><span data-stu-id="cacba-114">**NdrSimpleStructMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructmarshall)
-   [<span data-ttu-id="cacba-115">**Ndrsimplestructunmarshall**</span><span class="sxs-lookup"><span data-stu-id="cacba-115">**NdrSimpleStructUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructunmarshall)
-   [<span data-ttu-id="cacba-116">**Ndrusermarshalunmarshall**</span><span class="sxs-lookup"><span data-stu-id="cacba-116">**NdrUserMarshalUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalunmarshall)

 

 



