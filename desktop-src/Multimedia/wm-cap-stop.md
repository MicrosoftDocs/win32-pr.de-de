---
title: WM_CAP_STOP Meldung (VFW. h)
description: Die WM- \_ Obergrenze für das \_ Beenden hält den Aufzeichnungs Vorgang an. Sie können diese Nachricht explizit oder mithilfe des capcapturestoppt-Makros senden.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743537"
---
# <a name="wm_cap_stop-message"></a><span data-ttu-id="209b6-105">Meldung zum Abbrechen der WM- \_ Begrenzung \_</span><span class="sxs-lookup"><span data-stu-id="209b6-105">WM\_CAP\_STOP message</span></span>

<span data-ttu-id="209b6-106">Die **WM- \_ Obergrenze \_** für das Beenden hält den Aufzeichnungs Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="209b6-106">The **WM\_CAP\_STOP** message stops the capture operation.</span></span> <span data-ttu-id="209b6-107">Sie können diese Nachricht explizit oder mithilfe des [**capcapturestoppt**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="209b6-107">You can send this message explicitly or by using the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro.</span></span>

<span data-ttu-id="209b6-108">In Schritt Frame Erfassung werden die Bilddaten, die vor dem Senden dieser Nachricht erfasst wurden, in der Erfassungs Datei aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="209b6-108">In step frame capture, the image data that was collected before this message was sent is retained in the capture file.</span></span> <span data-ttu-id="209b6-109">Eine entsprechende Dauer von Audiodaten wird auch in der Erfassungs Datei aufbewahrt, wenn die Audioerfassung aktiviert war.</span><span class="sxs-lookup"><span data-stu-id="209b6-109">An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.</span></span>


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="209b6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="209b6-110">Return Value</span></span>

<span data-ttu-id="209b6-111">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="209b6-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="209b6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="209b6-112">Remarks</span></span>

<span data-ttu-id="209b6-113">Der Aufzeichnungs Vorgang muss durchführen, um diese Meldung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="209b6-113">The capture operation must yield to use this message.</span></span> <span data-ttu-id="209b6-114">Verwenden Sie die Abbruch Meldung "WM Cap", um den aktuellen Aufzeichnungs Vorgang [**\_ \_ abzubrechen**](wm-cap-abort.md) .</span><span class="sxs-lookup"><span data-stu-id="209b6-114">Use the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message to abandon the current capture operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="209b6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="209b6-115">Requirements</span></span>



| <span data-ttu-id="209b6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="209b6-116">Requirement</span></span> | <span data-ttu-id="209b6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="209b6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="209b6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="209b6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="209b6-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="209b6-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="209b6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="209b6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="209b6-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="209b6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="209b6-122">Header</span><span class="sxs-lookup"><span data-stu-id="209b6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="209b6-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="209b6-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="209b6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="209b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209b6-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="209b6-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="209b6-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="209b6-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





