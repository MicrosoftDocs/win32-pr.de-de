---
title: WM_VSCROLL Meldung (Winuser. h)
description: Die WM \_ -VScroll-Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der vertikalen Standard Scrollleiste des Fensters auftritt.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- Windows-Steuerelemente für WM_VSCROLL Meldung
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106154"
---
# <a name="wm_vscroll-message"></a><span data-ttu-id="13c37-104">WM- \_ VScroll-Nachricht</span><span class="sxs-lookup"><span data-stu-id="13c37-104">WM\_VSCROLL message</span></span>

<span data-ttu-id="13c37-105">Die **WM- \_ VScroll** -Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der vertikalen Standard Scrollleiste des Fensters auftritt.</span><span class="sxs-lookup"><span data-stu-id="13c37-105">The **WM\_VSCROLL** message is sent to a window when a scroll event occurs in the window's standard vertical scroll bar.</span></span> <span data-ttu-id="13c37-106">Diese Meldung wird auch an den Besitzer eines vertikalen Schiebe leisten-Steuer Elements gesendet, wenn im-Steuerelement ein scrollereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="13c37-106">This message is also sent to the owner of a vertical scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="13c37-107">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="13c37-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="13c37-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="13c37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c37-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13c37-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13c37-110">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die aktuelle Position des Bild Lauf Felds an, wenn das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) SB- \_ Fingerposition oder SB-Finger \_ Abdruck ist; andernfalls wird dieses Wort nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="13c37-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="13c37-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt einen Scrollleisten-Wert an, der die scrollanforderung des Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="13c37-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="13c37-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="13c37-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="13c37-113">Wert</span><span class="sxs-lookup"><span data-stu-id="13c37-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="13c37-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="13c37-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="13c37-115"><dt>**SB \_ unten**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-115"><dt>**SB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="13c37-116">Führt einen Bildlauf nach unten rechts aus.</span><span class="sxs-lookup"><span data-stu-id="13c37-116">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="13c37-117"><dt>**SB- \_ endscroll**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-117"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="13c37-118">Beendet den Bildlauf.</span><span class="sxs-lookup"><span data-stu-id="13c37-118">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="13c37-119"><dt>**SB- \_ LineDown**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-119"><dt>**SB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="13c37-120">Führt einen Bildlauf nach unten durch.</span><span class="sxs-lookup"><span data-stu-id="13c37-120">Scrolls one line down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="13c37-121"><dt>**SB \_ -Auflistung**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-121"><dt>**SB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="13c37-122">Führt einen Bildlauf nach oben durch.</span><span class="sxs-lookup"><span data-stu-id="13c37-122">Scrolls one line up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="13c37-123"><dt>**SB- \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-123"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="13c37-124">Führt einen Bildlauf nach unten durch.</span><span class="sxs-lookup"><span data-stu-id="13c37-124">Scrolls one page down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="13c37-125"><dt>**SB- \_ PageUp**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-125"><dt>**SB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="13c37-126">Führt einen Bildlauf nach oben durch.</span><span class="sxs-lookup"><span data-stu-id="13c37-126">Scrolls one page up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="13c37-127"><dt>**SB-Finger \_ Position**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-127"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="13c37-128">Der Benutzer hat das Bild Lauf Feld (Thumb) gezogen und die Maustaste losgelassen.</span><span class="sxs-lookup"><span data-stu-id="13c37-128">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="13c37-129">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) zeigt die Position des Bild Lauf Felds am Ende des Zieh Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="13c37-129">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="13c37-130"><dt>**SB-Finger \_ Abdruck**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-130"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="13c37-131">Der Benutzer zieht die Bildlaufbox.</span><span class="sxs-lookup"><span data-stu-id="13c37-131">The user is dragging the scroll box.</span></span> <span data-ttu-id="13c37-132">Diese Meldung wird wiederholt gesendet, bis der Benutzer die Maustaste loslässt.</span><span class="sxs-lookup"><span data-stu-id="13c37-132">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="13c37-133">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Position an, zu der das Bild Lauf Feld gezogen wurde.</span><span class="sxs-lookup"><span data-stu-id="13c37-133">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="13c37-134"><dt>**SB- \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-134"><dt>**SB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="13c37-135">Führt einen Bildlauf nach oben links durch.</span><span class="sxs-lookup"><span data-stu-id="13c37-135">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="13c37-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13c37-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13c37-137">Wenn die Nachricht von einem Schiebe leisten-Steuerelement gesendet wird, ist dieser Parameter das Handle für das ScrollBar-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="13c37-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="13c37-138">Wenn die Nachricht von einer Standard Scrollleiste gesendet wird, ist dieser Parameter **null**.</span><span class="sxs-lookup"><span data-stu-id="13c37-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13c37-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13c37-139">Return value</span></span>

