---
title: EN_REQUESTRESIZE Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Inhalt des Steuer Elements entweder kleiner oder größer als die Fenstergröße des Steuer Elements ist. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- Windows-Steuerelemente für EN_REQUESTRESIZE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104498"
---
# <a name="en_requestresize-notification-code"></a><span data-ttu-id="8b239-105">EN \_ RequestResize-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8b239-105">EN\_REQUESTRESIZE notification code</span></span>

<span data-ttu-id="8b239-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Inhalt des Steuer Elements entweder kleiner oder größer als die Fenstergröße des Steuer Elements ist.</span><span class="sxs-lookup"><span data-stu-id="8b239-106">Notifies a rich edit control's parent window that the control's contents are either smaller or larger than the control's window size.</span></span> <span data-ttu-id="8b239-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="8b239-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8b239-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b239-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b239-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b239-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b239-110">Eine [**reqresize**](/windows/desktop/api/Richedit/ns-richedit-reqresize) -Struktur, die die angeforderte Größe empfängt.</span><span class="sxs-lookup"><span data-stu-id="8b239-110">A [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure that receives the requested size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b239-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b239-111">Return value</span></span>

<span data-ttu-id="8b239-112">Dieser Benachrichtigungs Code gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8b239-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b239-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b239-113">Remarks</span></span>

<span data-ttu-id="8b239-114">Um das Verhalten eines Rich-Edit-Steuer Elements zu unterstützen, muss das übergeordnete Fenster die Größe des Steuer Elements ändern, wenn es diesen Benachrichtigungs Code empfängt.</span><span class="sxs-lookup"><span data-stu-id="8b239-114">To support the bottomless behavior of a rich edit control, the parent window must resize the control when it receives this notification code.</span></span>

<span data-ttu-id="8b239-115">Zum Empfangen von en \_ RequestResize-Benachrichtigungs Codes geben Sie [**ENM \_ RequestResize**](rich-edit-control-event-mask-flags.md) in der mit der Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) gesendeten Maske an.</span><span class="sxs-lookup"><span data-stu-id="8b239-115">To receive EN\_REQUESTRESIZE notification codes, specify [**ENM\_REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b239-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b239-116">Requirements</span></span>



| <span data-ttu-id="8b239-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b239-117">Requirement</span></span> | <span data-ttu-id="8b239-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8b239-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b239-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b239-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8b239-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b239-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b239-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b239-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8b239-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b239-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b239-123">Header</span><span class="sxs-lookup"><span data-stu-id="8b239-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b239-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b239-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b239-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b239-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b239-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8b239-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b239-127">**Reqresize**</span><span class="sxs-lookup"><span data-stu-id="8b239-127">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[<span data-ttu-id="8b239-128">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="8b239-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





