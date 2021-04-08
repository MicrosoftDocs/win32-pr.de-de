---
title: EM_SETPAGEROTATE Meldung (RichEdit. h)
description: Legt das Text Layout für ein Rich-Edit-Steuerelement fest.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- Windows-Steuerelemente für EM_SETPAGEROTATE Meldung
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949777"
---
# <a name="em_setpagerotate-message"></a><span data-ttu-id="00186-104">EM \_ SETPAGEROTATE Meldung</span><span class="sxs-lookup"><span data-stu-id="00186-104">EM\_SETPAGEROTATE message</span></span>

<span data-ttu-id="00186-105">\[**EM \_ SETPAGEROTATE** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="00186-105">\[**EM\_SETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00186-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="00186-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="00186-107">Legt das Text Layout für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="00186-107">Sets the text layout for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="00186-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="00186-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00186-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00186-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00186-110">Textlayoutwert.</span><span class="sxs-lookup"><span data-stu-id="00186-110">Text layout value.</span></span> <span data-ttu-id="00186-111">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="00186-111">This can be one of the following values.</span></span>



| <span data-ttu-id="00186-112">Wert</span><span class="sxs-lookup"><span data-stu-id="00186-112">Value</span></span>                                                                                                                                       | <span data-ttu-id="00186-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="00186-113">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <span data-ttu-id="00186-114"><dt>**EPR \_ 0**</dt></span><span class="sxs-lookup"><span data-stu-id="00186-114"><dt>**EPR\_0**</dt></span></span> </dl>       | <span data-ttu-id="00186-115">Der Text fließt von links nach rechts und von oben nach unten.</span><span class="sxs-lookup"><span data-stu-id="00186-115">Text flows from left to right and from top to bottom.</span></span><br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <span data-ttu-id="00186-116"><dt>**EPR \_ 90**</dt></span><span class="sxs-lookup"><span data-stu-id="00186-116"><dt>**EPR\_90**</dt></span></span> </dl>    | <span data-ttu-id="00186-117">Der Text fließt von unten nach oben und von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="00186-117">Text flows from bottom to top and from left to right.</span></span><br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <span data-ttu-id="00186-118"><dt>**EPR \_ 180**</dt></span><span class="sxs-lookup"><span data-stu-id="00186-118"><dt>**EPR\_180**</dt></span></span> </dl> | <span data-ttu-id="00186-119">Der Text fließt von rechts nach links und von unten nach oben.</span><span class="sxs-lookup"><span data-stu-id="00186-119">Text flows from right to left and from bottom to top.</span></span><br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <span data-ttu-id="00186-120"><dt>**EPR \_ 270**</dt></span><span class="sxs-lookup"><span data-stu-id="00186-120"><dt>**EPR\_270**</dt></span></span> </dl> | <span data-ttu-id="00186-121">Der Text fließt von oben nach unten und von rechts nach links.</span><span class="sxs-lookup"><span data-stu-id="00186-121">Text flows from top to bottom and from right to left.</span></span><br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <span data-ttu-id="00186-122"><dt>**EPR \_ SE**</dt></span><span class="sxs-lookup"><span data-stu-id="00186-122"><dt>**EPR\_SE**</dt></span></span> </dl>    | <span data-ttu-id="00186-123">**Windows 8:** Text fließt von oben nach unten und von links nach rechts (Mongolisches Text Layout).</span><span class="sxs-lookup"><span data-stu-id="00186-123">**Windows 8:** Text flows top to bottom and left to right (Mongolian text layout).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="00186-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00186-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00186-125">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="00186-125">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00186-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00186-126">Return value</span></span>

<span data-ttu-id="00186-127">Der Rückgabewert ist der neue textlayoutwert.</span><span class="sxs-lookup"><span data-stu-id="00186-127">Return value is the new text layout value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00186-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00186-128">Remarks</span></span>

<span data-ttu-id="00186-129">Mit dieser Meldung wird das Text Layout für das gesamte Dokument festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00186-129">This message sets the text layout for the entire document.</span></span> <span data-ttu-id="00186-130">Eingebettete Inhalte werden jedoch nicht gedreht und müssen separat von der Anwendung gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="00186-130">However, embedded contents are not rotated and must be rotated separately by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="00186-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00186-131">Requirements</span></span>



| <span data-ttu-id="00186-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00186-132">Requirement</span></span> | <span data-ttu-id="00186-133">Wert</span><span class="sxs-lookup"><span data-stu-id="00186-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00186-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00186-134">Minimum supported client</span></span><br/> | <span data-ttu-id="00186-135">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00186-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00186-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00186-136">Minimum supported server</span></span><br/> | <span data-ttu-id="00186-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00186-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00186-138">Header</span><span class="sxs-lookup"><span data-stu-id="00186-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="00186-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="00186-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00186-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00186-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00186-141">**EM- \_ GETPAGEROTATE**</span><span class="sxs-lookup"><span data-stu-id="00186-141">**EM\_GETPAGEROTATE**</span></span>](em-getpagerotate.md)
</dt> </dl>

 

 





