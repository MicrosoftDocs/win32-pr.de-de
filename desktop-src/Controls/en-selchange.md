---
title: EN_SELCHANGE Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass sich die aktuelle Auswahl geändert hat. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- Windows-Steuerelemente für EN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743032"
---
# <a name="en_selchange-notification-code"></a><span data-ttu-id="d2c35-105">EN \_ selChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d2c35-105">EN\_SELCHANGE notification code</span></span>

<span data-ttu-id="d2c35-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass sich die aktuelle Auswahl geändert hat.</span><span class="sxs-lookup"><span data-stu-id="d2c35-106">Notifies a rich edit control's parent window that the current selection has changed.</span></span> <span data-ttu-id="d2c35-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="d2c35-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d2c35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2c35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c35-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2c35-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2c35-110">Eine [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) -Struktur, die Informationen über die Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="d2c35-110">A [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c35-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2c35-111">Return value</span></span>

<span data-ttu-id="d2c35-112">Dieser Benachrichtigungs Code gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d2c35-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2c35-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2c35-113">Remarks</span></span>

<span data-ttu-id="d2c35-114">Um en \_ selChange-Benachrichtigungs Codes zu erhalten, geben Sie [**ENM \_ selChange**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Abmeldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2c35-114">To receive EN\_SELCHANGE notification codes, specify [**ENM\_SELCHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="d2c35-115">Dieser Benachrichtigungs Code wird gesendet, wenn sich die Position der Einfügemarke ändert und kein Text ausgewählt ist (die Auswahl ist leer).</span><span class="sxs-lookup"><span data-stu-id="d2c35-115">This notification code is sent when the caret position changes and no text is selected (the selection is empty).</span></span> <span data-ttu-id="d2c35-116">Die Position der Einfügemarke kann sich ändern, wenn der Benutzer auf die Maus, die Typen klickt oder eine Pfeiltaste drückt.</span><span class="sxs-lookup"><span data-stu-id="d2c35-116">The caret position can change when the user clicks the mouse, types, or presses an arrow key.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c35-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2c35-117">Requirements</span></span>



| <span data-ttu-id="d2c35-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2c35-118">Requirement</span></span> | <span data-ttu-id="d2c35-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d2c35-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c35-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2c35-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c35-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2c35-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2c35-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2c35-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c35-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2c35-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2c35-124">Header</span><span class="sxs-lookup"><span data-stu-id="d2c35-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c35-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c35-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2c35-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2c35-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2c35-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d2c35-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d2c35-128">**SelChange**</span><span class="sxs-lookup"><span data-stu-id="d2c35-128">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[<span data-ttu-id="d2c35-129">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="d2c35-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





