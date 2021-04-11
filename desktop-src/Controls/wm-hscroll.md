---
title: WM_HSCROLL Meldung (Winuser. h)
description: Die WM \_ -HScroll-Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der horizontalen Standard Scrollleiste des Fensters auftritt.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- Windows-Steuerelemente für WM_HSCROLL Meldung
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104421"
---
# <a name="wm_hscroll-message"></a><span data-ttu-id="30742-104">WM- \_ hscrollnachricht</span><span class="sxs-lookup"><span data-stu-id="30742-104">WM\_HSCROLL message</span></span>

<span data-ttu-id="30742-105">Die **WM- \_ HScroll** -Nachricht wird an ein Fenster gesendet, wenn ein scrollereignis in der horizontalen Standard Scrollleiste des Fensters auftritt.</span><span class="sxs-lookup"><span data-stu-id="30742-105">The **WM\_HSCROLL** message is sent to a window when a scroll event occurs in the window's standard horizontal scroll bar.</span></span> <span data-ttu-id="30742-106">Diese Meldung wird auch an den Besitzer eines horizontalen Schiebe leisten-Steuer Elements gesendet, wenn im-Steuerelement ein scrollereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="30742-106">This message is also sent to the owner of a horizontal scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="30742-107">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="30742-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="30742-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="30742-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30742-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30742-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30742-110">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die aktuelle Position des Bild Lauf Felds an, wenn das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) SB- \_ Fingerposition oder SB-Finger \_ Abdruck ist; andernfalls wird dieses Wort nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="30742-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="30742-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt einen Scrollleisten-Wert an, der die scrollanforderung des Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="30742-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="30742-112">Bei diesem Wort kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="30742-112">This word can be one of the following values.</span></span>



| <span data-ttu-id="30742-113">Wert</span><span class="sxs-lookup"><span data-stu-id="30742-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="30742-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="30742-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="30742-115"><dt>**SB- \_ endscroll**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-115"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="30742-116">Beendet den Bildlauf.</span><span class="sxs-lookup"><span data-stu-id="30742-116">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="30742-117"><dt>**SB \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-117"><dt>**SB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="30742-118">Führt einen Bildlauf nach oben links durch.</span><span class="sxs-lookup"><span data-stu-id="30742-118">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="30742-119"><dt>**SB \_ right**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-119"><dt>**SB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="30742-120">Führt einen Bildlauf nach unten rechts aus.</span><span class="sxs-lookup"><span data-stu-id="30742-120">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="30742-121"><dt>**SB- \_ LineLeft**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-121"><dt>**SB\_LINELEFT**</dt></span></span> </dl>                | <span data-ttu-id="30742-122">Scrollt nach links um eine Einheit.</span><span class="sxs-lookup"><span data-stu-id="30742-122">Scrolls left by one unit.</span></span><br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="30742-123"><dt>**SB- \_ LineRight**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-123"><dt>**SB\_LINERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="30742-124">Scrollt nach rechts um eine Einheit.</span><span class="sxs-lookup"><span data-stu-id="30742-124">Scrolls right by one unit.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="30742-125"><dt>**SB- \_ PageLeft**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-125"><dt>**SB\_PAGELEFT**</dt></span></span> </dl>                | <span data-ttu-id="30742-126">Führt einen Bildlauf nach links um die Breite des Fensters aus.</span><span class="sxs-lookup"><span data-stu-id="30742-126">Scrolls left by the width of the window.</span></span><br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="30742-127"><dt>**SB- \_ PageRight**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-127"><dt>**SB\_PAGERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="30742-128">Führt einen Bildlauf nach rechts um die Breite des Fensters aus.</span><span class="sxs-lookup"><span data-stu-id="30742-128">Scrolls right by the width of the window.</span></span><br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="30742-129"><dt>**SB-Finger \_ Position**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-129"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="30742-130">Der Benutzer hat das Bild Lauf Feld (Thumb) gezogen und die Maustaste losgelassen.</span><span class="sxs-lookup"><span data-stu-id="30742-130">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="30742-131">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) zeigt die Position des Bild Lauf Felds am Ende des Zieh Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="30742-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="30742-132"><dt>**SB-Finger \_ Abdruck**</dt></span><span class="sxs-lookup"><span data-stu-id="30742-132"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="30742-133">Der Benutzer zieht die Bildlaufbox.</span><span class="sxs-lookup"><span data-stu-id="30742-133">The user is dragging the scroll box.</span></span> <span data-ttu-id="30742-134">Diese Meldung wird wiederholt gesendet, bis der Benutzer die Maustaste loslässt.</span><span class="sxs-lookup"><span data-stu-id="30742-134">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="30742-135">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Position an, zu der das Bild Lauf Feld gezogen wurde.</span><span class="sxs-lookup"><span data-stu-id="30742-135">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="30742-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30742-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30742-137">Wenn die Nachricht von einem Schiebe leisten-Steuerelement gesendet wird, ist dieser Parameter das Handle für das ScrollBar-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="30742-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="30742-138">Wenn die Nachricht von einer Standard Scrollleiste gesendet wird, ist dieser Parameter **null**.</span><span class="sxs-lookup"><span data-stu-id="30742-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30742-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30742-139">Return value</span></span>

