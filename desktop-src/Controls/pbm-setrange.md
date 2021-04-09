---
title: PBM_SETRANGE Meldung (kommstrg. h)
description: Legt den minimalen und maximalen Wert für eine Statusanzeige fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- Windows-Steuerelemente für PBM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859072"
---
# <a name="pbm_setrange-message"></a><span data-ttu-id="f5f59-104">PBM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="f5f59-104">PBM\_SETRANGE message</span></span>

<span data-ttu-id="f5f59-105">Legt den minimalen und maximalen Wert für eine Statusanzeige fest und zeichnet den Balken neu, um den neuen Bereich widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="f5f59-105">Sets the minimum and maximum values for a progress bar and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5f59-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5f59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f59-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5f59-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f59-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f5f59-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f5f59-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5f59-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f59-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den minimalen Bereichs Wert an, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den maximalen Bereichs Wert an.</span><span class="sxs-lookup"><span data-stu-id="f5f59-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum range value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum range value.</span></span> <span data-ttu-id="f5f59-111">Der minimale Bereichs Wert darf nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="f5f59-111">The minimum range value must not be negative.</span></span> <span data-ttu-id="f5f59-112">Standardmäßig ist der Minimalwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f5f59-112">By default, the minimum value is zero.</span></span> <span data-ttu-id="f5f59-113">Der maximale Bereichs Wert muss größer als der minimale Bereichs Wert sein.</span><span class="sxs-lookup"><span data-stu-id="f5f59-113">The maximum range value must be greater than the minimum range value.</span></span> <span data-ttu-id="f5f59-114">Der maximale Bereichs Wert ist standardmäßig 100.</span><span class="sxs-lookup"><span data-stu-id="f5f59-114">By default, the maximum range value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5f59-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5f59-115">Return value</span></span>

<span data-ttu-id="f5f59-116">Gibt die vorherigen Bereichs Werte zurück, wenn erfolgreich, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f5f59-116">Returns the previous range values if successful, or zero otherwise.</span></span> <span data-ttu-id="f5f59-117">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den vorherigen Minimalwert an, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den vorherigen maximalen Wert an.</span><span class="sxs-lookup"><span data-stu-id="f5f59-117">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the previous minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the previous maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f59-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5f59-118">Remarks</span></span>

<span data-ttu-id="f5f59-119">Wenn Sie die Bereichs Werte nicht festlegen, legt das System den Minimalwert auf 0 und den maximalen Wert auf 100 fest.</span><span class="sxs-lookup"><span data-stu-id="f5f59-119">If you do not set the range values, the system sets the minimum value to 0 and the maximum value to 100.</span></span> <span data-ttu-id="f5f59-120">Da diese Nachricht den Bereich als 16-Bit-Ganzzahl ohne Vorzeichen drückt, kann Sie von 0 bis 65.535 erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="f5f59-120">Because this message expresses the range as a 16-bit unsigned integer, it can extend from 0 to 65,535.</span></span> <span data-ttu-id="f5f59-121">Der Minimalwert im Bereich kann zwischen 0 und 65.535 liegen.</span><span class="sxs-lookup"><span data-stu-id="f5f59-121">The minimum value in the range can be from 0 to 65,535.</span></span> <span data-ttu-id="f5f59-122">Ebenso kann der Höchstwert zwischen 0 und 65.535 liegen.</span><span class="sxs-lookup"><span data-stu-id="f5f59-122">Likewise, the maximum value can be from 0 to 65,535.</span></span>

<span data-ttu-id="f5f59-123">Um einen größeren Bereich festzulegen, nennen Sie [**PBM \_ SETRANGE32**](pbm-setrange32.md).</span><span class="sxs-lookup"><span data-stu-id="f5f59-123">To set a larger range, call [**PBM\_SETRANGE32**](pbm-setrange32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f59-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5f59-124">Requirements</span></span>



| <span data-ttu-id="f5f59-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5f59-125">Requirement</span></span> | <span data-ttu-id="f5f59-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f5f59-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f59-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5f59-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f59-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5f59-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5f59-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5f59-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f59-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5f59-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5f59-131">Header</span><span class="sxs-lookup"><span data-stu-id="f5f59-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5f59-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5f59-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5f59-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5f59-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5f59-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f5f59-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f5f59-135">**PBM- \_ GetRange**</span><span class="sxs-lookup"><span data-stu-id="f5f59-135">**PBM\_GETRANGE**</span></span>](pbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="f5f59-136">**PBM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="f5f59-136">**PBM\_SETRANGE32**</span></span>](pbm-setrange32.md)
</dt> </dl>

 

