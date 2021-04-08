---
title: EN_SETFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn ein Bearbeitungs Steuerelement den Tastaturfokus erhält. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung.
ms.assetid: 482d2afa-4e21-4f3f-bdf4-6966b34cc3c4
keywords:
- Windows-Steuerelemente für EN_SETFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cb96482f0e42669658dde3a39637e3c2311619
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743033"
---
# <a name="en_setfocus-notification-code"></a><span data-ttu-id="abef0-105">EN \_ SetFocus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="abef0-105">EN\_SETFOCUS notification code</span></span>

<span data-ttu-id="abef0-106">Wird gesendet, wenn ein Bearbeitungs Steuerelement den Tastaturfokus erhält.</span><span class="sxs-lookup"><span data-stu-id="abef0-106">Sent when an edit control receives the keyboard focus.</span></span> <span data-ttu-id="abef0-107">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="abef0-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="abef0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="abef0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abef0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abef0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abef0-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="abef0-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="abef0-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="abef0-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="abef0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abef0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abef0-113">Ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="abef0-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abef0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abef0-114">Remarks</span></span>

<span data-ttu-id="abef0-115">Das übergeordnete Fenster empfängt immer eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung für dieses Ereignis, es ist jedoch keine Benachrichtigungs Maske erforderlich, die mit EM-Einstellungs- [**\_ Maske**](em-seteventmask.md)gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="abef0-115">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="abef0-116">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abef0-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="abef0-117">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="abef0-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abef0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abef0-118">Requirements</span></span>



| <span data-ttu-id="abef0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abef0-119">Requirement</span></span> | <span data-ttu-id="abef0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="abef0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abef0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abef0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="abef0-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abef0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="abef0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abef0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="abef0-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abef0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="abef0-125">Header</span><span class="sxs-lookup"><span data-stu-id="abef0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="abef0-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="abef0-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abef0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abef0-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="abef0-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="abef0-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="abef0-129">EN \_ killfokus</span><span class="sxs-lookup"><span data-stu-id="abef0-129">EN\_KILLFOCUS</span></span>](en-killfocus.md)
</dt> <dt>

<span data-ttu-id="abef0-130">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="abef0-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="abef0-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="abef0-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

