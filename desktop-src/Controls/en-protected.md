---
title: EN_PROTECTED Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer eine Aktion durchführt, die einen geschützten Textbereich ändert. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- Windows-Steuerelemente für EN_PROTECTED Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476977"
---
# <a name="en_protected-notification-code"></a><span data-ttu-id="4e2fa-105">EN \_ geschützter Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="4e2fa-105">EN\_PROTECTED notification code</span></span>

<span data-ttu-id="4e2fa-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer eine Aktion durchführt, die einen geschützten Textbereich ändert.</span><span class="sxs-lookup"><span data-stu-id="4e2fa-106">Notifies a rich edit control's parent window that the user is taking an action that would change a protected range of text.</span></span> <span data-ttu-id="4e2fa-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="4e2fa-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4e2fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e2fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e2fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e2fa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e2fa-110">Eine [**geschützte**](/windows/desktop/api/Richedit/ns-richedit-enprotected) Struktur, die Informationen über die Meldung enthält, die den Benachrichtigungs Code ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="4e2fa-110">An [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure containing information about the message that triggered the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e2fa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e2fa-111">Return value</span></span>

<span data-ttu-id="4e2fa-112">Gibt 0 (null) zurück, um den Vorgang zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="4e2fa-112">Return zero to allow the operation.</span></span>

<span data-ttu-id="4e2fa-113">Gibt einen Wert ungleich 0 zurück, um den Vorgang zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4e2fa-113">Return a nonzero value to prevent the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e2fa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e2fa-114">Remarks</span></span>

<span data-ttu-id="4e2fa-115">Wenn 0 (null) zurückgegeben wird und die Member " **msg**", " **wParam**" und " **LPARAM** " der [**geschützten**](/windows/desktop/api/Richedit/ns-richedit-enprotected) Struktur geändert werden, verarbeitet das Steuerelement die überarbeitete Nachricht anstelle der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4e2fa-115">If zero is returned and the **msg**, **wParam**, and **lParam** members of the [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure are changed, the control processes the revised message instead of the original message.</span></span>

<span data-ttu-id="4e2fa-116">Um \_ geschützte Benachrichtigungs Codes zu erhalten, geben Sie [**ENM \_ Protected**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4e2fa-116">To receive EN\_PROTECTED notification codes, specify [**ENM\_PROTECTED**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2fa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e2fa-117">Requirements</span></span>



| <span data-ttu-id="4e2fa-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e2fa-118">Requirement</span></span> | <span data-ttu-id="4e2fa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4e2fa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2fa-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e2fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2fa-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e2fa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e2fa-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e2fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2fa-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e2fa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e2fa-124">Header</span><span class="sxs-lookup"><span data-stu-id="4e2fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2fa-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e2fa-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e2fa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e2fa-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e2fa-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="4e2fa-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4e2fa-128">**Geschützt**</span><span class="sxs-lookup"><span data-stu-id="4e2fa-128">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[<span data-ttu-id="4e2fa-129">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="4e2fa-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





