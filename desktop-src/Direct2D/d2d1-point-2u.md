---
title: D2D1_POINT_2U (D2DBaseTypes. h)
description: Stellt ein x-Koordinate-und ein y-Koordinaten Paar im zweidimensionalen Raum dar. | D2D1_POINT_2U (D2DBaseTypes. h)
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219240"
---
# <a name="d2d1_point_2u"></a><span data-ttu-id="d69a9-105">D2D1 \_ Punkt \_ 2U</span><span class="sxs-lookup"><span data-stu-id="d69a9-105">D2D1\_POINT\_2U</span></span>

<span data-ttu-id="d69a9-106">Stellt ein x-Koordinate-und ein y-Koordinaten Paar im zweidimensionalen Raum dar.</span><span class="sxs-lookup"><span data-stu-id="d69a9-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a><span data-ttu-id="d69a9-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d69a9-107">Remarks</span></span>

<span data-ttu-id="d69a9-108">Punkte in Direct2D werden durch die [**D2D1 \_ Point \_ 2F**](d2d1-point-2f.md) -oder **D2D1 \_ Point \_ 2U** -Strukturen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d69a9-108">Points in Direct2D are represented by the [**D2D1\_POINT\_2F**](d2d1-point-2f.md) or **D2D1\_POINT\_2U** structures.</span></span> <span data-ttu-id="d69a9-109">Beide enthalten ein x-Koordinate-und ein y-Koordinaten Paar im zweidimensionalen Raum.</span><span class="sxs-lookup"><span data-stu-id="d69a9-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="d69a9-110">Die **D2D1 \_ Point \_ 2F** -Struktur speichert die Koordinaten als **float** -Werte, und die **D2D1 \_ Point \_ 2U** -Struktur speichert Sie als **UInt32** -Werte.</span><span class="sxs-lookup"><span data-stu-id="d69a9-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="d69a9-111">**D2D1 \_ Punkt \_ 2U** ist ein neuer Name für den bereits definierten Typ [**D2D \_ Punkt \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span><span class="sxs-lookup"><span data-stu-id="d69a9-111">**D2D1\_POINT\_2U** is a new name for the already defined type [**D2D\_POINT\_2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span></span>

## <a name="requirements"></a><span data-ttu-id="d69a9-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d69a9-112">Requirements</span></span>



| <span data-ttu-id="d69a9-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d69a9-113">Requirement</span></span> | <span data-ttu-id="d69a9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d69a9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69a9-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d69a9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d69a9-116">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d69a9-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d69a9-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d69a9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d69a9-118">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d69a9-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d69a9-119">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="d69a9-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d69a9-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="d69a9-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="d69a9-121">Header</span><span class="sxs-lookup"><span data-stu-id="d69a9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d69a9-122"><dt>D2DBaseTypes. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d69a9-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d69a9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d69a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69a9-124">**D2D \_ Punkt \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="d69a9-124">**D2D\_POINT\_2U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[<span data-ttu-id="d69a9-125">**D2D \_ Punkt \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="d69a9-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





