---
title: D2D1_POINT_2F (D2DBaseTypes. h)
description: Stellt ein x-Koordinate-und ein y-Koordinaten Paar im zweidimensionalen Raum dar. | D2D1_POINT_2F (D2DBaseTypes. h)
ms.assetid: b317ae75-d738-4e1a-bcd1-adf3e95b197e
keywords:
- D2D1_POINT_2F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f93bf4a0d1a1b3f988f1c6d168388e9910080dcb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361812"
---
# <a name="d2d1_point_2f"></a><span data-ttu-id="d4c46-105">D2D1 \_ Punkt \_ 2F</span><span class="sxs-lookup"><span data-stu-id="d4c46-105">D2D1\_POINT\_2F</span></span>

<span data-ttu-id="d4c46-106">Stellt ein x-Koordinate-und ein y-Koordinaten Paar im zweidimensionalen Raum dar.</span><span class="sxs-lookup"><span data-stu-id="d4c46-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2F D2D1_POINT_2F;
```



## <a name="remarks"></a><span data-ttu-id="d4c46-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4c46-107">Remarks</span></span>

<span data-ttu-id="d4c46-108">Punkte in Direct2D werden durch die **D2D1 \_ Point \_ 2F** -oder [**D2D1 \_ Point \_ 2U**](d2d1-point-2u.md) -Strukturen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d4c46-108">Points in Direct2D are represented by the **D2D1\_POINT\_2F** or [**D2D1\_POINT\_2U**](d2d1-point-2u.md) structures.</span></span> <span data-ttu-id="d4c46-109">Beide enthalten ein x-Koordinate-und ein y-Koordinaten Paar im zweidimensionalen Raum.</span><span class="sxs-lookup"><span data-stu-id="d4c46-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="d4c46-110">Die **D2D1 \_ Point \_ 2F** -Struktur speichert die Koordinaten als **float** -Werte, und die **D2D1 \_ Point \_ 2U** -Struktur speichert Sie als **UInt32** -Werte.</span><span class="sxs-lookup"><span data-stu-id="d4c46-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="d4c46-111">**D2D1 \_ Punkt \_ 2F** ist ein neuer Name für den bereits definierten Typ [**D2D \_ Point \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span><span class="sxs-lookup"><span data-stu-id="d4c46-111">**D2D1\_POINT\_2F** is a new name for the already defined type [**D2D\_POINT\_2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c46-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4c46-112">Requirements</span></span>



| <span data-ttu-id="d4c46-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4c46-113">Requirement</span></span> | <span data-ttu-id="d4c46-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d4c46-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c46-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4c46-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c46-116">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4c46-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d4c46-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4c46-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c46-118">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4c46-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d4c46-119">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="d4c46-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d4c46-120">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="d4c46-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="d4c46-121">Header</span><span class="sxs-lookup"><span data-stu-id="d4c46-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4c46-122"><dt>D2DBaseTypes. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4c46-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d4c46-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4c46-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c46-124">**D2D1 \_ Punkt \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="d4c46-124">**D2D1\_POINT\_2U**</span></span>](/windows/desktop/Direct2D/d2d1-point-2u)
</dt> <dt>

[<span data-ttu-id="d4c46-125">**D2D \_ Punkt \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="d4c46-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

