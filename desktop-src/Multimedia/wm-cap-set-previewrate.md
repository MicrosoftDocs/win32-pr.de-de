---
title: WM_CAP_SET_PREVIEWRATE Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set \_ previewrate"-Meldung legt die Frame-Anzeige Rate im Vorschaumodus fest. Sie können diese Nachricht explizit oder mithilfe des cappreviewrate-Makros senden.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957134"
---
# <a name="wm_cap_set_previewrate-message"></a><span data-ttu-id="d6499-105">\_ \_ Previewrate-Meldung für WM-Cap-Set \_</span><span class="sxs-lookup"><span data-stu-id="d6499-105">WM\_CAP\_SET\_PREVIEWRATE message</span></span>

<span data-ttu-id="d6499-106">Die " **WM \_ Cap \_ Set \_ previewrate** "-Meldung legt die Frame-Anzeige Rate im Vorschaumodus fest.</span><span class="sxs-lookup"><span data-stu-id="d6499-106">The **WM\_CAP\_SET\_PREVIEWRATE** message sets the frame display rate in preview mode.</span></span> <span data-ttu-id="d6499-107">Sie können diese Nachricht explizit oder mithilfe des [**cappreviewrate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d6499-107">You can send this message explicitly or by using the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro.</span></span>


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="d6499-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6499-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6499-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span><span class="sxs-lookup"><span data-stu-id="d6499-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span></span>
</dt> <dd>

<span data-ttu-id="d6499-110">Rate (in Millisekunden), mit der neue Frames aufgezeichnet und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6499-110">Rate, in milliseconds, at which new frames are captured and displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6499-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6499-111">Return Value</span></span>

<span data-ttu-id="d6499-112">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d6499-112">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6499-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6499-113">Remarks</span></span>

<span data-ttu-id="d6499-114">Im Vorschaumodus werden beträchtliche CPU-Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6499-114">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="d6499-115">Anwendungen können die Vorschau deaktivieren oder die Vorschau Rate verringern, wenn eine andere Anwendung den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="d6499-115">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="d6499-116">Während der Streaming-Video Erfassung hat die Vorschau Aufgabe eine niedrigere Priorität als das Schreiben von Frames auf den Datenträger, und Vorschau Rahmen werden nur angezeigt, wenn keine anderen Puffer zum Schreiben verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d6499-116">During streaming video capture, the previewing task is lower priority than writing frames to disk, and preview frames are displayed only if no other buffers are available for writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6499-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6499-117">Requirements</span></span>



| <span data-ttu-id="d6499-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6499-118">Requirement</span></span> | <span data-ttu-id="d6499-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d6499-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d6499-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6499-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d6499-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6499-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d6499-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6499-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d6499-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6499-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d6499-124">Header</span><span class="sxs-lookup"><span data-stu-id="d6499-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6499-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6499-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6499-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6499-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6499-127">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="d6499-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d6499-128">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="d6499-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





