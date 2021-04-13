---
title: EN_MAXTEXT Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn die aktuelle Text Einfügung die angegebene Anzahl von Zeichen für das Bearbeitungs Steuerelement überschritten hat.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- Windows-Steuerelemente für EN_MAXTEXT Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518659"
---
# <a name="en_maxtext-notification-code"></a><span data-ttu-id="2b06d-104">EN \_ maxtext-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2b06d-104">EN\_MAXTEXT notification code</span></span>

<span data-ttu-id="2b06d-105">Wird gesendet, wenn die aktuelle Text Einfügung die angegebene Anzahl von Zeichen für das Bearbeitungs Steuerelement überschritten hat.</span><span class="sxs-lookup"><span data-stu-id="2b06d-105">Sent when the current text insertion has exceeded the specified number of characters for the edit control.</span></span> <span data-ttu-id="2b06d-106">Die Text Einfügung wurde abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="2b06d-106">The text insertion has been truncated.</span></span>

<span data-ttu-id="2b06d-107">Dieser Benachrichtigungs Code wird auch gesendet, wenn ein Bearbeitungs Steuerelement nicht den " [**es \_ autohscroll**](edit-control-styles.md) "-Stil hat und die Anzahl der einzufügenden Zeichen die Breite des Bearbeitungs Steuer Elements überschreiten würde.</span><span class="sxs-lookup"><span data-stu-id="2b06d-107">This notification code is also sent when an edit control does not have the [**ES\_AUTOHSCROLL**](edit-control-styles.md) style and the number of characters to be inserted would exceed the width of the edit control.</span></span>

<span data-ttu-id="2b06d-108">Dieser Benachrichtigungs Code wird auch gesendet, wenn ein Bearbeitungs Steuerelement nicht den " [**es \_ autovscroll**](edit-control-styles.md) "-Stil hat und die Gesamtanzahl der Zeilen, die sich aus einer Text Einfügung ergeben, die Höhe des Bearbeitungs Steuer Elements überschreiten würde.</span><span class="sxs-lookup"><span data-stu-id="2b06d-108">This notification code is also sent when an edit control does not have the [**ES\_AUTOVSCROLL**](edit-control-styles.md) style and the total number of lines resulting from a text insertion would exceed the height of the edit control.</span></span>

<span data-ttu-id="2b06d-109">Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="2b06d-109">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="2b06d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b06d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b06d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b06d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b06d-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="2b06d-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="2b06d-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="2b06d-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2b06d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b06d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b06d-115">Ein Handle für das Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2b06d-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b06d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b06d-116">Remarks</span></span>

<span data-ttu-id="2b06d-117">Das übergeordnete Fenster empfängt immer eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung für dieses Ereignis, es ist jedoch keine Benachrichtigungs Maske erforderlich, die mit EM-Einstellungs- [**\_ Maske**](em-seteventmask.md)gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2b06d-117">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="2b06d-118">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b06d-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2b06d-119">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="2b06d-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b06d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b06d-120">Requirements</span></span>



| <span data-ttu-id="2b06d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b06d-121">Requirement</span></span> | <span data-ttu-id="2b06d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2b06d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b06d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b06d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b06d-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b06d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b06d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b06d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b06d-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b06d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b06d-127">Header</span><span class="sxs-lookup"><span data-stu-id="2b06d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b06d-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2b06d-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b06d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b06d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b06d-130">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="2b06d-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

