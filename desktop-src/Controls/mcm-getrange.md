---
title: MCM_GETRANGE Meldung (kommstrg. h)
description: Ruft die minimalen und maximalen zulässigen Datumsangaben für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mit dem monthcal- \_ GetRange-Makro senden.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- Windows-Steuerelemente für MCM_GETRANGE Meldung
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859251"
---
# <a name="mcm_getrange-message"></a><span data-ttu-id="391c3-105">MCM- \_ GetRange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="391c3-105">MCM\_GETRANGE message</span></span>

<span data-ttu-id="391c3-106">Ruft die minimalen und maximalen zulässigen Datumsangaben für ein Monatskalender-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="391c3-106">Retrieves the minimum and maximum allowable dates set for a month calendar control.</span></span> <span data-ttu-id="391c3-107">Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="391c3-107">You can send this message explicitly or by using the [**MonthCal\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="391c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="391c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391c3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="391c3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="391c3-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="391c3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="391c3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="391c3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="391c3-112">Ein Zeiger auf ein Array aus zwei Elementen von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, die die Datums Limit-Informationen empfangen.</span><span class="sxs-lookup"><span data-stu-id="391c3-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the date limit information.</span></span> <span data-ttu-id="391c3-113">Die minimale Grenze wird in *lprgsystimearray* \[ 0 festgelegt \] , und *lprgsystimearray* \[ 1 \] erhält die maximale Grenze.</span><span class="sxs-lookup"><span data-stu-id="391c3-113">The minimum limit is set in *lprgSysTimeArray*\[0\], and *lprgSysTimeArray*\[1\] receives the maximum limit.</span></span> <span data-ttu-id="391c3-114">Wenn eines der beiden Elemente auf Nullen festgelegt ist, wird kein entsprechendes Limit für das Monatskalender-Steuerelement festgelegt.</span><span class="sxs-lookup"><span data-stu-id="391c3-114">If either element is set to all zeros, then no corresponding limit is set for the month calendar control.</span></span> <span data-ttu-id="391c3-115">Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="391c3-115">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391c3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="391c3-116">Return value</span></span>

<span data-ttu-id="391c3-117">Gibt ein **DWORD** zurück, das 0 (null) (keine Limits) oder eine Kombination der folgenden Werte sein kann, die Grenz Informationen angeben:</span><span class="sxs-lookup"><span data-stu-id="391c3-117">Returns a **DWORD** that can be zero (no limits are set) or a combination of the following values that specify limit information:</span></span>



| <span data-ttu-id="391c3-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="391c3-118">Return code</span></span>                                                                              | <span data-ttu-id="391c3-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="391c3-119">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="391c3-120"><dt>**maximal zulässige dstr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="391c3-120"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="391c3-121">Für das Steuerelement ist eine Obergrenze festgelegt. *lprgsystimearray* \[ 0 \] ist gültig und enthält die anwendbaren Datumsinformationen.</span><span class="sxs-lookup"><span data-stu-id="391c3-121">A maximum limit is set for the control; *lprgSysTimeArray*\[0\] is valid and contains the applicable date information.</span></span> <br/> |
| <dl> <span data-ttu-id="391c3-122"><dt>**dstr \_ Min.**</dt></span><span class="sxs-lookup"><span data-stu-id="391c3-122"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="391c3-123">Für das Steuerelement ist ein minimal Grenzwert festgelegt. *lprgsystimearray* \[ 1 \] ist gültig und enthält die anwendbaren Datumsinformationen.</span><span class="sxs-lookup"><span data-stu-id="391c3-123">A minimum limit is set for the control; *lprgSysTimeArray*\[1\] is valid and contains the applicable date information.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="391c3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="391c3-124">Requirements</span></span>



| <span data-ttu-id="391c3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="391c3-125">Requirement</span></span> | <span data-ttu-id="391c3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="391c3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="391c3-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="391c3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="391c3-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="391c3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="391c3-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="391c3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="391c3-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="391c3-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="391c3-131">Header</span><span class="sxs-lookup"><span data-stu-id="391c3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="391c3-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="391c3-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="391c3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="391c3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391c3-134">Uhrzeiten im Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="391c3-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

