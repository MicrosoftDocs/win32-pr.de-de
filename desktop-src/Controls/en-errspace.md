---
title: EN_ERRSPACE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn ein Bearbeitungs Steuerelement nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung.
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- Windows-Steuerelemente für EN_ERRSPACE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b100811741ee5c5f6bf53eb49ff05b118de3c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858687"
---
# <a name="en_errspace-notification-code"></a><span data-ttu-id="0fdf4-105">EN \_ errspace-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="0fdf4-105">EN\_ERRSPACE notification code</span></span>

<span data-ttu-id="0fdf4-106">Wird gesendet, wenn ein Bearbeitungs Steuerelement nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0fdf4-106">Sent when an edit control cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="0fdf4-107">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="0fdf4-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0fdf4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fdf4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fdf4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fdf4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fdf4-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="0fdf4-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="0fdf4-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="0fdf4-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0fdf4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fdf4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fdf4-113">Ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0fdf4-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fdf4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fdf4-114">Remarks</span></span>

<span data-ttu-id="0fdf4-115">Das übergeordnete Fenster erhält immer eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung für dieses Ereignis. es ist keine Benachrichtigungs Maske erforderlich, die mit der EM-Nachricht " [**\_ tventmask**](em-seteventmask.md) " gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fdf4-115">The parent window will always get a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event; it does not require a notification mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="0fdf4-116">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0fdf4-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="0fdf4-117">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="0fdf4-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fdf4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fdf4-118">Requirements</span></span>



| <span data-ttu-id="0fdf4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fdf4-119">Requirement</span></span> | <span data-ttu-id="0fdf4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0fdf4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdf4-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fdf4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0fdf4-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fdf4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0fdf4-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fdf4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0fdf4-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fdf4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0fdf4-125">Header</span><span class="sxs-lookup"><span data-stu-id="0fdf4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fdf4-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0fdf4-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fdf4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fdf4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fdf4-128">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="0fdf4-128">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

