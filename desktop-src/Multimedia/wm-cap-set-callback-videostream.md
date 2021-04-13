---
title: WM_CAP_SET_CALLBACK_VIDEOSTREAM Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set \_ Callback Videostream"- \_ Meldung legt eine Rückruffunktion in der Anwendung fest.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391544"
---
# <a name="wm_cap_set_callback_videostream-message"></a><span data-ttu-id="5f27a-104">WM- \_ Cap- \_ Rückruf- \_ \_ videostreamnachricht</span><span class="sxs-lookup"><span data-stu-id="5f27a-104">WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM message</span></span>

<span data-ttu-id="5f27a-105">Die " **WM \_ Cap \_ Set \_ Callback \_ Videostream** "-Meldung legt eine Rückruffunktion in der Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="5f27a-105">The **WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="5f27a-106">Avicap ruft dieses Verfahren während der streamingerfassung auf, wenn ein Video Puffer gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="5f27a-106">AVICap calls this procedure during streaming capture when a video buffer is filled.</span></span> <span data-ttu-id="5f27a-107">Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonvideostream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="5f27a-107">You can send this message explicitly or by using the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="5f27a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f27a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f27a-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*</span><span class="sxs-lookup"><span data-stu-id="5f27a-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="5f27a-110">Ein Zeiger auf die videostreamrückruf-Funktion vom Typ [**capvideostreamcallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="5f27a-110">Pointer to the video-stream callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="5f27a-111">Geben Sie **null** für diesen Parameter an, um eine zuvor installierte videostreamrückruf-Funktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f27a-111">Specify **NULL** for this parameter to disable a previously installed video-stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f27a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f27a-112">Return Value</span></span>

<span data-ttu-id="5f27a-113">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f27a-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f27a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f27a-114">Remarks</span></span>

<span data-ttu-id="5f27a-115">Das Aufzeichnungs Fenster Ruft die Rückruffunktion auf, bevor der erfasste Frame auf den Datenträger geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5f27a-115">The capture window calls the callback function before writing the captured frame to disk.</span></span> <span data-ttu-id="5f27a-116">Dies ermöglicht es Anwendungen, den Frame bei Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5f27a-116">This allows applications to modify the frame if desired.</span></span>

<span data-ttu-id="5f27a-117">Wenn eine videostreamrückruf-Funktion für die streamingerfassung verwendet wird, muss die Prozedur vor dem Start der Erfassungs Sitzung installiert werden, und Sie muss für die Dauer der Sitzung aktiviert bleiben.</span><span class="sxs-lookup"><span data-stu-id="5f27a-117">If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="5f27a-118">Sie kann nach Ende der streamingerfassung deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5f27a-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f27a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f27a-119">Requirements</span></span>



| <span data-ttu-id="5f27a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f27a-120">Requirement</span></span> | <span data-ttu-id="5f27a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5f27a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f27a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f27a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5f27a-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f27a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5f27a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f27a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5f27a-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f27a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f27a-126">Header</span><span class="sxs-lookup"><span data-stu-id="5f27a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f27a-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f27a-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f27a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f27a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f27a-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="5f27a-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5f27a-130">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="5f27a-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





