---
title: WM_CAP_GRAB_FRAME Meldung (VFW. h)
description: Die Sende \_ \_ \_ Rahmen Nachricht des WM-Abbilds Ruft einen einzelnen Frame aus dem Erfassungs Treiber ab und zeigt ihn an. Nach der Erfassung sind Overlay und Vorschau deaktiviert. Sie können diese Nachricht explizit oder mithilfe des capgrabframe-Makros senden.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477253"
---
# <a name="wm_cap_grab_frame-message"></a><span data-ttu-id="5752e-106">WM- \_ Abdeckungs \_ \_ Nachricht zum Abbild</span><span class="sxs-lookup"><span data-stu-id="5752e-106">WM\_CAP\_GRAB\_FRAME message</span></span>

<span data-ttu-id="5752e-107">Die Sende Rahmen Nachricht des **WM- \_ \_ \_ Abbilds** Ruft einen einzelnen Frame aus dem Erfassungs Treiber ab und zeigt ihn an.</span><span class="sxs-lookup"><span data-stu-id="5752e-107">The **WM\_CAP\_GRAB\_FRAME** message retrieves and displays a single frame from the capture driver.</span></span> <span data-ttu-id="5752e-108">Nach der Erfassung sind Overlay und Vorschau deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5752e-108">After capture, overlay and preview are disabled.</span></span> <span data-ttu-id="5752e-109">Sie können diese Nachricht explizit oder mithilfe des [**capgrabframe**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="5752e-109">You can send this message explicitly or by using the [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a><span data-ttu-id="5752e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5752e-110">Return Value</span></span>

<span data-ttu-id="5752e-111">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="5752e-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5752e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5752e-112">Remarks</span></span>

<span data-ttu-id="5752e-113">Weitere Informationen zum Installieren von Rückruf Funktionen finden Sie in den Rückruf-und [**WM- \_ Cap \_ - \_ \_**](wm-cap-set-callback-frame.md) Set-Rückruf [**\_ \_ \_ \_ Fehlern**](wm-cap-set-callback-error.md) .</span><span class="sxs-lookup"><span data-stu-id="5752e-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="5752e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5752e-114">Requirements</span></span>



| <span data-ttu-id="5752e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5752e-115">Requirement</span></span> | <span data-ttu-id="5752e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5752e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5752e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5752e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5752e-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5752e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5752e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5752e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5752e-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5752e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5752e-121">Header</span><span class="sxs-lookup"><span data-stu-id="5752e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5752e-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5752e-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5752e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5752e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5752e-124">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="5752e-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5752e-125">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="5752e-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





