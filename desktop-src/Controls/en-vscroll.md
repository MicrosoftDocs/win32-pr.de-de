---
title: EN_VSCROLL Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf die vertikale Schiebe Leiste eines Bearbeitungs Steuer Elements klickt oder wenn der Benutzer den Mauszeiger über das Bearbeitungs Steuerelement bewegt.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- Windows-Steuerelemente für EN_VSCROLL Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859279"
---
# <a name="en_vscroll-notification-code"></a><span data-ttu-id="c6d4d-104">EN \_ VScroll-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="c6d4d-104">EN\_VSCROLL notification code</span></span>

<span data-ttu-id="c6d4d-105">Wird gesendet, wenn der Benutzer auf die vertikale Schiebe Leiste eines Bearbeitungs Steuer Elements klickt oder wenn der Benutzer den Mauszeiger über das Bearbeitungs Steuerelement bewegt.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-105">Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control.</span></span> <span data-ttu-id="c6d4d-106">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-106">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="c6d4d-107">Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-107">The parent window is notified before the screen is updated.</span></span>


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="c6d4d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6d4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6d4d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6d4d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6d4d-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="c6d4d-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c6d4d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6d4d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6d4d-113">Ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6d4d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6d4d-114">Remarks</span></span>

<span data-ttu-id="c6d4d-115">Diese Meldung wird für die folgenden Mausereignisse auf der vertikalen Schiebe Leiste gesendet: Klicken Sie auf die Pfeil Schaltfläche, oder klicken Sie auf die Pfeil Schaltfläche und den Ziehpunkt.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-115">This message is sent for the following mouse events on the vertical scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="c6d4d-116">Die Meldung wird jedoch nicht gesendet, wenn Sie auf die Schiebe Leiste mit der Maus selbst klicken.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-116">However, the message is not sent when clicking the scroll bar mouse itself.</span></span> <span data-ttu-id="c6d4d-117">Die Meldung wird auch gesendet, wenn ein Tastaturereignis eine Änderung im Ansichts Bereich des Bearbeitungs Steuer Elements bewirkt, z. b. durch Drücken von Start, Ende, Bild-auf, Bild-ab, Pfeil nach oben oder nach-unten-Taste.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-117">The message is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, PAGE UP, PAGE DOWN, UP ARROW, or DOWN ARROW.</span></span>

<span data-ttu-id="c6d4d-118">Das Mausrad ist eine Maus mit einem mittelrad, das einen Bildlauf durchführt.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-118">The mouse wheel is a mouse that has a center wheel that scrolls.</span></span> <span data-ttu-id="c6d4d-119">Weitere Informationen finden Sie unter "das Mausrad" in [etwa Maus Eingaben](/windows/desktop/inputdev/about-mouse-input).</span><span class="sxs-lookup"><span data-stu-id="c6d4d-119">For more information, see "The Mouse Wheel" in [About Mouse Input](/windows/desktop/inputdev/about-mouse-input).</span></span>

<span data-ttu-id="c6d4d-120">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c6d4d-121">Um en \_ VScroll-Benachrichtigungs Codes zu erhalten, geben Sie [**ENM- \_ Scroll**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-121">To receive EN\_VSCROLL notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="c6d4d-122">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="c6d4d-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d4d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6d4d-123">Requirements</span></span>



| <span data-ttu-id="c6d4d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6d4d-124">Requirement</span></span> | <span data-ttu-id="c6d4d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c6d4d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d4d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6d4d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d4d-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6d4d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6d4d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6d4d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d4d-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6d4d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6d4d-130">Header</span><span class="sxs-lookup"><span data-stu-id="c6d4d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6d4d-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c6d4d-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d4d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6d4d-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6d4d-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c6d4d-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6d4d-134">EN \_ HScroll</span><span class="sxs-lookup"><span data-stu-id="c6d4d-134">EN\_HSCROLL</span></span>](en-hscroll.md)
</dt> <dt>

<span data-ttu-id="c6d4d-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c6d4d-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c6d4d-136">Verwenden von Bearbeitungs Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="c6d4d-136">Using Edit Controls</span></span>](using-edit-controls.md)
</dt> <dt>

<span data-ttu-id="c6d4d-137">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c6d4d-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c6d4d-138">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="c6d4d-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

