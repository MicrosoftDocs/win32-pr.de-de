---
title: UDM_SETRANGE Meldung (kommstrg. h)
description: Legt die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement fest.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- Windows-Steuerelemente für UDM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040787"
---
# <a name="udm_setrange-message"></a><span data-ttu-id="ee54e-104">UDM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="ee54e-104">UDM\_SETRANGE message</span></span>

<span data-ttu-id="ee54e-105">Legt die minimalen und maximalen Positionen (Bereich) für ein auf-ab-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="ee54e-105">Sets the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee54e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee54e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee54e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee54e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ee54e-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ee54e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ee54e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee54e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee54e-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **kurzes** Element, das die maximale Position für das auf-ab-Steuerelement angibt, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **kurzes** Element, das die minimale Position angibt.</span><span class="sxs-lookup"><span data-stu-id="ee54e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **short** that specifies the maximum position for the up-down control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **short** that specifies the minimum position.</span></span> <span data-ttu-id="ee54e-111">Keine der Positionen kann größer als der UD \_ MaxVal-Wert oder kleiner als der UD \_ MinVal-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="ee54e-111">Neither position can be greater than the UD\_MAXVAL value or less than the UD\_MINVAL value.</span></span> <span data-ttu-id="ee54e-112">Außerdem darf der Unterschied zwischen den beiden Positionen UD MaxVal nicht überschreiten \_ .</span><span class="sxs-lookup"><span data-stu-id="ee54e-112">In addition, the difference between the two positions cannot exceed UD\_MAXVAL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee54e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee54e-113">Return value</span></span>

<span data-ttu-id="ee54e-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ee54e-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee54e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee54e-115">Remarks</span></span>

<span data-ttu-id="ee54e-116">Die maximale Position kann kleiner als die minimale Position sein.</span><span class="sxs-lookup"><span data-stu-id="ee54e-116">The maximum position can be less than the minimum position.</span></span> <span data-ttu-id="ee54e-117">Durch Klicken auf die Schaltfläche mit dem Pfeil nach oben wird die aktuelle Position näher an die maximale Position verschoben, und durch Klicken auf die nach-unten-Taste wird die minimale Position</span><span class="sxs-lookup"><span data-stu-id="ee54e-117">Clicking the up arrow button moves the current position closer to the maximum position, and clicking the down arrow button moves toward the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee54e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee54e-118">Requirements</span></span>



| <span data-ttu-id="ee54e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee54e-119">Requirement</span></span> | <span data-ttu-id="ee54e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ee54e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee54e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee54e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ee54e-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee54e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee54e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee54e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ee54e-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee54e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee54e-125">Header</span><span class="sxs-lookup"><span data-stu-id="ee54e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee54e-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee54e-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee54e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee54e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee54e-128">**Makelparam**</span><span class="sxs-lookup"><span data-stu-id="ee54e-128">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="ee54e-129">**UDM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="ee54e-129">**UDM\_SETRANGE**</span></span>](udm-setrange.md)
</dt> </dl>

 

