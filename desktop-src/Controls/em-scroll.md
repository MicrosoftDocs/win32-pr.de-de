---
title: EM_SCROLL Meldung (Winuser. h)
description: Führt einen vertikalen Bildlauf in einem mehrzeiligen Bearbeitungs Steuerelement aus. Diese Meldung entspricht dem Senden einer WM- \_ VScroll-Nachricht an das Bearbeitungs Steuerelement. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- Windows-Steuerelemente für EM_SCROLL Meldung
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106268"
---
# <a name="em_scroll-message"></a><span data-ttu-id="c0b12-106">EM- \_ scrollnachricht</span><span class="sxs-lookup"><span data-stu-id="c0b12-106">EM\_SCROLL message</span></span>

<span data-ttu-id="c0b12-107">Führt einen vertikalen Bildlauf in einem mehrzeiligen Bearbeitungs Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="c0b12-107">Scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="c0b12-108">Diese Meldung entspricht dem Senden einer [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht an das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c0b12-108">This message is equivalent to sending a [**WM\_VSCROLL**](wm-vscroll.md) message to the edit control.</span></span> <span data-ttu-id="c0b12-109">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="c0b12-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0b12-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0b12-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b12-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0b12-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0b12-112">Die Aktion, die von der Scrollleiste ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0b12-112">The action the scroll bar is to take.</span></span> <span data-ttu-id="c0b12-113">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c0b12-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c0b12-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c0b12-114">Value</span></span>                                                                                                                                                   | <span data-ttu-id="c0b12-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c0b12-115">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="c0b12-116"><dt>**SB- \_ LineDown**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b12-116"><dt>**SB\_LINEDOWN**</dt></span></span> </dl> | <span data-ttu-id="c0b12-117">Führt einen Bildlauf um eine Zeile nach unten durch</span><span class="sxs-lookup"><span data-stu-id="c0b12-117">Scrolls down one line.</span></span><br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="c0b12-118"><dt>**SB \_ -Auflistung**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b12-118"><dt>**SB\_LINEUP**</dt></span></span> </dl>       | <span data-ttu-id="c0b12-119">Führt einen Bildlauf eine Zeile nach oben aus</span><span class="sxs-lookup"><span data-stu-id="c0b12-119">Scrolls up one line.</span></span><br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="c0b12-120"><dt>**SB- \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b12-120"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl> | <span data-ttu-id="c0b12-121">Scrollt eine Seite nach unten</span><span class="sxs-lookup"><span data-stu-id="c0b12-121">Scrolls down one page.</span></span><br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="c0b12-122"><dt>**SB- \_ PageUp**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b12-122"><dt>**SB\_PAGEUP**</dt></span></span> </dl>       | <span data-ttu-id="c0b12-123">Führt einen Bildlauf eine Seite nach oben aus</span><span class="sxs-lookup"><span data-stu-id="c0b12-123">Scrolls up one page.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c0b12-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0b12-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0b12-125">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b12-125">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b12-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0b12-126">Return value</span></span>

<span data-ttu-id="c0b12-127">Wenn die Nachricht erfolgreich ist, ist das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) des Rückgabewerts **true**, und das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die Anzahl der Zeilen, in denen der Befehl einen Bildlauf durchführt.</span><span class="sxs-lookup"><span data-stu-id="c0b12-127">If the message is successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the return value is **TRUE**, and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the number of lines that the command scrolls.</span></span> <span data-ttu-id="c0b12-128">Die zurückgegebene Zahl ist möglicherweise nicht identisch mit der tatsächlichen Anzahl der Zeilen, die gescrollt werden, wenn der Bildlauf an den Anfang oder das Ende des Texts verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="c0b12-128">The number returned may not be the same as the actual number of lines scrolled if the scrolling moves to the beginning or the end of the text.</span></span> <span data-ttu-id="c0b12-129">Wenn der *wParam* -Parameter einen ungültigen Wert angibt, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="c0b12-129">If the *wParam* parameter specifies an invalid value, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0b12-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0b12-130">Remarks</span></span>

<span data-ttu-id="c0b12-131">Um einen Bildlauf zu einer bestimmten Zeile oder Zeichenposition durchführen zu können, verwenden Sie die [**EM \_ linescroll**](em-linescroll.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c0b12-131">To scroll to a specific line or character position, use the [**EM\_LINESCROLL**](em-linescroll.md) message.</span></span> <span data-ttu-id="c0b12-132">Wenn Sie die Einfügemarke in die Ansicht scrollen möchten, verwenden Sie die [**EM \_ scrollcaret**](em-scrollcaret.md)</span><span class="sxs-lookup"><span data-stu-id="c0b12-132">To scroll the caret into view, use the [**EM\_SCROLLCARET**](em-scrollcaret.md) message.</span></span>

<span data-ttu-id="c0b12-133">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c0b12-133">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c0b12-134">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="c0b12-134">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b12-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0b12-135">Requirements</span></span>



| <span data-ttu-id="c0b12-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0b12-136">Requirement</span></span> | <span data-ttu-id="c0b12-137">Wert</span><span class="sxs-lookup"><span data-stu-id="c0b12-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b12-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0b12-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b12-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0b12-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c0b12-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0b12-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b12-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0b12-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c0b12-142">Header</span><span class="sxs-lookup"><span data-stu-id="c0b12-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b12-143"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c0b12-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b12-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0b12-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0b12-145">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c0b12-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c0b12-146">**EM- \_ linescroll**</span><span class="sxs-lookup"><span data-stu-id="c0b12-146">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="c0b12-147">**EM \_ scrollcaret**</span><span class="sxs-lookup"><span data-stu-id="c0b12-147">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="c0b12-148">**WM- \_ VScroll**</span><span class="sxs-lookup"><span data-stu-id="c0b12-148">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

