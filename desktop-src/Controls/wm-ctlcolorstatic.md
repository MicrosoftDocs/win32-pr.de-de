---
title: WM_CTLCOLORSTATIC Meldung (Winuser. h)
description: Ein statisches Steuerelement oder ein Schreib geschütztes oder deaktiviertes Bearbeitungs Steuerelement sendet die WM \_ ctlcolorstatic-Meldung an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- Windows-Steuerelemente für WM_CTLCOLORSTATIC Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741368"
---
# <a name="wm_ctlcolorstatic-message"></a><span data-ttu-id="9d517-104">WM \_ ctlcolorstatic-Meldung</span><span class="sxs-lookup"><span data-stu-id="9d517-104">WM\_CTLCOLORSTATIC message</span></span>

<span data-ttu-id="9d517-105">Ein statisches Steuerelement oder ein Schreib geschütztes oder deaktiviertes Bearbeitungs Steuerelement sendet die **WM \_ ctlcolorstatic** -Meldung an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d517-105">A static control, or an edit control that is read-only or disabled, sends the **WM\_CTLCOLORSTATIC** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="9d517-106">Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster den angegebenen Gerätekontext Handle verwenden, um die Text Vordergrund-und Hintergrundfarben des statischen Steuer Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9d517-106">By responding to this message, the parent window can use the specified device context handle to set the text foreground and background colors of the static control.</span></span>

<span data-ttu-id="9d517-107">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9d517-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9d517-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d517-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d517-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d517-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d517-110">Handle für den Gerätekontext für das statische Steuerelement Fenster.</span><span class="sxs-lookup"><span data-stu-id="9d517-110">Handle to the device context for the static control window.</span></span>

</dd> <dt>

<span data-ttu-id="9d517-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d517-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d517-112">Handle für das statische Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9d517-112">Handle to the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d517-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d517-113">Return value</span></span>

<span data-ttu-id="9d517-114">Wenn eine Anwendung diese Nachricht verarbeitet, ist der Rückgabewert ein Handle für einen Pinsel, den das System zum Zeichnen des Hintergrunds des statischen Steuer Elements verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d517-114">If an application processes this message, the return value is a handle to a brush that the system uses to paint the background of the static control.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d517-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d517-115">Remarks</span></span>

<span data-ttu-id="9d517-116">Wenn die Anwendung einen Pinsel zurückgibt, den Sie erstellt hat (z. b. durch die Verwendung [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) [**kreatesolidbrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) " oder "-Funktion"), muss die Anwendung den Pinsel freigeben.</span><span class="sxs-lookup"><span data-stu-id="9d517-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="9d517-117">Wenn die Anwendung einen System Pinsel zurückgibt (z. b. einen, der von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion oder der [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion abgerufen wurde), muss die Anwendung den Pinsel nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="9d517-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="9d517-118">Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für das statische Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="9d517-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the static control.</span></span>

<span data-ttu-id="9d517-119">Sie können die Text Hintergrundfarbe eines deaktivierten Bearbeitungs Steuer Elements festlegen, aber Sie können die textvorder Grundfarbe nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="9d517-119">You can set the text background color of a disabled edit control, but you cannot set the text foreground color.</span></span> <span data-ttu-id="9d517-120">Das System verwendet immer Color \_ GrayText.</span><span class="sxs-lookup"><span data-stu-id="9d517-120">The system always uses COLOR\_GRAYTEXT.</span></span>

<span data-ttu-id="9d517-121">Wenn Sie Steuerelemente bearbeiten, die nicht schreibgeschützt oder deaktiviert sind, wird die " **WM \_ ctlcolorstatic** "-Nachricht nicht gesendet; stattdessen wird die [**WM- \_ ctlcoloredit**](wm-ctlcoloredit.md) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="9d517-121">Edit controls that are not read-only or disabled do not send the **WM\_CTLCOLORSTATIC** message; instead, they send the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

<span data-ttu-id="9d517-122">Die " **WM \_ ctlcolorstatic** "-Meldung wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.</span><span class="sxs-lookup"><span data-stu-id="9d517-122">The **WM\_CTLCOLORSTATIC** message is never sent between threads; it is sent only within the same thread.</span></span>

<span data-ttu-id="9d517-123">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9d517-123">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="9d517-124">Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d517-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="9d517-125">Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9d517-125">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="9d517-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d517-126">Examples</span></span>

<span data-ttu-id="9d517-127">Im folgenden C++-Beispiel wird gezeigt, wie die Text Vordergrund-und Hintergrundfarben eines statischen-Steuer Elements als Reaktion auf die **WM \_ ctlcolorstatic** -Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9d517-127">The following C++ example shows how to set the text foreground and background colors of a static control in response to the **WM\_CTLCOLORSTATIC** message.</span></span> <span data-ttu-id="9d517-128">Die `hbrBkgnd` Variable ist eine statische **hBrush** -Variable, die mit NULL initialisiert wird, und speichert den Hintergrund Pinsel zwischen den Aufrufen von **WM \_ ctlcolorstatic**.</span><span class="sxs-lookup"><span data-stu-id="9d517-128">The `hbrBkgnd` variable is a static **HBRUSH** variable that is initialized to NULL, and stores the background brush between calls to **WM\_CTLCOLORSTATIC**.</span></span> <span data-ttu-id="9d517-129">Der Pinsel muss durch einen Aufrufen der [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) -Funktion zerstört werden, wenn er nicht mehr benötigt wird, in der Regel, wenn das zugehörige Dialogfeld zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="9d517-129">The brush must be destroyed by a call to the [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) function when it is no longer needed, typically when the associated dialog box is destroyed.</span></span>


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a><span data-ttu-id="9d517-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d517-130">Requirements</span></span>



| <span data-ttu-id="9d517-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d517-131">Requirement</span></span> | <span data-ttu-id="9d517-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9d517-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d517-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d517-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9d517-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d517-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9d517-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d517-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9d517-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d517-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9d517-137">Header</span><span class="sxs-lookup"><span data-stu-id="9d517-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d517-138"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9d517-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d517-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d517-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d517-140">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9d517-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9d517-141">**WM \_ ctlcolorbtn**</span><span class="sxs-lookup"><span data-stu-id="9d517-141">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="9d517-142">**WM \_ ctlcoloredit**</span><span class="sxs-lookup"><span data-stu-id="9d517-142">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="9d517-143">**WM \_ ctlcolorlistbox**</span><span class="sxs-lookup"><span data-stu-id="9d517-143">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="9d517-144">**WM \_ ctlcolorscrollbar**</span><span class="sxs-lookup"><span data-stu-id="9d517-144">**WM\_CTLCOLORSCROLLBAR**</span></span>](wm-ctlcolorscrollbar.md)
</dt> <dt>

<span data-ttu-id="9d517-145">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9d517-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9d517-146">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9d517-146">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9d517-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="9d517-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="9d517-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="9d517-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="9d517-149">**WM \_ ctlcolordlg**</span><span class="sxs-lookup"><span data-stu-id="9d517-149">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

