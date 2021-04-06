---
title: EN_OLEOPFAILED Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine Benutzeraktion für ein Component Object Model (com)-Objekt fehlgeschlagen ist. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- Windows-Steuerelemente für EN_OLEOPFAILED Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 139c51642c8cb6d5efd369cf6b373068604439b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858944"
---
# <a name="en_oleopfailed-notification-code"></a><span data-ttu-id="91572-105">EN \_ oleopfailed-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="91572-105">EN\_OLEOPFAILED notification code</span></span>

<span data-ttu-id="91572-106">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine Benutzeraktion für ein Component Object Model (com)-Objekt fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="91572-106">Notifies a rich edit control's parent window that a user action on a Component Object Model (COM) object has failed.</span></span> <span data-ttu-id="91572-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="91572-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="91572-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="91572-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91572-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91572-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91572-110">Eine " [**finoleopfailed**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) "-Struktur, die Informationen über den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="91572-110">An [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) structure that contains information about the failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91572-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91572-111">Return value</span></span>

<span data-ttu-id="91572-112">Dieser Benachrichtigungs Code gibt NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="91572-112">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="91572-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91572-113">Remarks</span></span>

<span data-ttu-id="91572-114">Das übergeordnete Fenster ruft immer eine [**WM \_**](wm-notify.md) -Benachrichtigungs Meldung für dieses Ereignis ab. es ist keine Benachrichtigungs Maske erforderlich, die mit der "em-Einstellungs [**\_ Maske**](em-seteventmask.md)" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="91572-114">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91572-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91572-115">Requirements</span></span>



| <span data-ttu-id="91572-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91572-116">Requirement</span></span> | <span data-ttu-id="91572-117">Wert</span><span class="sxs-lookup"><span data-stu-id="91572-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91572-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91572-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91572-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91572-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91572-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91572-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91572-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91572-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91572-122">Header</span><span class="sxs-lookup"><span data-stu-id="91572-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91572-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="91572-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91572-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91572-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="91572-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="91572-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91572-126">**"Endfailed"**</span><span class="sxs-lookup"><span data-stu-id="91572-126">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





