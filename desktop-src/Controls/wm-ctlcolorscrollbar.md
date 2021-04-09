---
title: WM_CTLCOLORSCROLLBAR Meldung (Winuser. h)
description: Die WM- \_ ctlcolorscrollbar-Meldung wird an das übergeordnete Fenster eines ScrollBar-Steuer Elements gesendet, wenn das Steuerelement gezeichnet wird.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- Windows-Steuerelemente für WM_CTLCOLORSCROLLBAR Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949814"
---
# <a name="wm_ctlcolorscrollbar-message"></a><span data-ttu-id="3a274-104">WM \_ ctlcolorscrollbar-Meldung</span><span class="sxs-lookup"><span data-stu-id="3a274-104">WM\_CTLCOLORSCROLLBAR message</span></span>

<span data-ttu-id="3a274-105">Die **WM- \_ ctlcolorscrollbar** -Meldung wird an das übergeordnete Fenster eines ScrollBar-Steuer Elements gesendet, wenn das Steuerelement gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3a274-105">The **WM\_CTLCOLORSCROLLBAR** message is sent to the parent window of a scroll bar control when the control is about to be drawn.</span></span> <span data-ttu-id="3a274-106">Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster den Kontext Zieh Punkt der Anzeige verwenden, um die Hintergrundfarbe des ScrollBar-Steuer Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3a274-106">By responding to this message, the parent window can use the display context handle to set the background color of the scroll bar control.</span></span>

<span data-ttu-id="3a274-107">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3a274-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3a274-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a274-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a274-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a274-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a274-110">Handle für den Gerätekontext für das ScrollBar-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3a274-110">Handle to the device context for the scroll bar control.</span></span>

</dd> <dt>

<span data-ttu-id="3a274-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a274-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a274-112">Handle für die Bild Lauf Leiste.</span><span class="sxs-lookup"><span data-stu-id="3a274-112">Handle to the scroll bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a274-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a274-113">Return value</span></span>

<span data-ttu-id="3a274-114">Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie das Handle an einen Pinsel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3a274-114">If an application processes this message, it must return the handle to a brush.</span></span> <span data-ttu-id="3a274-115">Das System verwendet den Pinsel zum Zeichnen des Hintergrunds des ScrollBar-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="3a274-115">The system uses the brush to paint the background of the scroll bar control.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a274-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a274-116">Remarks</span></span>

<span data-ttu-id="3a274-117">Wenn die Anwendung einen Pinsel zurückgibt, den Sie erstellt hat (z. b. durch die Verwendung [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) [**kreatesolidbrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) " oder "-Funktion"), muss die Anwendung den Pinsel freigeben.</span><span class="sxs-lookup"><span data-stu-id="3a274-117">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="3a274-118">Wenn die Anwendung einen System Pinsel zurückgibt (z. b. einen, der von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion oder der [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion abgerufen wurde), muss die Anwendung den Pinsel nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="3a274-118">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="3a274-119">Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für das ScrollBar-Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="3a274-119">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the scroll bar control.</span></span>

<span data-ttu-id="3a274-120">Die " **WM \_ ctlcolorscrollbar** "-Nachricht wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.</span><span class="sxs-lookup"><span data-stu-id="3a274-120">The **WM\_CTLCOLORSCROLLBAR** message is never sent between threads; it is only sent within the same thread.</span></span>

<span data-ttu-id="3a274-121">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3a274-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="3a274-122">Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a274-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="3a274-123">Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3a274-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="3a274-124">Die " **WM \_ ctlcolorscrollbar** "-Meldung wird nur von untergeordneten ScrollBar-Steuerelementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a274-124">The **WM\_CTLCOLORSCROLLBAR** message is used only by child scroll bar controls.</span></span> <span data-ttu-id="3a274-125">Bild Lauf leisten, die an ein Fenster angefügt sind (WS \_ Scroll und WS \_ VScroll), generieren diese Meldung nicht.</span><span class="sxs-lookup"><span data-stu-id="3a274-125">Scrollbars attached to a window (WS\_SCROLL and WS\_VSCROLL) do not generate this message.</span></span> <span data-ttu-id="3a274-126">Verwenden Sie zum Anpassen der Darstellung von Bild Lauf leisten, die an ein Fenster angefügt sind, die Funktionen der flatscrollleiste.</span><span class="sxs-lookup"><span data-stu-id="3a274-126">To customize the appearance of scrollbars attached to a window, use the flat scroll bar functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a274-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a274-127">Requirements</span></span>



| <span data-ttu-id="3a274-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a274-128">Requirement</span></span> | <span data-ttu-id="3a274-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3a274-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a274-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a274-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a274-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a274-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3a274-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a274-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a274-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a274-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a274-134">Header</span><span class="sxs-lookup"><span data-stu-id="3a274-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a274-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3a274-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a274-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a274-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a274-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="3a274-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3a274-138">**WM \_ ctlcolorbtn**</span><span class="sxs-lookup"><span data-stu-id="3a274-138">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="3a274-139">**WM \_ ctlcoloredit**</span><span class="sxs-lookup"><span data-stu-id="3a274-139">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="3a274-140">**WM \_ ctlcolorlistbox**</span><span class="sxs-lookup"><span data-stu-id="3a274-140">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="3a274-141">**WM \_ ctlcolorstatic**</span><span class="sxs-lookup"><span data-stu-id="3a274-141">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="3a274-142">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="3a274-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3a274-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3a274-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3a274-144">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="3a274-144">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="3a274-145">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="3a274-145">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="3a274-146">**WM \_ ctlcolordlg**</span><span class="sxs-lookup"><span data-stu-id="3a274-146">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

