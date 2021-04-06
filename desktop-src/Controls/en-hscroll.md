---
title: EN_HSCROLL Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf die horizontale Schiebe Leiste eines Bearbeitungs Steuer Elements klickt. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung. Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- Windows-Steuerelemente für EN_HSCROLL Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859007"
---
# <a name="en_hscroll-notification-code"></a><span data-ttu-id="cc90a-106">EN \_ HScroll-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="cc90a-106">EN\_HSCROLL notification code</span></span>

<span data-ttu-id="cc90a-107">Wird gesendet, wenn der Benutzer auf die horizontale Schiebe Leiste eines Bearbeitungs Steuer Elements klickt.</span><span class="sxs-lookup"><span data-stu-id="cc90a-107">Sent when the user clicks an edit control's horizontal scroll bar.</span></span> <span data-ttu-id="cc90a-108">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="cc90a-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="cc90a-109">Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cc90a-109">The parent window is notified before the screen is updated.</span></span>


```C++
EN_HSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="cc90a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc90a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc90a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc90a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc90a-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="cc90a-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="cc90a-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="cc90a-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="cc90a-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc90a-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc90a-115">Ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="cc90a-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc90a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc90a-116">Remarks</span></span>

<span data-ttu-id="cc90a-117">Dieser Benachrichtigungs Code wird für die folgenden Mausereignisse auf der horizontalen Schiebe Leiste gesendet: Klicken Sie auf die Pfeil Schaltfläche, oder klicken Sie auf die Pfeil Schaltfläche und den Ziehpunkt.</span><span class="sxs-lookup"><span data-stu-id="cc90a-117">This notification code is sent for the following mouse events on the horizontal scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="cc90a-118">Der Benachrichtigungs Code wird jedoch nicht gesendet, wenn Sie auf den Ziehpunkt der Bild Lauf Leiste selbst klicken.</span><span class="sxs-lookup"><span data-stu-id="cc90a-118">However, the notification code is not sent when clicking the scroll bar thumb itself.</span></span> <span data-ttu-id="cc90a-119">Der Benachrichtigungs Code wird auch gesendet, wenn ein Tastaturereignis eine Änderung im Ansichts Bereich des Bearbeitungs Steuer Elements bewirkt, z. b. durch Drücken von Start, Ende, Pfeil nach links oder nach rechts.</span><span class="sxs-lookup"><span data-stu-id="cc90a-119">The notification code is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, LEFT ARROW, or RIGHT ARROW.</span></span>

<span data-ttu-id="cc90a-120">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc90a-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="cc90a-121">Geben Sie zum Empfangen von **en \_ HScroll** -Benachrichtigungs Codes [**ENM- \_ Scroll**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Abmeldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc90a-121">To receive **EN\_HSCROLL** notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="cc90a-122">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="cc90a-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc90a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc90a-123">Requirements</span></span>



| <span data-ttu-id="cc90a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc90a-124">Requirement</span></span> | <span data-ttu-id="cc90a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="cc90a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc90a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc90a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cc90a-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc90a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cc90a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc90a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cc90a-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc90a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cc90a-130">Header</span><span class="sxs-lookup"><span data-stu-id="cc90a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc90a-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="cc90a-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc90a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc90a-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc90a-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cc90a-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cc90a-134">EN \_ VScroll</span><span class="sxs-lookup"><span data-stu-id="cc90a-134">EN\_VSCROLL</span></span>](en-vscroll.md)
</dt> <dt>

<span data-ttu-id="cc90a-135">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="cc90a-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cc90a-136">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="cc90a-136">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

