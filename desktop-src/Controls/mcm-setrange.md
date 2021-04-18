---
title: MCM_SETRANGE Meldung (kommstrg. h)
description: Legt das minimal-und maximal zulässige Datum für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem monthcal-- \_ Makro senden.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- Windows-Steuerelemente für MCM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344490"
---
# <a name="mcm_setrange-message"></a><span data-ttu-id="d3f9c-105">MCM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="d3f9c-105">MCM\_SETRANGE message</span></span>

<span data-ttu-id="d3f9c-106">Legt das minimal-und maximal zulässige Datum für ein Monatskalender-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-106">Sets the minimum and maximum allowable dates for a month calendar control.</span></span> <span data-ttu-id="d3f9c-107">Sie können diese Nachricht explizit oder mit dem [**monthcal \_**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) --Makro senden.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-107">You can send this message explicitly or by using the [**MonthCal\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3f9c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3f9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3f9c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3f9c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3f9c-110">Flagwerte, die angeben, welche Datums Limits festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-110">Flag values that specify which date limits are being set.</span></span> <span data-ttu-id="d3f9c-111">Dieser Wert muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="d3f9c-111">This value must be one or both of the following:</span></span>



| <span data-ttu-id="d3f9c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d3f9c-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="d3f9c-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d3f9c-113">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="d3f9c-114"><dt>**maximal zulässige dstr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d3f9c-114"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="d3f9c-115">Das maximal zulässige Datum wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-115">The maximum allowable date is being set.</span></span> <span data-ttu-id="d3f9c-116">Die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur bei *lpsystimearray* \[ 1 \] muss Datumsinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-116">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[1\] must contain date information.</span></span> <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="d3f9c-117"><dt>**dstr \_ Min.**</dt></span><span class="sxs-lookup"><span data-stu-id="d3f9c-117"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="d3f9c-118">Das minimal zulässige Datum wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-118">The minimum allowable date is being set.</span></span> <span data-ttu-id="d3f9c-119">Die [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur bei *lpsystimearray* \[ 0 \] muss Datumsinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-119">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[0\] must contain date information.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="d3f9c-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3f9c-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3f9c-121">Ein Zeiger auf ein Array aus zwei Elementen von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, die die Datums Limits enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-121">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain the date limits.</span></span> <span data-ttu-id="d3f9c-122">Der maximale Grenzwert muss in *lpsystimearray* \[ 1 liegen \] , wenn dstr \_ Max angegeben ist, und *lpsystimearray* \[ 0 \] muss das minimale Limit enthalten, wenn dstr \_ Min angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-122">The maximum limit must be in *lpSysTimeArray*\[1\] if GDTR\_MAX is specified, and *lpSysTimeArray*\[0\] must contain the minimum limit if GDTR\_MIN is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3f9c-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3f9c-123">Return value</span></span>

<span data-ttu-id="d3f9c-124">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="d3f9c-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f9c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3f9c-125">Requirements</span></span>



| <span data-ttu-id="d3f9c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3f9c-126">Requirement</span></span> | <span data-ttu-id="d3f9c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d3f9c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f9c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3f9c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f9c-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3f9c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3f9c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3f9c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f9c-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3f9c-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3f9c-132">Header</span><span class="sxs-lookup"><span data-stu-id="d3f9c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3f9c-133"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3f9c-133"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f9c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3f9c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f9c-135">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d3f9c-135">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