<span data-ttu-id="30742-140">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="30742-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="30742-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30742-141">Remarks</span></span>

<span data-ttu-id="30742-142">Der SB- \_ ThumbTrack-Anforderungs Code wird in der Regel von Anwendungen verwendet, die Feedback geben, wenn der Benutzer das Bild Lauf Feld zieht.</span><span class="sxs-lookup"><span data-stu-id="30742-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="30742-143">Wenn eine Anwendung im Inhalt des Fensters einen Bildlauf durchführt, muss Sie auch die Position des Bild Lauf Felds mithilfe der [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) -Funktion Zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="30742-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="30742-144">Beachten Sie, dass die **WM- \_ HScroll** -Nachricht nur 16 Bits an Positionsdaten der Scrollbox enthält.</span><span class="sxs-lookup"><span data-stu-id="30742-144">Note that the **WM\_HSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="30742-145">Daher haben Anwendungen, die ausschließlich von **WM \_ HScroll** (und [**WM \_ VScroll**](wm-vscroll.md)) für Bild Lauf Positionsdaten abhängen, einen praktischen maximalen Positionswert von 65.535.</span><span class="sxs-lookup"><span data-stu-id="30742-145">Thus, applications that rely solely on **WM\_HSCROLL** (and [**WM\_VSCROLL**](wm-vscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="30742-146">Da die Funktionen [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**setscrollrange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**getscrollpos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)und [**getscrollrange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) jedoch 32-Bit-ScrollBar-Positionsdaten unterstützen, gibt es eine Möglichkeit, die 16-Bit-Barriere der **WM \_ HScroll** -und [**WM \_ VScroll**](wm-vscroll.md) -Nachrichten zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="30742-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the **WM\_HSCROLL** and [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span> <span data-ttu-id="30742-147">Eine Beschreibung der Technik finden Sie unter **getscrollinfo** .</span><span class="sxs-lookup"><span data-stu-id="30742-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="30742-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30742-148">Requirements</span></span>



| <span data-ttu-id="30742-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30742-149">Requirement</span></span> | <span data-ttu-id="30742-150">Wert</span><span class="sxs-lookup"><span data-stu-id="30742-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30742-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30742-151">Minimum supported client</span></span><br/> | <span data-ttu-id="30742-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30742-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30742-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30742-153">Minimum supported server</span></span><br/> | <span data-ttu-id="30742-154">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30742-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30742-155">Header</span><span class="sxs-lookup"><span data-stu-id="30742-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="30742-156"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="30742-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30742-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30742-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="30742-158">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="30742-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30742-159">**Getscrollinfo**</span><span class="sxs-lookup"><span data-stu-id="30742-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="30742-160">**Getscrollpos**</span><span class="sxs-lookup"><span data-stu-id="30742-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="30742-161">**Getscrollrange**</span><span class="sxs-lookup"><span data-stu-id="30742-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="30742-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="30742-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="30742-163">**Setscrollpos**</span><span class="sxs-lookup"><span data-stu-id="30742-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="30742-164">**Setscrollrange**</span><span class="sxs-lookup"><span data-stu-id="30742-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="30742-165">**WM \_ HScroll (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="30742-165">**WM\_HSCROLL (trackbar)**</span></span>](wm-hscroll--trackbar-.md)
</dt> <dt>

[<span data-ttu-id="30742-166">**WM- \_ VScroll**</span><span class="sxs-lookup"><span data-stu-id="30742-166">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

