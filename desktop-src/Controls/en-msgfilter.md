---
title: EN_MSGFILTER Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements über ein Tastatur-oder Maus Ereignis im-Steuerelement. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- Windows-Steuerelemente für EN_MSGFILTER Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103929"
---
# <a name="en_msgfilter-notification-code"></a><span data-ttu-id="d534e-105">EN \_ msgfilter-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d534e-105">EN\_MSGFILTER notification code</span></span>

<span data-ttu-id="d534e-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements über ein Tastatur-oder Maus Ereignis im-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d534e-106">Notifies a rich edit control's parent window of a keyboard or mouse event in the control.</span></span> <span data-ttu-id="d534e-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="d534e-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d534e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d534e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d534e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d534e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d534e-110">Eine [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) -Struktur, die Informationen über die Tastatur-oder Maus Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="d534e-110">A [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure containing information about the keyboard or mouse message.</span></span> <span data-ttu-id="d534e-111">Wenn das übergeordnete Fenster diese Struktur ändert und einen Wert ungleich 0 (null) zurückgibt, wird die geänderte Nachricht anstelle der ursprünglichen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d534e-111">If the parent window modifies this structure and returns a nonzero value, the modified message is processed instead of the original one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d534e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d534e-112">Return value</span></span>

<span data-ttu-id="d534e-113">Gibt NULL zurück, wenn das Steuerelement das Tastatur-oder Maus Ereignis verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="d534e-113">Return zero if the control should process the keyboard or mouse event.</span></span>

<span data-ttu-id="d534e-114">Gibt einen Wert ungleich 0 zurück, wenn das Steuerelement das Tastatur-oder Maus Ereignis ignorieren soll.</span><span class="sxs-lookup"><span data-stu-id="d534e-114">Return nonzero if the control should ignore the keyboard or mouse event.</span></span>

## <a name="remarks"></a><span data-ttu-id="d534e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d534e-115">Remarks</span></span>

<span data-ttu-id="d534e-116">Zum Empfangen von en- \_ msgfilter-Benachrichtigungs Codes für Ereignisse geben Sie mindestens eines der folgenden Flags in der Maske an, die mit der [**EM \_**](em-seteventmask.md) -Nachricht "-Abmeldung gesendet" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d534e-116">To receive EN\_MSGFILTER notification codes for events, specify one or more of the following flags in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>



| <span data-ttu-id="d534e-117">Flag</span><span class="sxs-lookup"><span data-stu-id="d534e-117">Flag</span></span>                                                                             | <span data-ttu-id="d534e-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d534e-118">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d534e-119">**"ESM"- \_ KEYEVENTs**</span><span class="sxs-lookup"><span data-stu-id="d534e-119">**ENM\_KEYEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)       | <span data-ttu-id="d534e-120">Zum Empfangen von Benachrichtigungs Codes für Tastatur Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="d534e-120">To receive notification codes for keyboard events.</span></span>     |
| [<span data-ttu-id="d534e-121">**"en"- \_ mouevent-Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="d534e-121">**ENM\_MOUSEEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)   | <span data-ttu-id="d534e-122">Zum Empfangen von Benachrichtigungs Codes für Mausereignisse.</span><span class="sxs-lookup"><span data-stu-id="d534e-122">To receive notification codes for mouse events.</span></span>        |
| [<span data-ttu-id="d534e-123">**\_SM-scrollevents**</span><span class="sxs-lookup"><span data-stu-id="d534e-123">**ENM\_SCROLLEVENTS**</span></span>](rich-edit-control-event-mask-flags.md) | <span data-ttu-id="d534e-124">Zum Empfangen von Benachrichtigungs Codes für ein Mausrad Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d534e-124">To receive notification codes for a mouse wheel event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d534e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d534e-125">Requirements</span></span>



| <span data-ttu-id="d534e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d534e-126">Requirement</span></span> | <span data-ttu-id="d534e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d534e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d534e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d534e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d534e-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d534e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d534e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d534e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d534e-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d534e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d534e-132">Header</span><span class="sxs-lookup"><span data-stu-id="d534e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d534e-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d534e-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d534e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d534e-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="d534e-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d534e-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d534e-136">**Msgfilter**</span><span class="sxs-lookup"><span data-stu-id="d534e-136">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[<span data-ttu-id="d534e-137">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="d534e-137">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





