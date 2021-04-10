---
title: EN_IMECHANGE Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuer Elements, dass der IME-Konvertierungs Status geändert wurde.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- Windows-Steuerelemente für EN_IMECHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040641"
---
# <a name="en_imechange-notification-code"></a><span data-ttu-id="456aa-104">EN \_ ImeChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="456aa-104">EN\_IMECHANGE notification code</span></span>

<span data-ttu-id="456aa-105">Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuer Elements, dass der IME-Konvertierungs Status geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="456aa-105">Notifies a rich edit control's parent that the IME conversion status has changed.</span></span> <span data-ttu-id="456aa-106">Dieser Benachrichtigungs Code ist *nur* für Versionen des Betriebssystems in der asiatischen Sprache verfügbar.</span><span class="sxs-lookup"><span data-stu-id="456aa-106">This notification code is available *only* for Asian-language versions of the operating system.</span></span> <span data-ttu-id="456aa-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.</span><span class="sxs-lookup"><span data-stu-id="456aa-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="456aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="456aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456aa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="456aa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="456aa-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Rich Edit-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="456aa-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="456aa-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="456aa-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="456aa-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="456aa-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="456aa-113">Handle für das Rich Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="456aa-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456aa-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="456aa-114">Return value</span></span>

<span data-ttu-id="456aa-115">Dieser Benachrichtigungs Code gibt NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="456aa-115">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="456aa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="456aa-116">Remarks</span></span>

<span data-ttu-id="456aa-117">Um \_ ImeChange-Benachrichtigungs Codes zu erhalten, geben Sie [**ENM \_ ImeChange**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="456aa-117">To receive EN\_IMECHANGE notification codes, specify [**ENM\_IMECHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="456aa-118">Dieser Benachrichtigungs Code wird nur in der asiatischen Version von Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="456aa-118">This notification code is only supported in the Asian version of Rich Edit 1.0.</span></span> <span data-ttu-id="456aa-119">Sie wird in späteren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="456aa-119">It is not supported in later versions.</span></span> <span data-ttu-id="456aa-120">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="456aa-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="456aa-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="456aa-121">Requirements</span></span>



| <span data-ttu-id="456aa-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="456aa-122">Requirement</span></span> | <span data-ttu-id="456aa-123">Wert</span><span class="sxs-lookup"><span data-stu-id="456aa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="456aa-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="456aa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="456aa-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="456aa-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="456aa-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="456aa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="456aa-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="456aa-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="456aa-128">Header</span><span class="sxs-lookup"><span data-stu-id="456aa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="456aa-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="456aa-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="456aa-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="456aa-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="456aa-131">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="456aa-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="456aa-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="456aa-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="456aa-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="456aa-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="456aa-134">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="456aa-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

