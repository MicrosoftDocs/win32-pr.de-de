---
title: EN_CORRECTTEXT Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine ordnungsgemäße Syv- \_ Geste aufgetreten ist, sodass das übergeordnete Fenster die Korrektur des Texts abbrechen kann. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- Windows-Steuerelemente für EN_CORRECTTEXT Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102982"
---
# <a name="en_correcttext-notification-code"></a><span data-ttu-id="ea424-105">De \_ correcttext-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ea424-105">EN\_CORRECTTEXT notification code</span></span>

<span data-ttu-id="ea424-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine ordnungsgemäße Syv- \_ Geste aufgetreten ist, sodass das übergeordnete Fenster die Korrektur des Texts abbrechen kann.</span><span class="sxs-lookup"><span data-stu-id="ea424-106">Notifies a rich edit control parent window that a SYV\_CORRECT gesture occurred, giving the parent window a chance to cancel correcting the text.</span></span> <span data-ttu-id="ea424-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="ea424-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ea424-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea424-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea424-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea424-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea424-110">Eine [**encorrecttext**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) -Struktur, die die zu korrigierende Auswahl angibt.</span><span class="sxs-lookup"><span data-stu-id="ea424-110">An [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) structure specifying the selection to be corrected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea424-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea424-111">Return value</span></span>

<span data-ttu-id="ea424-112">Gibt NULL zurück, um die Aktion zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="ea424-112">Return zero to ignore the action.</span></span>

<span data-ttu-id="ea424-113">Gibt einen Wert ungleich 0 zurück, um die Aktion zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ea424-113">Returns a nonzero value to process the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea424-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea424-114">Remarks</span></span>

<span data-ttu-id="ea424-115">Dieser Benachrichtigungs Code wird nur gesendet, wenn die Stift Funktionen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ea424-115">This notification code is sent only if pen capabilities are available.</span></span>

<span data-ttu-id="ea424-116">Geben Sie zum Empfangen von en- \_ korrettext-Benachrichtigungs Codes [**ENM \_ correcttext**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_**](em-seteventmask.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea424-116">To receive EN\_CORRECTTEXT notification codes, specify [**ENM\_CORRECTTEXT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="ea424-117">Der en \_ correcttext-Benachrichtigungs Code wird nur in der Rich Edit-Version 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ea424-117">The EN\_CORRECTTEXT notification code is only supported in rich edit version 1.0.</span></span> <span data-ttu-id="ea424-118">Sie wird in späteren Versionen der Rich-Edit-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ea424-118">It is not supported in later versions of rich edit.</span></span> <span data-ttu-id="ea424-119">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="ea424-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea424-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea424-120">Requirements</span></span>



| <span data-ttu-id="ea424-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea424-121">Requirement</span></span> | <span data-ttu-id="ea424-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ea424-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea424-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea424-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea424-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea424-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea424-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea424-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea424-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea424-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea424-127">Header</span><span class="sxs-lookup"><span data-stu-id="ea424-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea424-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea424-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea424-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea424-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea424-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ea424-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ea424-131">**"Tcorrecttext"**</span><span class="sxs-lookup"><span data-stu-id="ea424-131">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





