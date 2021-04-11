---
title: EN_STOPNOUNDO Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine Aktion aufgetreten ist, für die das-Steuerelement nicht genügend Arbeitsspeicher zuordnen kann Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- Windows-Steuerelemente für EN_STOPNOUNDO Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105548"
---
# <a name="en_stopnoundo-notification-code"></a><span data-ttu-id="6255e-105">EN \_ stopnoundo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="6255e-105">EN\_STOPNOUNDO notification code</span></span>

<span data-ttu-id="6255e-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine Aktion aufgetreten ist, für die das-Steuerelement nicht genügend Arbeitsspeicher zuordnen kann</span><span class="sxs-lookup"><span data-stu-id="6255e-106">Notifies a rich edit control's parent window that an action occurred for which the control cannot allocate enough memory to maintain the undo state.</span></span> <span data-ttu-id="6255e-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="6255e-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6255e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6255e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6255e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6255e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6255e-110">Eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6255e-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6255e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6255e-111">Return value</span></span>

<span data-ttu-id="6255e-112">NULL zurückgeben, um **den** Rückgängigvorgang fortzusetzen</span><span class="sxs-lookup"><span data-stu-id="6255e-112">Return zero to continue the **Undo** operation.</span></span>

<span data-ttu-id="6255e-113">Gibt einen Wert ungleich 0 zurück, um  den Rückgängigvorgang zu verhindern</span><span class="sxs-lookup"><span data-stu-id="6255e-113">Return a nonzero value to stop the **Undo** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6255e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6255e-114">Remarks</span></span>

<span data-ttu-id="6255e-115">Das übergeordnete Fenster ruft immer eine [**WM \_**](wm-notify.md) -Benachrichtigungs Meldung für dieses Ereignis ab. es ist keine Benachrichtigungs Maske erforderlich, die mit der "em-Einstellungs [**\_ Maske**](em-seteventmask.md)" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="6255e-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6255e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6255e-116">Requirements</span></span>



| <span data-ttu-id="6255e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6255e-117">Requirement</span></span> | <span data-ttu-id="6255e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6255e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6255e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6255e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6255e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6255e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6255e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6255e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6255e-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6255e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6255e-123">Header</span><span class="sxs-lookup"><span data-stu-id="6255e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6255e-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6255e-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6255e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6255e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6255e-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6255e-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6255e-127">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="6255e-127">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[<span data-ttu-id="6255e-128">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="6255e-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





