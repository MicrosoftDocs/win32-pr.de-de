---
title: WM_CAP_SINGLE_FRAME_CLOSE Meldung (VFW. h)
description: Die "WM \_ Cap \_ Single Frame Close"- \_ \_ Nachricht schließt die Erfassungs Datei, die von der Nachricht zum Öffnen des WM-Cap geöffnet wurde \_ \_ \_ \_ . Sie können diese Nachricht explizit oder mithilfe des capcapturesingleframeclose-Makros senden.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743545"
---
# <a name="wm_cap_single_frame_close-message"></a><span data-ttu-id="2d377-105">WM- \_ Cap- \_ Nachricht zum Schließen eines einzelnen \_ Frames \_</span><span class="sxs-lookup"><span data-stu-id="2d377-105">WM\_CAP\_SINGLE\_FRAME\_CLOSE message</span></span>

<span data-ttu-id="2d377-106">Die " **WM \_ Cap \_ Single \_ Frame \_ Close** "-Nachricht schließt die Erfassungs Datei, die von der Nachricht zum [**\_ \_ \_ \_ Öffnen des WM-Cap**](wm-cap-single-frame-open.md) geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="2d377-106">The **WM\_CAP\_SINGLE\_FRAME\_CLOSE** message closes the capture file opened by the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="2d377-107">Sie können diese Nachricht explizit oder mithilfe des [**capcapturesingleframeclose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="2d377-107">You can send this message explicitly or by using the [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="2d377-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d377-108">Return Value</span></span>

<span data-ttu-id="2d377-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="2d377-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d377-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d377-110">Remarks</span></span>

<span data-ttu-id="2d377-111">Weitere Informationen zum Installieren von Rückruf Funktionen finden Sie in den Rückruf-und [**WM- \_ Cap \_ - \_ \_**](wm-cap-set-callback-frame.md) Set-Rückruf [**\_ \_ \_ \_ Fehlern**](wm-cap-set-callback-error.md) .</span><span class="sxs-lookup"><span data-stu-id="2d377-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d377-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d377-112">Requirements</span></span>



| <span data-ttu-id="2d377-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d377-113">Requirement</span></span> | <span data-ttu-id="2d377-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2d377-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2d377-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d377-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2d377-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d377-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2d377-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d377-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2d377-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d377-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2d377-119">Header</span><span class="sxs-lookup"><span data-stu-id="2d377-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d377-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d377-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d377-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d377-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d377-122">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="2d377-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2d377-123">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="2d377-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





