---
title: Berührungs Maske
description: Werte, die im Feld touchmask der POINTER_TOUCH_INFO Struktur angezeigt werden können.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478753"
---
# <a name="touch-mask"></a><span data-ttu-id="e85ac-103">Berührungs Maske</span><span class="sxs-lookup"><span data-stu-id="e85ac-103">Touch Mask</span></span>

<span data-ttu-id="e85ac-104">Werte, die im Feld **touchmask** der [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="e85ac-104">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="e85ac-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="e85ac-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e85ac-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e85ac-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="e85ac-107">Standard.</span><span class="sxs-lookup"><span data-stu-id="e85ac-107">Default.</span></span> <span data-ttu-id="e85ac-108">Keines der optionalen Felder ist gültig.</span><span class="sxs-lookup"><span data-stu-id="e85ac-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e85ac-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span><span class="sxs-lookup"><span data-stu-id="e85ac-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e85ac-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e85ac-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="e85ac-111">**rccontact** der [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) Struktur ist gültig.</span><span class="sxs-lookup"><span data-stu-id="e85ac-111">**rcContact** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e85ac-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span><span class="sxs-lookup"><span data-stu-id="e85ac-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e85ac-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e85ac-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="e85ac-114">die **Ausrichtung** der [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) Struktur ist gültig.</span><span class="sxs-lookup"><span data-stu-id="e85ac-114">**orientation** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e85ac-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="e85ac-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e85ac-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e85ac-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="e85ac-117">der **Druck** der [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) Struktur ist gültig.</span><span class="sxs-lookup"><span data-stu-id="e85ac-117">**pressure** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e85ac-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e85ac-118">Requirements</span></span>



| <span data-ttu-id="e85ac-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e85ac-119">Requirement</span></span> | <span data-ttu-id="e85ac-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e85ac-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e85ac-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e85ac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e85ac-122">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e85ac-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e85ac-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e85ac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e85ac-124">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e85ac-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e85ac-125">Header</span><span class="sxs-lookup"><span data-stu-id="e85ac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e85ac-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e85ac-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e85ac-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e85ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85ac-128">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e85ac-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="e85ac-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="e85ac-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





