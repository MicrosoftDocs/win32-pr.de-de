---
title: EN_UPDATE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn sich das Bearbeitungs Steuerelement selbst neu zeichnet.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- Windows-Steuerelemente für EN_UPDATE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105549"
---
# <a name="en_update-notification-code"></a><span data-ttu-id="4da15-104">EN \_ Update-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="4da15-104">EN\_UPDATE notification code</span></span>

<span data-ttu-id="4da15-105">Wird gesendet, wenn sich das Bearbeitungs Steuerelement selbst neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="4da15-105">Sent when an edit control is about to redraw itself.</span></span> <span data-ttu-id="4da15-106">Dieser Benachrichtigungs Code wird gesendet, nachdem das Steuerelement den Text formatiert hat, aber bevor der Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4da15-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="4da15-107">Dadurch ist es möglich, ggf. die Größe des Bearbeitungs Steuer Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4da15-107">This makes it possible to resize the edit control window, if necessary.</span></span> <span data-ttu-id="4da15-108">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="4da15-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="4da15-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4da15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da15-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4da15-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4da15-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="4da15-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="4da15-112">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="4da15-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="4da15-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4da15-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4da15-114">Ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="4da15-114">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4da15-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4da15-115">Remarks</span></span>

<span data-ttu-id="4da15-116">**Rich Edit 1,0:** Zum Empfangen von en- \_ Update-Benachrichtigungs Codes geben Sie [**ENM- \_ Update**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4da15-116">**Rich Edit 1.0:** To receive EN\_UPDATE notification codes, specify [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="4da15-117">**Rich Edit 2,0 und höher:** Das Flag zum [**\_ Aktualisieren von SM**](rich-edit-control-event-mask-flags.md) wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4da15-117">**Rich Edit 2.0 and later:** The [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) flag is ignored.</span></span> <span data-ttu-id="4da15-118">Der en \_ Update-Benachrichtigungs Code wird immer empfangen.</span><span class="sxs-lookup"><span data-stu-id="4da15-118">The EN\_UPDATE notification code is always received.</span></span> <span data-ttu-id="4da15-119">Wenn Microsoft Rich Edit 3,0 jedoch Microsoft Rich Edit 1,0 emuliert, müssen Sie zum Empfangen von en \_ Update-Benachrichtigungs Codes das **ENM- \_ Update** in der Maske angeben, die mit der Nachricht [**\_ EM**](em-seteventmask.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4da15-119">However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, to receive EN\_UPDATE notification codes you must specify **ENM\_UPDATE** in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="4da15-120">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="4da15-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4da15-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4da15-121">Requirements</span></span>



| <span data-ttu-id="4da15-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4da15-122">Requirement</span></span> | <span data-ttu-id="4da15-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4da15-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da15-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4da15-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4da15-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4da15-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4da15-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4da15-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4da15-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4da15-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4da15-128">Header</span><span class="sxs-lookup"><span data-stu-id="4da15-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da15-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="4da15-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da15-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4da15-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="4da15-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="4da15-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4da15-132">\_Änderung der Änderung</span><span class="sxs-lookup"><span data-stu-id="4da15-132">EN\_CHANGE</span></span>](en-change.md)
</dt> <dt>

<span data-ttu-id="4da15-133">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="4da15-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4da15-134">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="4da15-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

