---
description: Testet das BoundingBox-Objekt auf eine Überschneidung mit einem anderen Objekt.
ms.assetid: df3d3df9-aa74-413d-808c-f7b276d11279
title: BoundingBox. intersekten-Methoden
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9039d99640ae3989d0b20e9d48f681edabb021f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528115"
---
# <a name="boundingboxintersects-methods"></a><span data-ttu-id="2cbb4-103">BoundingBox. intersekten-Methoden</span><span class="sxs-lookup"><span data-stu-id="2cbb4-103">BoundingBox.Intersects methods</span></span>

<span data-ttu-id="2cbb4-104">Testet das BoundingBox-Objekt auf eine Überschneidung mit einem anderen Objekt.</span><span class="sxs-lookup"><span data-stu-id="2cbb4-104">Tests the BoundingBox for intersection with another object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2cbb4-105">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="2cbb4-105">Overload list</span></span>



| <span data-ttu-id="2cbb4-106">Methode</span><span class="sxs-lookup"><span data-stu-id="2cbb4-106">Method</span></span>                                                                                   | <span data-ttu-id="2cbb4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cbb4-107">Description</span></span>                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbb4-108">[**BoundingBox:: intersekten (xmvector)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span><span class="sxs-lookup"><span data-stu-id="2cbb4-108">[**BoundingBox::Intersects (XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector))</span></span>                   | <span data-ttu-id="2cbb4-109">Testen Sie die BoundingBox für Schnittmenge mit einer Ebene.</span><span class="sxs-lookup"><span data-stu-id="2cbb4-109">Test the BoundingBox for intersection with a plane.</span></span><br/>                                                                     |
| <span data-ttu-id="2cbb4-110">[**BoundingBox:: Schnittpunkte (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span><span class="sxs-lookup"><span data-stu-id="2cbb4-110">[**BoundingBox::Intersects (const BoundingBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingbox_))</span></span>         | <span data-ttu-id="2cbb4-111">Testet die BoundingBox auf Schnittmenge mit einer anderen BoundingBox.</span><span class="sxs-lookup"><span data-stu-id="2cbb4-111">Tests the BoundingBox for intersection with another BoundingBox.</span></span><br/>                                                        |
| <span data-ttu-id="2cbb4-112">[**BoundingBox:: intersekten (const boundingsphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2cbb4-112">[**BoundingBox::Intersects (const BoundingSphere&)**](/previous-versions/windows/desktop/legacy/hh437825(v=vs.85))</span></span>      | <span data-ttu-id="2cbb4-113">Testet die BoundingBox auf Schnittmenge mit einer boundingsphere.</span><span class="sxs-lookup"><span data-stu-id="2cbb4-113">Tests the BoundingBox for intersection with a BoundingSphere.</span></span><br/>                                                           |
| <span data-ttu-id="2cbb4-114">[**BoundingBox:: intersekten (const boundingfrustum-&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span><span class="sxs-lookup"><span data-stu-id="2cbb4-114">[**BoundingBox::Intersects (const BoundingFrustum&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingfrustum_))</span></span>     | <span data-ttu-id="2cbb4-115">Testen Sie die [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) für Schnittmenge mit einem [**boundingfrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span><span class="sxs-lookup"><span data-stu-id="2cbb4-115">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingFrustum**](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).</span></span><br/>         |
| <span data-ttu-id="2cbb4-116">[**BoundingBox:: intersekten (xmvector, xmvector, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span><span class="sxs-lookup"><span data-stu-id="2cbb4-116">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))</span></span>   | <span data-ttu-id="2cbb4-117">Testen Sie die BoundingBox für Schnittmenge mit einem Strahl.</span><span class="sxs-lookup"><span data-stu-id="2cbb4-117">Test the BoundingBox for intersection with a ray.</span></span><br/>                                                                       |
| <span data-ttu-id="2cbb4-118">[**BoundingBox:: intersekten (xmvector, xmvector, xmvector)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span><span class="sxs-lookup"><span data-stu-id="2cbb4-118">[**BoundingBox::Intersects (XMVECTOR,XMVECTOR,XMVECTOR)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_fxmvector))</span></span> | <span data-ttu-id="2cbb4-119">Testen Sie die BoundingBox für Schnittmenge mit einem Dreieck.</span><span class="sxs-lookup"><span data-stu-id="2cbb4-119">Test the BoundingBox for intersection with a triangle.</span></span><br/>                                                                  |
| <span data-ttu-id="2cbb4-120">[**BoundingBox:: intersekten (const boundingorientedbox-&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span><span class="sxs-lookup"><span data-stu-id="2cbb4-120">[**BoundingBox::Intersects (const BoundingOrientedBox&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(constboundingorientedbox_))</span></span> | <span data-ttu-id="2cbb4-121">Testen Sie die [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) -Schnittstelle mit einer [**boundingorientedbox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span><span class="sxs-lookup"><span data-stu-id="2cbb4-121">Test the [**BoundingBox**](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox) for intersection with a [**BoundingOrientedBox**](/windows/win32/api/directxcollision/ns-directxcollision-boundingorientedbox).</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cbb4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cbb4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbb4-123">Methoden</span><span class="sxs-lookup"><span data-stu-id="2cbb4-123">Methods</span></span>](boundingbox-methods.md)
</dt> <dt>

<span data-ttu-id="2cbb4-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2cbb4-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2cbb4-125">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="2cbb4-125">**BoundingBox**</span></span>](/windows/desktop/api/DirectXCollision/ns-directxcollision-boundingbox)
</dt> </dl>

 

 
