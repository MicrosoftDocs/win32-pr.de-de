---
title: EN_DRAGDROPDONE Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Drag & Drop-Vorgang abgeschlossen wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- Windows-Steuerelemente für EN_DRAGDROPDONE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949465"
---
# <a name="en_dragdropdone-notification-code"></a><span data-ttu-id="0eb39-105">EN \_ dragdropdone-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="0eb39-105">EN\_DRAGDROPDONE notification code</span></span>

<span data-ttu-id="0eb39-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Drag & Drop-Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0eb39-106">Notifies a rich edit control's parent window that the drag-and-drop operation has completed.</span></span> <span data-ttu-id="0eb39-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="0eb39-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0eb39-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0eb39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eb39-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0eb39-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0eb39-110">Eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0eb39-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eb39-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0eb39-111">Return value</span></span>

<span data-ttu-id="0eb39-112">Dieser Benachrichtigungs Code gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0eb39-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eb39-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0eb39-113">Remarks</span></span>

<span data-ttu-id="0eb39-114">Um einen en \_ dragdropdone-Benachrichtigungs Code zu erhalten, geben Sie das [**ENM \_ dragdropdone**](rich-edit-control-event-mask-flags.md) -Flag in der mit der [**EM \_ SetEventMask**](em-seteventmask.md) -Nachricht gesendeten Maske an.</span><span class="sxs-lookup"><span data-stu-id="0eb39-114">To receive an EN\_DRAGDROPDONE notification code, specify the [**ENM\_DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eb39-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0eb39-115">Requirements</span></span>



| <span data-ttu-id="0eb39-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0eb39-116">Requirement</span></span> | <span data-ttu-id="0eb39-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0eb39-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb39-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0eb39-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb39-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0eb39-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0eb39-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0eb39-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb39-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0eb39-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0eb39-122">Header</span><span class="sxs-lookup"><span data-stu-id="0eb39-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eb39-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eb39-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eb39-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eb39-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="0eb39-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0eb39-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0eb39-126">**EM-- \_ einventmask**</span><span class="sxs-lookup"><span data-stu-id="0eb39-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> </dl>

 

 





