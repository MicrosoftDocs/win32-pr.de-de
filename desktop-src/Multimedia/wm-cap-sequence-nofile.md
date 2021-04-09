---
title: WM_CAP_SEQUENCE_NOFILE Meldung (VFW. h)
description: Die "WM \_ Cap \_ Sequence NoFile"- \_ Meldung initiiert die Streaming-Video Erfassung, ohne Daten in eine Datei zu schreiben. Sie können diese Nachricht explizit oder mithilfe des capcapturesequencenofile-Makros senden.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a08f470989b8000e9757c1cb81924b875b5303
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103027"
---
# <a name="wm_cap_sequence_nofile-message"></a><span data-ttu-id="faeb0-105">WM- \_ Abdeckungs \_ Sequenz- \_ NoFile-Nachricht</span><span class="sxs-lookup"><span data-stu-id="faeb0-105">WM\_CAP\_SEQUENCE\_NOFILE message</span></span>

<span data-ttu-id="faeb0-106">Die " **WM \_ Cap \_ Sequence \_ NoFile** "-Meldung initiiert die Streaming-Video Erfassung, ohne Daten in eine Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="faeb0-106">The **WM\_CAP\_SEQUENCE\_NOFILE** message initiates streaming video capture without writing data to a file.</span></span> <span data-ttu-id="faeb0-107">Sie können diese Nachricht explizit oder mithilfe des [**capcapturesequencenofile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="faeb0-107">You can send this message explicitly or by using the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro.</span></span>


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="faeb0-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="faeb0-108">Return Value</span></span>

<span data-ttu-id="faeb0-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="faeb0-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="faeb0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faeb0-110">Remarks</span></span>

<span data-ttu-id="faeb0-111">Diese Meldung ist hilfreich in Verbindung mit Videostream-oder Waveform-Audiodatenstrom-Rückruf Funktionen, mit denen Ihre Anwendung die Video-und Audiodaten direkt verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="faeb0-111">This message is useful in conjunction with video stream or waveform-audio stream callback functions that let your application use the video and audio data directly.</span></span>

<span data-ttu-id="faeb0-112">Wenn Sie die Parameter, die die streamingerfassung steuern, ändern möchten, verwenden Sie vor dem Start der Erfassung die [**\_ \_ Set \_ Sequence- \_ Setup**](wm-cap-set-sequence-setup.md) Nachricht.</span><span class="sxs-lookup"><span data-stu-id="faeb0-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="faeb0-113">Standardmäßig lässt das Erfassungsfenster nicht zu, dass andere Anwendungen während der Erfassung weiter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="faeb0-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="faeb0-114">Um dies zu überschreiben, legen Sie entweder den **fyield** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) auf **true** fest, oder installieren Sie eine Yield-Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="faeb0-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="faeb0-115">Während der streamingerfassung kann das Erfassungsfenster optional Benachrichtigungen für bestimmte Arten von Bedingungen an Ihre Anwendung ausgeben.</span><span class="sxs-lookup"><span data-stu-id="faeb0-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="faeb0-116">Verwenden Sie zum Installieren von Rückruf Prozeduren für diese Benachrichtigungen die folgenden Meldungen:</span><span class="sxs-lookup"><span data-stu-id="faeb0-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="faeb0-117">**Rückruf Fehler bei WM-Abdeckung \_ \_ festgelegt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faeb0-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="faeb0-118">**Rückruf Status der WM- \_ Obergrenze \_ festlegen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faeb0-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="faeb0-119">**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**</span><span class="sxs-lookup"><span data-stu-id="faeb0-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="faeb0-120">**WM- \_ Abdeckungs \_ Satz \_ Rückruf \_ Videostream**</span><span class="sxs-lookup"><span data-stu-id="faeb0-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="faeb0-121">**WM- \_ Cap- \_ Satz \_ Rückruf \_ WaveStream**</span><span class="sxs-lookup"><span data-stu-id="faeb0-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="faeb0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faeb0-122">Requirements</span></span>



| <span data-ttu-id="faeb0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faeb0-123">Requirement</span></span> | <span data-ttu-id="faeb0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="faeb0-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="faeb0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faeb0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="faeb0-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faeb0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="faeb0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faeb0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="faeb0-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faeb0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="faeb0-129">Header</span><span class="sxs-lookup"><span data-stu-id="faeb0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="faeb0-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="faeb0-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faeb0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faeb0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faeb0-132">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="faeb0-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="faeb0-133">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="faeb0-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





