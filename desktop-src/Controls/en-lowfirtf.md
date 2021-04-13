---
title: EN_LOWFIRTF Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Microsoft Rich Edit-Steuer Elements, dass ein nicht unterstütztes RTF-Schlüsselwort (Rich Text Format) empfangen wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- Windows-Steuerelemente für EN_LOWFIRTF Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518662"
---
# <a name="en_lowfirtf-notification-code"></a><span data-ttu-id="a725f-105">EN \_ lowfirtf-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a725f-105">EN\_LOWFIRTF notification code</span></span>

<span data-ttu-id="a725f-106">Benachrichtigt das übergeordnete Fenster eines Microsoft Rich Edit-Steuer Elements, dass ein nicht unterstütztes RTF-Schlüsselwort (Rich Text Format) empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a725f-106">Notifies the parent window of a Microsoft Rich Edit control that an unsupported Rich Text Format (RTF) keyword was received.</span></span> <span data-ttu-id="a725f-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="a725f-107">A Rich Edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a725f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a725f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a725f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a725f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a725f-110">Die Struktur von " [**umlowfirtf**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) ".</span><span class="sxs-lookup"><span data-stu-id="a725f-110">The [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a725f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a725f-111">Return value</span></span>

<span data-ttu-id="a725f-112">Dieser Benachrichtigungs Code gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a725f-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a725f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a725f-113">Remarks</span></span>

<span data-ttu-id="a725f-114">Um eine en \_ lowfirtf-Benachrichtigung zu erhalten, geben Sie das ENM \_ lowfirtf-Flag in der mit der [**EM \_ SetEventMask**](em-seteventmask.md) -Nachricht gesendeten Maske an.</span><span class="sxs-lookup"><span data-stu-id="a725f-114">To receive an EN\_LOWFIRTF notification, specify the ENM\_LOWFIRTF flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a725f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a725f-115">Requirements</span></span>



| <span data-ttu-id="a725f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a725f-116">Requirement</span></span> | <span data-ttu-id="a725f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a725f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a725f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a725f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a725f-119">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a725f-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a725f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a725f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a725f-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a725f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a725f-122">Header</span><span class="sxs-lookup"><span data-stu-id="a725f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a725f-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a725f-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a725f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a725f-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="a725f-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a725f-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a725f-126">**"Umlowfirtf"**</span><span class="sxs-lookup"><span data-stu-id="a725f-126">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[<span data-ttu-id="a725f-127">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="a725f-127">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





