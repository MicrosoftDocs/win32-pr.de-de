---
title: EN_CHANGE (Rich Edit)-Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt das Host Fenster eines fensterlosen Bearbeitungs Steuer Elements, dass eine Änderung aufgetreten ist. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- EN_CHANGE (Rich Edit)-Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949707"
---
# <a name="en_change-rich-edit-notification-code"></a><span data-ttu-id="78edc-105">EN- \_ Änderungs Benachrichtigungs Code (Rich Edit)</span><span class="sxs-lookup"><span data-stu-id="78edc-105">EN\_CHANGE (rich edit) notification code</span></span>

<span data-ttu-id="78edc-106">Benachrichtigt das Host Fenster eines fensterlosen Bearbeitungs Steuer Elements, dass eine Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="78edc-106">Notifies a windowless rich edit control's host window that a change has occurred.</span></span> <span data-ttu-id="78edc-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="78edc-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="78edc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78edc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78edc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78edc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78edc-110">Eine [**changenotify**](/windows/desktop/api/Textserv/ns-textserv-changenotify) -Struktur, die die vorgenommene Änderung angibt.</span><span class="sxs-lookup"><span data-stu-id="78edc-110">A [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) structure specifying the change that was made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78edc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78edc-111">Return value</span></span>

<span data-ttu-id="78edc-112">Dieser Benachrichtigungs Code gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78edc-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78edc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78edc-113">Remarks</span></span>

<span data-ttu-id="78edc-114">Um \_ Änderungs Benachrichtigungs Codes von en zu erhalten, geben Sie [**ENM- \_ Änderung**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="78edc-114">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="78edc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78edc-115">Requirements</span></span>



| <span data-ttu-id="78edc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78edc-116">Requirement</span></span> | <span data-ttu-id="78edc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="78edc-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="78edc-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78edc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78edc-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78edc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="78edc-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78edc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78edc-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78edc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="78edc-122">Header</span><span class="sxs-lookup"><span data-stu-id="78edc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78edc-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="78edc-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78edc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78edc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78edc-125">**Txnotify**</span><span class="sxs-lookup"><span data-stu-id="78edc-125">**TxNotify**</span></span>](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





