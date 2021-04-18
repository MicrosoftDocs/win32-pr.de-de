---
title: TTM_SETMARGIN Meldung (kommstrg. h)
description: Legt die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster fest. Ein Rand ist der Abstand zwischen dem QuickInfo-Fensterrahmen und dem im QuickInfo-Fenster enthaltenen Text in Pixel.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- Windows-Steuerelemente für TTM_SETMARGIN Meldung
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338732"
---
# <a name="ttm_setmargin-message"></a><span data-ttu-id="fe9fa-105">TTM- \_ setMargin-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fe9fa-105">TTM\_SETMARGIN message</span></span>

<span data-ttu-id="fe9fa-106">Legt die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-106">Sets the top, left, bottom, and right margins for a tooltip window.</span></span> <span data-ttu-id="fe9fa-107">Ein Rand ist der Abstand zwischen dem QuickInfo-Fensterrahmen und dem im QuickInfo-Fenster enthaltenen Text in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe9fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe9fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe9fa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe9fa-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe9fa-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fe9fa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe9fa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe9fa-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die zu festzulegenden Rand Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margin information to be set.</span></span> <span data-ttu-id="fe9fa-113">Die Elemente der **Rect** -Struktur definieren kein Begrenzungs Rechteck.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="fe9fa-114">Für den Zweck dieser Nachricht werden die Strukturmember wie folgt interpretiert:</span><span class="sxs-lookup"><span data-stu-id="fe9fa-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="fe9fa-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fe9fa-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="fe9fa-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fe9fa-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="fe9fa-117"><dt>**top**</dt></span><span class="sxs-lookup"><span data-stu-id="fe9fa-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="fe9fa-118">Abstand zwischen dem oberen und oberen Rand des QuickInfo-Texts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="fe9fa-119"><dt>**linken**</dt></span><span class="sxs-lookup"><span data-stu-id="fe9fa-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="fe9fa-120">Abstand zwischen dem linken Rand und dem linken Ende des QuickInfo-Texts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="fe9fa-121"><dt>**unten**</dt></span><span class="sxs-lookup"><span data-stu-id="fe9fa-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="fe9fa-122">Abstand zwischen dem unteren und dem unteren Rand des QuickInfo-Texts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="fe9fa-123"><dt>**Richting**</dt></span><span class="sxs-lookup"><span data-stu-id="fe9fa-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="fe9fa-124">Abstand zwischen dem rechten Rand und dem rechten Ende des QuickInfo-Texts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe9fa-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe9fa-125">Return value</span></span>

<span data-ttu-id="fe9fa-126">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe9fa-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe9fa-127">Remarks</span></span>

<span data-ttu-id="fe9fa-128">Diese Nachricht hat keine Auswirkung, wenn die Anwendung unter Windows Vista ausgeführt wird und visuelle Stile für die QuickInfo aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-128">This message has no effect when the application runs on Windows Vista and visual styles are enabled for the tooltip.</span></span> <span data-ttu-id="fe9fa-129">Sie können visuelle Stile für die QuickInfo mithilfe von [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fe9fa-129">You can disable visual styles for the tooltip by using [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe9fa-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe9fa-130">Requirements</span></span>



| <span data-ttu-id="fe9fa-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe9fa-131">Requirement</span></span> | <span data-ttu-id="fe9fa-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fe9fa-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9fa-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe9fa-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fe9fa-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe9fa-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe9fa-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe9fa-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fe9fa-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe9fa-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe9fa-137">Header</span><span class="sxs-lookup"><span data-stu-id="fe9fa-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe9fa-138"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe9fa-138"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe9fa-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe9fa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9fa-140">**TTM \_ getMargin**</span><span class="sxs-lookup"><span data-stu-id="fe9fa-140">**TTM\_GETMARGIN**</span></span>](ttm-getmargin.md)
</dt> </dl>

 

