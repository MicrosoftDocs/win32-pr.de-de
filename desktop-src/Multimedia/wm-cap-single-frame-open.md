---
title: WM_CAP_SINGLE_FRAME_OPEN Meldung (VFW. h)
description: Die \_ Meldung zum Öffnen eines einzelnen Frames mit dem WM-Cap \_ \_ \_ öffnet die Erfassungs Datei für die Erfassung mit einem Frame. Alle vorherigen Informationen in der Erfassungs Datei werden überschrieben. Sie können diese Nachricht explizit oder mithilfe des capcapturesingleframeopen-Makros senden.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859249"
---
# <a name="wm_cap_single_frame_open-message"></a><span data-ttu-id="06849-106">WM- \_ Cap- \_ Nachricht zum Öffnen eines einzelnen \_ Frames \_</span><span class="sxs-lookup"><span data-stu-id="06849-106">WM\_CAP\_SINGLE\_FRAME\_OPEN message</span></span>

<span data-ttu-id="06849-107">Die Meldung zum **\_ \_ \_ \_ Öffnen eines einzelnen Frames** mit dem WM-Cap öffnet die Erfassungs Datei für die Erfassung mit einem Frame.</span><span class="sxs-lookup"><span data-stu-id="06849-107">The **WM\_CAP\_SINGLE\_FRAME\_OPEN** message opens the capture file for single-frame capturing.</span></span> <span data-ttu-id="06849-108">Alle vorherigen Informationen in der Erfassungs Datei werden überschrieben.</span><span class="sxs-lookup"><span data-stu-id="06849-108">Any previous information in the capture file is overwritten.</span></span> <span data-ttu-id="06849-109">Sie können diese Nachricht explizit oder mithilfe des [**capcapturesingleframeopen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="06849-109">You can send this message explicitly or by using the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_OPEN 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="06849-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06849-110">Return Value</span></span>

<span data-ttu-id="06849-111">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="06849-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="06849-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06849-112">Remarks</span></span>

<span data-ttu-id="06849-113">Weitere Informationen zum Installieren von Rückruf Funktionen finden Sie in den Rückruf-und [**WM- \_ Cap \_ - \_ \_**](wm-cap-set-callback-frame.md) Set-Rückruf [**\_ \_ \_ \_ Fehlern**](wm-cap-set-callback-error.md) .</span><span class="sxs-lookup"><span data-stu-id="06849-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="06849-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06849-114">Requirements</span></span>



| <span data-ttu-id="06849-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06849-115">Requirement</span></span> | <span data-ttu-id="06849-116">Wert</span><span class="sxs-lookup"><span data-stu-id="06849-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="06849-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06849-117">Minimum supported client</span></span><br/> | <span data-ttu-id="06849-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06849-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="06849-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06849-119">Minimum supported server</span></span><br/> | <span data-ttu-id="06849-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06849-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="06849-121">Header</span><span class="sxs-lookup"><span data-stu-id="06849-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="06849-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="06849-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06849-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06849-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06849-124">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="06849-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="06849-125">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="06849-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





