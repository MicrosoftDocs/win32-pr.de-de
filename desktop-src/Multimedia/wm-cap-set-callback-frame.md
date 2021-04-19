---
title: WM_CAP_SET_CALLBACK_FRAME Meldung (VFW. h)
description: Die \_ Rückruffunktion für den WM-Cap- \_ Satz \_ \_ legt eine Vorschau Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren auf, wenn das Aufzeichnungs Fenster vorschauframes erfasst. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackonframe-Makros senden.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337937"
---
# <a name="wm_cap_set_callback_frame-message"></a><span data-ttu-id="574c9-106">\_ \_ \_ Rückruf \_ Rahmen Nachricht für WM-Cap-Satz</span><span class="sxs-lookup"><span data-stu-id="574c9-106">WM\_CAP\_SET\_CALLBACK\_FRAME message</span></span>

<span data-ttu-id="574c9-107">Die Rückruffunktion für den WM-Cap-Satz legt eine Vorschau Rückruffunktion in der Anwendung **\_ \_ fest \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="574c9-107">The **WM\_CAP\_SET\_CALLBACK\_FRAME** message sets a preview callback function in the application.</span></span> <span data-ttu-id="574c9-108">Avicap ruft dieses Verfahren auf, wenn das Aufzeichnungs Fenster vorschauframes erfasst.</span><span class="sxs-lookup"><span data-stu-id="574c9-108">AVICap calls this procedure when the capture window captures preview frames.</span></span> <span data-ttu-id="574c9-109">Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonframe**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="574c9-109">You can send this message explicitly or by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="574c9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="574c9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="574c9-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*</span><span class="sxs-lookup"><span data-stu-id="574c9-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="574c9-112">Zeiger auf die Vorschau Rückruffunktion vom Typ [**capvideostreamcallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="574c9-112">Pointer to the preview callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="574c9-113">Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Rückruffunktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="574c9-113">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="574c9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="574c9-114">Return Value</span></span>

<span data-ttu-id="574c9-115">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="574c9-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="574c9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="574c9-116">Remarks</span></span>

<span data-ttu-id="574c9-117">Das Erfassungsfenster Ruft die Rückruffunktion auf, bevor Vorschau Frames angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="574c9-117">The capture window calls the callback function before displaying preview frames.</span></span> <span data-ttu-id="574c9-118">Dies ermöglicht es einer Anwendung, den Frame bei Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="574c9-118">This allows an application to modify the frame if desired.</span></span> <span data-ttu-id="574c9-119">Diese Rückruffunktion wird bei der Streaming-Video Erfassung nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="574c9-119">This callback function is not used during streaming video capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="574c9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="574c9-120">Requirements</span></span>



| <span data-ttu-id="574c9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="574c9-121">Requirement</span></span> | <span data-ttu-id="574c9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="574c9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="574c9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="574c9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="574c9-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="574c9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="574c9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="574c9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="574c9-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="574c9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="574c9-127">Header</span><span class="sxs-lookup"><span data-stu-id="574c9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="574c9-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="574c9-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="574c9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="574c9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="574c9-130">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="574c9-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="574c9-131">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="574c9-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





