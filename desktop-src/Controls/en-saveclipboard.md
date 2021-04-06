---
title: EN_SAVECLIPBOARD Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster des Rich-Edit-Steuer Elements, dass das-Steuerelement geschlossen wird und die Zwischenablage Informationen enthält. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- Windows-Steuerelemente für EN_SAVECLIPBOARD Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858826"
---
# <a name="en_saveclipboard-notification-code"></a><span data-ttu-id="9de5a-105">EN \_ saveclipboard-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="9de5a-105">EN\_SAVECLIPBOARD notification code</span></span>

<span data-ttu-id="9de5a-106">Benachrichtigt das übergeordnete Fenster des Rich-Edit-Steuer Elements, dass das-Steuerelement geschlossen wird und die Zwischenablage Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="9de5a-106">Notifies the rich edit control's parent window that the control is closing and the clipboard contains information.</span></span> <span data-ttu-id="9de5a-107">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="9de5a-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9de5a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9de5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de5a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9de5a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9de5a-110">Eine [](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) eingefüchende-Struktur, die Informationen zu Zwischenablage Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="9de5a-110">An [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) structure that contains information about clipboard information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de5a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9de5a-111">Return value</span></span>

<span data-ttu-id="9de5a-112">Gibt 0 (null) zurück, wenn die Zwischenablage anderen Anwendungen zur Verfügung gestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9de5a-112">Return zero if the clipboard should be made available to other applications.</span></span>

<span data-ttu-id="9de5a-113">Gibt einen Wert ungleich 0 (null) zurück, wenn die Zwischenablage nicht gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9de5a-113">Return a nonzero value if the clipboard should not be saved.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de5a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9de5a-114">Remarks</span></span>

<span data-ttu-id="9de5a-115">Das übergeordnete Fenster ruft immer eine [**WM \_**](wm-notify.md) -Benachrichtigungs Meldung für dieses Ereignis ab. es ist keine Benachrichtigungs Maske erforderlich, die mit der "em-Einstellungs [**\_ Maske**](em-seteventmask.md)" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9de5a-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9de5a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9de5a-116">Requirements</span></span>



| <span data-ttu-id="9de5a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9de5a-117">Requirement</span></span> | <span data-ttu-id="9de5a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9de5a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9de5a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9de5a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9de5a-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9de5a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9de5a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9de5a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9de5a-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9de5a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9de5a-123">Header</span><span class="sxs-lookup"><span data-stu-id="9de5a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de5a-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de5a-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de5a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9de5a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9de5a-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9de5a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9de5a-127">**""**</span><span class="sxs-lookup"><span data-stu-id="9de5a-127">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





