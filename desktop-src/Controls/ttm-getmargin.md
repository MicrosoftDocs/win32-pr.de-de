---
title: TTM_GETMARGIN Meldung (kommstrg. h)
description: Ruft die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster ab. Ein Rand ist der Abstand zwischen dem QuickInfo-Fensterrahmen und dem im QuickInfo-Fenster enthaltenen Text in Pixel.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- Windows-Steuerelemente für TTM_GETMARGIN Meldung
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956489"
---
# <a name="ttm_getmargin-message"></a><span data-ttu-id="5b1e2-105">TTM \_ getMargin-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5b1e2-105">TTM\_GETMARGIN message</span></span>

<span data-ttu-id="5b1e2-106">Ruft die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-106">Retrieves the top, left, bottom, and right margins set for a tooltip window.</span></span> <span data-ttu-id="5b1e2-107">Ein Rand ist der Abstand zwischen dem QuickInfo-Fensterrahmen und dem im QuickInfo-Fenster enthaltenen Text in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b1e2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b1e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b1e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b1e2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5b1e2-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5b1e2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b1e2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b1e2-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Rand Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the margin information.</span></span> <span data-ttu-id="5b1e2-113">Die Elemente der **Rect** -Struktur definieren kein Begrenzungs Rechteck.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="5b1e2-114">Für den Zweck dieser Nachricht werden die Strukturmember wie folgt interpretiert:</span><span class="sxs-lookup"><span data-stu-id="5b1e2-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="5b1e2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5b1e2-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="5b1e2-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5b1e2-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="5b1e2-117"><dt>**top**</dt></span><span class="sxs-lookup"><span data-stu-id="5b1e2-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="5b1e2-118">Abstand zwischen dem oberen und oberen Rand des QuickInfo-Texts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="5b1e2-119"><dt>**linken**</dt></span><span class="sxs-lookup"><span data-stu-id="5b1e2-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="5b1e2-120">Abstand zwischen dem linken Rand und dem linken Ende des QuickInfo-Texts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="5b1e2-121"><dt>**unten**</dt></span><span class="sxs-lookup"><span data-stu-id="5b1e2-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="5b1e2-122">Abstand zwischen dem unteren und dem unteren Rand des QuickInfo-Texts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="5b1e2-123"><dt>**Richting**</dt></span><span class="sxs-lookup"><span data-stu-id="5b1e2-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="5b1e2-124">Abstand zwischen dem rechten Rand und dem rechten Ende des QuickInfo-Texts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b1e2-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b1e2-125">Return value</span></span>

<span data-ttu-id="5b1e2-126">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b1e2-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b1e2-127">Remarks</span></span>

<span data-ttu-id="5b1e2-128">Alle vier Ränder werden standardmäßig auf 0 gesetzt, wenn Sie das ToolTip-Steuerelement erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b1e2-128">All four margins default to zero when you create the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1e2-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b1e2-129">Requirements</span></span>



| <span data-ttu-id="5b1e2-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b1e2-130">Requirement</span></span> | <span data-ttu-id="5b1e2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5b1e2-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1e2-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b1e2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5b1e2-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b1e2-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b1e2-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b1e2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5b1e2-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b1e2-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b1e2-136">Header</span><span class="sxs-lookup"><span data-stu-id="5b1e2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b1e2-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b1e2-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b1e2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b1e2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b1e2-139">**TTM- \_ setMargin**</span><span class="sxs-lookup"><span data-stu-id="5b1e2-139">**TTM\_SETMARGIN**</span></span>](ttm-setmargin.md)
</dt> </dl>

 

