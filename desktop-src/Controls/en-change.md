---
title: EN_CHANGE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer eine Aktion durchgeführt hat, die möglicherweise Text in einem Bearbeitungs Steuerelement geändert hat.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- Windows-Steuerelemente für EN_CHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858786"
---
# <a name="en_change-notification-code"></a><span data-ttu-id="2be19-104">EN \_ Änderungs Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2be19-104">EN\_CHANGE notification code</span></span>

<span data-ttu-id="2be19-105">Wird gesendet, wenn der Benutzer eine Aktion durchgeführt hat, die möglicherweise Text in einem Bearbeitungs Steuerelement geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2be19-105">Sent when the user has taken an action that may have altered text in an edit control.</span></span> <span data-ttu-id="2be19-106">Im Gegensatz zum [en \_ Update](en-update.md) -Benachrichtigungs Code wird dieser Benachrichtigungs Code gesendet, nachdem das System den Bildschirm aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="2be19-106">Unlike the [EN\_UPDATE](en-update.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="2be19-107">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="2be19-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="2be19-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2be19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be19-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2be19-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2be19-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="2be19-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="2be19-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="2be19-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2be19-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2be19-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2be19-113">Ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2be19-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2be19-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2be19-114">Remarks</span></span>

<span data-ttu-id="2be19-115">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2be19-115">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2be19-116">Um \_ Änderungs Benachrichtigungs Codes von en zu erhalten, geben Sie [**ENM- \_ Änderung**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2be19-116">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="2be19-117">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="2be19-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="2be19-118">Der \_ Änderungs Benachrichtigungs Code von en wird nicht gesendet, wenn der [**\_ mehrzeilige**](edit-control-styles.md) Stil von es verwendet wird und der Text über [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext)gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2be19-118">The EN\_CHANGE notification code is not sent when the [**ES\_MULTILINE**](edit-control-styles.md) style is used and the text is sent through [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span>

## <a name="requirements"></a><span data-ttu-id="2be19-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2be19-119">Requirements</span></span>



| <span data-ttu-id="2be19-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2be19-120">Requirement</span></span> | <span data-ttu-id="2be19-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2be19-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be19-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2be19-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2be19-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2be19-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2be19-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2be19-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2be19-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2be19-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2be19-126">Header</span><span class="sxs-lookup"><span data-stu-id="2be19-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2be19-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2be19-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be19-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2be19-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2be19-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2be19-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2be19-130">EN \_ Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2be19-130">EN\_UPDATE</span></span>](en-update.md)
</dt> <dt>

<span data-ttu-id="2be19-131">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="2be19-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2be19-132">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="2be19-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

