---
description: Testet die boundingfrustum-Schnittmenge mit einem anderen Objekt.
ms.assetid: b087761c-b298-4b64-86e7-60cd73543144
title: Boundingfrustum. intersekten-Methoden
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9eb0082fda21978fdf6371267e4cfa0bf531622b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754161"
---
# <a name="boundingfrustumintersects-methods"></a><span data-ttu-id="e8d1c-103">Boundingfrustum. intersekten-Methoden</span><span class="sxs-lookup"><span data-stu-id="e8d1c-103">BoundingFrustum.Intersects methods</span></span>

<span data-ttu-id="e8d1c-104">Testet die [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) -Schnittmenge mit einem anderen Objekt.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-104">Tests the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="e8d1c-105">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="e8d1c-105">Overload list</span></span>



| <span data-ttu-id="e8d1c-106">Methode</span><span class="sxs-lookup"><span data-stu-id="e8d1c-106">Method</span></span>                                                                                           | <span data-ttu-id="e8d1c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8d1c-107">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d1c-108">[**Boundingfrustum:: intersekten (xmvector)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="e8d1c-108">[**BoundingFrustum::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector))</span></span>                   | <span data-ttu-id="e8d1c-109">Testen Sie die [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) -Schnittmenge mit einer Ebene.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-109">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a plane.</span></span><br/>                                              |
| <span data-ttu-id="e8d1c-110">[**Boundingfrustum:: intersekten (const BoundingBox-&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="e8d1c-110">[**BoundingFrustum::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="e8d1c-111">Testen Sie die [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) -Schnittmenge mit einer [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox).</span><span class="sxs-lookup"><span data-stu-id="e8d1c-111">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox).</span></span><br/>                 |
| <span data-ttu-id="e8d1c-112">[**Boundingfrustum:: intersekten (const boundingsphere&)**](/previous-versions/windows/desktop/legacy/hh855929(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8d1c-112">[**BoundingFrustum::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh855929(v=vs.85))</span></span>      | <span data-ttu-id="e8d1c-113">Testen Sie die [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) -Schnittmenge mit einer [**boundingsphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere).</span><span class="sxs-lookup"><span data-stu-id="e8d1c-113">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingSphere**](/windows/win32/api/directxcollision/ns-directxcollision-boundingsphere).</span></span><br/>           |
| <span data-ttu-id="e8d1c-114">[**Boundingfrustum:: intersekten (const boundingfrustum-&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="e8d1c-114">[**BoundingFrustum::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="e8d1c-115">Testen Sie die [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) -Schnittmenge mit einer anderen **boundingfrustum**-Schnittmenge.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-115">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with another **BoundingFrustum**.</span></span><br/>                          |
| <span data-ttu-id="e8d1c-116">[**Boundingfrustum:: intersekten (xmvector, xmvector, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="e8d1c-116">[**BoundingFrustum::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="e8d1c-117">Testen Sie die [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) -Schnittmenge mit einem Strahl.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-117">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a ray.</span></span><br/>                                                |
| <span data-ttu-id="e8d1c-118">[**Boundingfrustum:: intersekten (xmvector, xmvector, xmvector)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="e8d1c-118">[**BoundingFrustum::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="e8d1c-119">Testen Sie die [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) -Schnittmenge mit einem Dreieck.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-119">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a triangle.</span></span><br/>                                           |
| <span data-ttu-id="e8d1c-120">[**Boundingfrustum:: intersekten (const boundingorientedbox-&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="e8d1c-120">[**BoundingFrustum::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingfrustum-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="e8d1c-121">Testen Sie die [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) -Schnittmenge mit einer [**boundingorientedbox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span><span class="sxs-lookup"><span data-stu-id="e8d1c-121">Test the [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8d1c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8d1c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8d1c-123">Methoden</span><span class="sxs-lookup"><span data-stu-id="e8d1c-123">Methods</span></span>](boundingfrustum-methods.md)
</dt> <dt>

<span data-ttu-id="e8d1c-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e8d1c-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e8d1c-125">**Boundingfrustum**</span><span class="sxs-lookup"><span data-stu-id="e8d1c-125">**BoundingFrustum**</span></span>](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)
</dt> </dl>

 

 
