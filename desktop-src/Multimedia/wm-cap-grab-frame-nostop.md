---
title: WM_CAP_GRAB_FRAME_NOSTOP Meldung (VFW. h)
description: Die " \_ WM \_ Cap \_ Capture Frame" \_ -nostoppmeldung füllt den Frame Puffer mit einem einzelnen unkomprimierten Frame aus dem Erfassungsgerät und zeigt ihn an.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859140"
---
# <a name="wm_cap_grab_frame_nostop-message"></a><span data-ttu-id="0bf19-104">WM- \_ Obergrenze für \_ \_ Abbild \_ Ende-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0bf19-104">WM\_CAP\_GRAB\_FRAME\_NOSTOP message</span></span>

<span data-ttu-id="0bf19-105">Die " **WM Cap Capture Frame"- \_ \_ \_ \_ nostoppmeldung** füllt den Frame Puffer mit einem einzelnen unkomprimierten Frame aus dem Erfassungsgerät und zeigt ihn an.</span><span class="sxs-lookup"><span data-stu-id="0bf19-105">The **WM\_CAP\_GRAB\_FRAME\_NOSTOP** message fills the frame buffer with a single uncompressed frame from the capture device and displays it.</span></span> <span data-ttu-id="0bf19-106">Anders als bei der " [**WM Cap"- \_ \_ \_ Abbild**](wm-cap-grab-frame.md) Nachricht wird der Zustand der Überlagerung oder der Vorschau nicht von dieser Nachricht geändert.</span><span class="sxs-lookup"><span data-stu-id="0bf19-106">Unlike with the [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message, the state of overlay or preview is not altered by this message.</span></span> <span data-ttu-id="0bf19-107">Sie können diese Nachricht explizit oder mithilfe des [**capgrabframenostop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="0bf19-107">You can send this message explicitly or by using the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="0bf19-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bf19-108">Return Value</span></span>

<span data-ttu-id="0bf19-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0bf19-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bf19-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bf19-110">Remarks</span></span>

<span data-ttu-id="0bf19-111">Weitere Informationen zum Installieren von Rückruf Funktionen finden Sie in den Rückruf-und [**WM- \_ Cap \_ - \_ \_**](wm-cap-set-callback-frame.md) Set-Rückruf [**\_ \_ \_ \_ Fehlern**](wm-cap-set-callback-error.md) .</span><span class="sxs-lookup"><span data-stu-id="0bf19-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf19-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bf19-112">Requirements</span></span>



| <span data-ttu-id="0bf19-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bf19-113">Requirement</span></span> | <span data-ttu-id="0bf19-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0bf19-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0bf19-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0bf19-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf19-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bf19-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0bf19-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0bf19-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf19-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bf19-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0bf19-119">Header</span><span class="sxs-lookup"><span data-stu-id="0bf19-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bf19-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bf19-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf19-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bf19-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf19-122">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="0bf19-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0bf19-123">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="0bf19-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





