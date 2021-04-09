---
title: EN_KILLFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn ein Bearbeitungs Steuerelement den Tastaturfokus verliert. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- Windows-Steuerelemente für EN_KILLFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c30c037d985647f50b93402667832b18b3897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858686"
---
# <a name="en_killfocus-notification-code"></a><span data-ttu-id="9c3bf-105">EN \_ killfocus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="9c3bf-105">EN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="9c3bf-106">Wird gesendet, wenn ein Bearbeitungs Steuerelement den Tastaturfokus verliert.</span><span class="sxs-lookup"><span data-stu-id="9c3bf-106">Sent when an edit control loses the keyboard focus.</span></span> <span data-ttu-id="9c3bf-107">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="9c3bf-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="9c3bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c3bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c3bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c3bf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c3bf-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="9c3bf-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="9c3bf-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="9c3bf-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9c3bf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c3bf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c3bf-113">Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9c3bf-113">Handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c3bf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c3bf-114">Remarks</span></span>

<span data-ttu-id="9c3bf-115">Das übergeordnete Fenster empfängt immer eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung für dieses Ereignis, es ist jedoch keine Benachrichtigungs Maske erforderlich, die mit EM-Einstellungs- [**\_ Maske**](em-seteventmask.md)gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9c3bf-115">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="9c3bf-116">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c3bf-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="9c3bf-117">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="9c3bf-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c3bf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c3bf-118">Requirements</span></span>



| <span data-ttu-id="9c3bf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c3bf-119">Requirement</span></span> | <span data-ttu-id="9c3bf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9c3bf-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c3bf-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c3bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9c3bf-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c3bf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9c3bf-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c3bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9c3bf-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c3bf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c3bf-125">Header</span><span class="sxs-lookup"><span data-stu-id="9c3bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c3bf-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9c3bf-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c3bf-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c3bf-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c3bf-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9c3bf-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c3bf-129">**EN \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="9c3bf-129">**EN\_SETFOCUS**</span></span>](en-setfocus.md)
</dt> <dt>

<span data-ttu-id="9c3bf-130">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9c3bf-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9c3bf-131">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="9c3bf-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