<span data-ttu-id="13c37-140">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="13c37-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="13c37-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13c37-141">Remarks</span></span>

<span data-ttu-id="13c37-142">Der SB- \_ ThumbTrack-Anforderungs Code wird in der Regel von Anwendungen verwendet, die Feedback geben, wenn der Benutzer das Bild Lauf Feld zieht.</span><span class="sxs-lookup"><span data-stu-id="13c37-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="13c37-143">Wenn eine Anwendung im Inhalt des Fensters einen Bildlauf durchführt, muss Sie auch die Position des Bild Lauf Felds mithilfe der [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) -Funktion Zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="13c37-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="13c37-144">Beachten Sie, dass die **WM \_ VScroll** -Nachricht nur 16 Bits an Positionsdaten der Scrollbox enthält.</span><span class="sxs-lookup"><span data-stu-id="13c37-144">Note that the **WM\_VSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="13c37-145">Daher haben Anwendungen, die sich ausschließlich auf **WM \_ VScroll** (und [**WM \_ HScroll**](wm-hscroll.md)) für Bild Lauf Positionsdaten verlassen, einen praktischen maximalen Positionswert von 65.535.</span><span class="sxs-lookup"><span data-stu-id="13c37-145">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="13c37-146">Da die Funktionen [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**setscrollrange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**getscrollpos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)und [**getscrollrange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) jedoch 32-Bit-ScrollBar-Positionsdaten unterstützen, gibt es eine Möglichkeit, die 16-Bit-Barriere der [**WM \_ HScroll**](wm-hscroll.md) -und **WM \_ VScroll** -Nachrichten zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="13c37-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the [**WM\_HSCROLL**](wm-hscroll.md) and **WM\_VSCROLL** messages.</span></span> <span data-ttu-id="13c37-147">Eine Beschreibung der Technik finden Sie unter **getscrollinfo** .</span><span class="sxs-lookup"><span data-stu-id="13c37-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c37-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13c37-148">Requirements</span></span>



| <span data-ttu-id="13c37-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13c37-149">Requirement</span></span> | <span data-ttu-id="13c37-150">Wert</span><span class="sxs-lookup"><span data-stu-id="13c37-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c37-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13c37-151">Minimum supported client</span></span><br/> | <span data-ttu-id="13c37-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13c37-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13c37-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13c37-153">Minimum supported server</span></span><br/> | <span data-ttu-id="13c37-154">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13c37-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13c37-155">Header</span><span class="sxs-lookup"><span data-stu-id="13c37-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="13c37-156"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="13c37-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c37-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13c37-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="13c37-158">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="13c37-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="13c37-159">**Getscrollinfo**</span><span class="sxs-lookup"><span data-stu-id="13c37-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="13c37-160">**Getscrollpos**</span><span class="sxs-lookup"><span data-stu-id="13c37-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="13c37-161">**Getscrollrange**</span><span class="sxs-lookup"><span data-stu-id="13c37-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="13c37-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="13c37-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="13c37-163">**Setscrollpos**</span><span class="sxs-lookup"><span data-stu-id="13c37-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="13c37-164">**Setscrollrange**</span><span class="sxs-lookup"><span data-stu-id="13c37-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="13c37-165">**WM- \_ HScroll**</span><span class="sxs-lookup"><span data-stu-id="13c37-165">**WM\_HSCROLL**</span></span>](wm-hscroll.md)
</dt> <dt>

[<span data-ttu-id="13c37-166">**WM \_ VScroll (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="13c37-166">**WM\_VSCROLL (Trackbar)**</span></span>](wm-vscroll--trackbar-.md)
</dt> </dl>

 

