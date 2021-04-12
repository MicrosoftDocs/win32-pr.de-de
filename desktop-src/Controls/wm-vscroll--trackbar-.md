---
title: WM_VSCROLL (TrackBar)-Benachrichtigungs Code (Winuser. h)
description: Die WM- \_ VScroll-Nachricht wird an den Besitzer eines vertikalen TrackBar-Steuer Elements gesendet, wenn die Position des Schiebereglers geändert wird. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- WM_VSCROLL (TrackBar)-Benachrichtigungs Code Windows-Steuerelemente
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
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104415"
---
# <a name="wm_vscroll-trackbar-notification-code"></a><span data-ttu-id="d919b-105">WM- \_ VScroll-Benachrichtigungs Code (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="d919b-105">WM\_VSCROLL (Trackbar) notification code</span></span>

<span data-ttu-id="d919b-106">Die **WM- \_ VScroll** -Nachricht wird an den Besitzer eines vertikalen TrackBar-Steuer Elements gesendet, wenn die Position des Schiebereglers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d919b-106">The **WM\_VSCROLL** message is sent to the owner of a vertical trackbar control when the slider changes position.</span></span>

<span data-ttu-id="d919b-107">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d919b-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d919b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d919b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d919b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d919b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d919b-110">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die aktuelle Position des Schiebereglers an, wenn das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) eine TB- \_ Fingerposition oder TB-Finger \_ Abdruck aufweist.</span><span class="sxs-lookup"><span data-stu-id="d919b-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the slider if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is TB\_THUMBPOSITION or TB\_THUMBTRACK.</span></span> <span data-ttu-id="d919b-111">Für alle anderen Benachrichtigungs Codes ist das höchst wertige Wort 0 (null). sendet die [**TBM- \_ GetPos**](tbm-getpos.md) -Nachricht, um die Position des Schiebereglers zu ermitteln</span><span class="sxs-lookup"><span data-stu-id="d919b-111">For all other notification codes, the high-order word is zero; send the [**TBM\_GETPOS**](tbm-getpos.md) message to determine the slider position.</span></span>

<span data-ttu-id="d919b-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt einen Benachrichtigungs Code an, der die Interaktion des Benutzers mit der TrackBar angibt.</span><span class="sxs-lookup"><span data-stu-id="d919b-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a notification code that indicates the user's interaction with the trackbar.</span></span> <span data-ttu-id="d919b-113">Bei diesem Wort kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="d919b-113">This word can be one of the following values.</span></span>



