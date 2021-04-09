---
title: WM_CAP_EDIT_COPY Meldung (VFW. h)
description: Die " \_ WM \_ \_ -Cap-Kopier Nachricht bearbeiten" kopiert den Inhalt des Video Frame Puffers und der zugehörigen Palette in die Zwischenablage. Sie können diese Nachricht explizit oder mithilfe des capeditcopy-Makros senden.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104702"
---
# <a name="wm_cap_edit_copy-message"></a><span data-ttu-id="4b39f-105">\_Meldung zum \_ Bearbeiten der WM-Abdeckung \_</span><span class="sxs-lookup"><span data-stu-id="4b39f-105">WM\_CAP\_EDIT\_COPY message</span></span>

<span data-ttu-id="4b39f-106">Die " **WM-Cap- \_ \_ \_ Kopier Nachricht bearbeiten** " kopiert den Inhalt des Video Frame Puffers und der zugehörigen Palette in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="4b39f-106">The **WM\_CAP\_EDIT\_COPY** message copies the contents of the video frame buffer and associated palette to the clipboard.</span></span> <span data-ttu-id="4b39f-107">Sie können diese Nachricht explizit oder mithilfe des [**capeditcopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="4b39f-107">You can send this message explicitly or by using the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro.</span></span>


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="4b39f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b39f-108">Return Value</span></span>

<span data-ttu-id="4b39f-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="4b39f-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b39f-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b39f-110">Requirements</span></span>



| <span data-ttu-id="4b39f-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b39f-111">Requirement</span></span> | <span data-ttu-id="4b39f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4b39f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4b39f-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b39f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4b39f-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b39f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4b39f-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b39f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4b39f-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b39f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4b39f-117">Header</span><span class="sxs-lookup"><span data-stu-id="4b39f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b39f-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b39f-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b39f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b39f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b39f-120">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="4b39f-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4b39f-121">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="4b39f-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





