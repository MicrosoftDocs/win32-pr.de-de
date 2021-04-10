---
title: Stift Maske
description: Werte, die im Feld "Straf Maske" der POINTER_PEN_INFO Struktur angezeigt werden können.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bd181b5eafbe1cf6de56c95886deb04e5bd6d2b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104564"
---
# <a name="pen-mask"></a><span data-ttu-id="813a3-103">Stift Maske</span><span class="sxs-lookup"><span data-stu-id="813a3-103">Pen Mask</span></span>

<span data-ttu-id="813a3-104">Werte, die im Feld " **Straf Maske** " der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="813a3-104">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="813a3-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="813a3-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="813a3-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="813a3-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="813a3-107">Standard.</span><span class="sxs-lookup"><span data-stu-id="813a3-107">Default.</span></span> <span data-ttu-id="813a3-108">Keines der optionalen Felder ist gültig.</span><span class="sxs-lookup"><span data-stu-id="813a3-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="813a3-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="813a3-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="813a3-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="813a3-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="813a3-111">der **Druck** der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) Struktur ist gültig.</span><span class="sxs-lookup"><span data-stu-id="813a3-111">**pressure** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="813a3-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span><span class="sxs-lookup"><span data-stu-id="813a3-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="813a3-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="813a3-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="813a3-114">die **Drehung** der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) Struktur ist gültig.</span><span class="sxs-lookup"><span data-stu-id="813a3-114">**rotation** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="813a3-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span><span class="sxs-lookup"><span data-stu-id="813a3-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="813a3-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="813a3-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="813a3-117">der **TiltX** -Wert der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) -Struktur ist gültig.</span><span class="sxs-lookup"><span data-stu-id="813a3-117">**tiltX** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="813a3-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span><span class="sxs-lookup"><span data-stu-id="813a3-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="813a3-119">0x00000008</span><span class="sxs-lookup"><span data-stu-id="813a3-119">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="813a3-120">die **TiltY** der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) Struktur ist gültig.</span><span class="sxs-lookup"><span data-stu-id="813a3-120">**tiltY** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="813a3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="813a3-121">Requirements</span></span>



| <span data-ttu-id="813a3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="813a3-122">Requirement</span></span> | <span data-ttu-id="813a3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="813a3-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="813a3-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="813a3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="813a3-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="813a3-125">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="813a3-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="813a3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="813a3-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="813a3-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="813a3-128">Header</span><span class="sxs-lookup"><span data-stu-id="813a3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="813a3-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="813a3-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="813a3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="813a3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="813a3-131">Konstanten</span><span class="sxs-lookup"><span data-stu-id="813a3-131">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="813a3-132">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="813a3-132">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