| <span data-ttu-id="d919b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d919b-114">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="d919b-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d919b-115">Meaning</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <span data-ttu-id="d919b-116"><dt>**TB \_ unten**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-116"><dt>**TB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="d919b-117">Der Benutzer hat die endtaste gedrückt ([**VK- \_ Ende**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="d919b-117">The user pressed the END key ([**VK\_END**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <span data-ttu-id="d919b-118"><dt>**TB- \_ EndTrack**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-118"><dt>**TB\_ENDTRACK**</dt></span></span> </dl>                | <span data-ttu-id="d919b-119">Die TrackBar erhielt eine [**WM- \_ KeyUp**](/windows/desktop/inputdev/wm-keyup), was bedeutet, dass der Benutzer einen Schlüssel freigegeben hat, der einen relevanten Code für den virtuellen Schlüssel gesendet hat</span><span class="sxs-lookup"><span data-stu-id="d919b-119">The trackbar received [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup), meaning that the user released a key that sent a relevant virtual key code.</span></span> <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <span data-ttu-id="d919b-120"><dt>**TB \_ nach unten**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-120"><dt>**TB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="d919b-121">Der Benutzer hat den Pfeil nach rechts ([**VK \_ Rechts**](/windows/desktop/inputdev/virtual-key-codes)) oder die nach-unten-Taste ([**VK- \_ ab**](/windows/desktop/inputdev/virtual-key-codes)) gedrückt.</span><span class="sxs-lookup"><span data-stu-id="d919b-121">The user pressed the RIGHT ARROW ([**VK\_RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) or DOWN ARROW ([**VK\_DOWN**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <span data-ttu-id="d919b-122"><dt>**TB \_ -Auflistung**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-122"><dt>**TB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="d919b-123">Der Benutzer hat den Pfeil nach links ([**VK \_ Links**](/windows/desktop/inputdev/virtual-key-codes)) oder nach oben (nach [**oben) gedrückt \_**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="d919b-123">The user pressed the LEFT ARROW ([**VK\_LEFT**](/windows/desktop/inputdev/virtual-key-codes)) or UP ARROW ([**VK\_UP**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <span data-ttu-id="d919b-124"><dt>**TB- \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-124"><dt>**TB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="d919b-125">Der Benutzer hat auf den Kanal unten oder rechts neben dem Schieberegler geklickt ("[**VK \_ Next**](/windows/desktop/inputdev/virtual-key-codes)").</span><span class="sxs-lookup"><span data-stu-id="d919b-125">The user clicked the channel below or to the right of the slider ([**VK\_NEXT**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <span data-ttu-id="d919b-126"><dt>**TB- \_ PageUp**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-126"><dt>**TB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="d919b-127">Der Benutzer hat auf den Kanal oberhalb oder links neben dem Schieberegler geklickt ([**VK \_ vor**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="d919b-127">The user clicked the channel above or to the left of the slider ([**VK\_PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <span data-ttu-id="d919b-128"><dt>**TB-Finger \_ Position**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-128"><dt>**TB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="d919b-129">Die TrackBar erhielt [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) nach einem Finger \_ Abdruck-Benachrichtigungs Code von TB.</span><span class="sxs-lookup"><span data-stu-id="d919b-129">The trackbar received [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) following a TB\_THUMBTRACK notification code.</span></span><br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <span data-ttu-id="d919b-130"><dt>**TB-Finger \_ Abdruck**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-130"><dt>**TB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="d919b-131">Der Benutzer hat den Schieberegler gezogen.</span><span class="sxs-lookup"><span data-stu-id="d919b-131">The user dragged the slider.</span></span><br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <span data-ttu-id="d919b-132"><dt>**TB ( \_ oben)**</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-132"><dt>**TB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="d919b-133">Der Benutzer hat die Start Taste gedrückt ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="d919b-133">The user pressed the HOME key ([**VK\_HOME**](/windows/desktop/inputdev/virtual-key-codes)).</span></span> <br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="d919b-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d919b-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d919b-135">Das Handle für das TrackBar-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d919b-135">The handle to the trackbar control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d919b-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d919b-136">Return value</span></span>

<span data-ttu-id="d919b-137">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d919b-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d919b-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d919b-138">Remarks</span></span>

<span data-ttu-id="d919b-139">Der TB-Finger \_ Abdruck Code wird in der Regel von Anwendungen verwendet, die Feedback geben, wenn der Benutzer das Bild Lauf Feld zieht.</span><span class="sxs-lookup"><span data-stu-id="d919b-139">The TB\_THUMBTRACK code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="d919b-140">Beachten Sie, dass die **WM- \_ VScroll** -Nachricht nur 16 Bits an Positionsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="d919b-140">Note that the **WM\_VSCROLL** message carries only 16 bits of position data.</span></span> <span data-ttu-id="d919b-141">Daher haben Anwendungen, die ausschließlich auf **WM \_ VScroll** (und [**WM \_ HScroll**](wm-hscroll--trackbar-.md)) für Schieberegler-Positionsdaten basieren, einen praktischen maximalen Positionswert von 65.535.</span><span class="sxs-lookup"><span data-stu-id="d919b-141">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll--trackbar-.md)) for slider position data have a practical maximum position value of 65,535.</span></span>

## <a name="requirements"></a><span data-ttu-id="d919b-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d919b-142">Requirements</span></span>



| <span data-ttu-id="d919b-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d919b-143">Requirement</span></span> | <span data-ttu-id="d919b-144">Wert</span><span class="sxs-lookup"><span data-stu-id="d919b-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d919b-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d919b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d919b-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d919b-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d919b-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d919b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d919b-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d919b-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d919b-149">Header</span><span class="sxs-lookup"><span data-stu-id="d919b-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="d919b-150"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d919b-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d919b-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d919b-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="d919b-152">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d919b-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d919b-153">**WM- \_ HScroll**</span><span class="sxs-lookup"><span data-stu-id="d919b-153">**WM\_HSCROLL**</span></span>](wm-hscroll--trackbar-.md)
</dt> </dl>

 

