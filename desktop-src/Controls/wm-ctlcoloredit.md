---
title: WM_CTLCOLOREDIT Meldung (Winuser. h)
description: Ein Bearbeitungs Steuerelement, das nicht schreibgeschützt oder deaktiviert ist, sendet die WM \_ ctlcoloredit-Nachricht an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- Windows-Steuerelemente für WM_CTLCOLOREDIT Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475111"
---
# <a name="wm_ctlcoloredit-message"></a><span data-ttu-id="d661e-104">\_Ctlcoloredit-Meldung von WM</span><span class="sxs-lookup"><span data-stu-id="d661e-104">WM\_CTLCOLOREDIT message</span></span>

<span data-ttu-id="d661e-105">Ein Bearbeitungs Steuerelement, das nicht schreibgeschützt oder deaktiviert ist, sendet die **WM \_ ctlcoloredit** -Nachricht an das übergeordnete Fenster, wenn das Steuerelement gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d661e-105">An edit control that is not read-only or disabled sends the **WM\_CTLCOLOREDIT** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="d661e-106">Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster den angegebenen Gerätekontext Handle verwenden, um die Text-und Hintergrundfarben des Bearbeitungs Steuer Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d661e-106">By responding to this message, the parent window can use the specified device context handle to set the text and background colors of the edit control.</span></span>


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d661e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d661e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d661e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d661e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d661e-109">Ein Handle für den Gerätekontext für das Bearbeitungs Steuerelement Fenster.</span><span class="sxs-lookup"><span data-stu-id="d661e-109">A handle to the device context for the edit control window.</span></span>

</dd> <dt>

<span data-ttu-id="d661e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d661e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d661e-111">Ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d661e-111">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d661e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d661e-112">Return value</span></span>

<span data-ttu-id="d661e-113">Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie das Handle eines Pinsels zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d661e-113">If an application processes this message, it must return the handle of a brush.</span></span> <span data-ttu-id="d661e-114">Das System verwendet den Pinsel zum Zeichnen des Hintergrunds des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d661e-114">The system uses the brush to paint the background of the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d661e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d661e-115">Remarks</span></span>

<span data-ttu-id="d661e-116">Wenn die Anwendung einen Pinsel zurückgibt, den Sie erstellt hat (z. b. durch die Verwendung [**der Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) [**kreatesolidbrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) " oder "-Funktion"), muss die Anwendung den Pinsel freigeben.</span><span class="sxs-lookup"><span data-stu-id="d661e-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="d661e-117">Wenn die Anwendung einen System Pinsel zurückgibt (z. b. einen, der von der [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) -Funktion oder der [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion abgerufen wurde), muss die Anwendung den Pinsel nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="d661e-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="d661e-118">Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für das Bearbeitungs Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="d661e-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the edit control.</span></span>

<span data-ttu-id="d661e-119">Schreibgeschützte oder deaktivierte Bearbeitungs Steuerelemente senden die **WM- \_ ctlcoloredit** -Nachricht nicht, sondern senden die " [**WM \_ ctlcolorstatic**](wm-ctlcolorstatic.md) "-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d661e-119">Read-only or disabled edit controls do not send the **WM\_CTLCOLOREDIT** message; instead, they send the [**WM\_CTLCOLORSTATIC**](wm-ctlcolorstatic.md) message.</span></span>

<span data-ttu-id="d661e-120">Die **WM- \_ ctlcoloredit** -Nachricht wird nie zwischen Threads gesendet, sondern nur innerhalb desselben Threads.</span><span class="sxs-lookup"><span data-stu-id="d661e-120">The **WM\_CTLCOLOREDIT** message is never sent between threads, it is only sent within the same thread.</span></span>

<span data-ttu-id="d661e-121">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d661e-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="d661e-122">Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d661e-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="d661e-123">Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d661e-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="d661e-124">Umfassende **Bearbeitung:** Diese Meldung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d661e-124">**Rich Edit:** This message is not supported.</span></span> <span data-ttu-id="d661e-125">Um die Hintergrundfarbe für ein Rich-Edit-Steuerelement festzulegen, verwenden Sie die Nachricht [**EM \_ setbkgndcolor**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="d661e-125">To set the background color for a rich edit control, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d661e-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d661e-126">Requirements</span></span>



| <span data-ttu-id="d661e-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d661e-127">Requirement</span></span> | <span data-ttu-id="d661e-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d661e-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d661e-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d661e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d661e-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d661e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d661e-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d661e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d661e-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d661e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d661e-133">Header</span><span class="sxs-lookup"><span data-stu-id="d661e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d661e-134"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d661e-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d661e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d661e-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="d661e-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d661e-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d661e-137">**EM \_ setbkgndcolor**</span><span class="sxs-lookup"><span data-stu-id="d661e-137">**EM\_SETBKGNDCOLOR**</span></span>](em-setbkgndcolor.md)
</dt> <dt>

[<span data-ttu-id="d661e-138">**WM \_ ctlcolorstatic**</span><span class="sxs-lookup"><span data-stu-id="d661e-138">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="d661e-139">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d661e-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d661e-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d661e-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d661e-141">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="d661e-141">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="d661e-142">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="d661e-142">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

