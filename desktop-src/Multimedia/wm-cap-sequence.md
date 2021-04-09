---
title: WM_CAP_SEQUENCE Meldung (VFW. h)
description: Die WM \_ \_ -Cap-Sequenz Nachricht initiiert Streaming-Video und Audioerfassung in eine Datei. Sie können diese Nachricht explizit oder mithilfe des capcapturesequence-Makros senden.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956611"
---
# <a name="wm_cap_sequence-message"></a><span data-ttu-id="08f2b-105">WM- \_ Abdeckungs \_ Sequenz Nachricht</span><span class="sxs-lookup"><span data-stu-id="08f2b-105">WM\_CAP\_SEQUENCE message</span></span>

<span data-ttu-id="08f2b-106">Die **WM- \_ Cap- \_ Sequenz** Nachricht initiiert Streaming-Video und Audioerfassung in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="08f2b-106">The **WM\_CAP\_SEQUENCE** message initiates streaming video and audio capture to a file.</span></span> <span data-ttu-id="08f2b-107">Sie können diese Nachricht explizit oder mithilfe des [**capcapturesequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="08f2b-107">You can send this message explicitly or by using the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro.</span></span>


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="08f2b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08f2b-108">Return Value</span></span>

<span data-ttu-id="08f2b-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="08f2b-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="08f2b-110">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="08f2b-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="08f2b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08f2b-111">Remarks</span></span>

<span data-ttu-id="08f2b-112">Wenn Sie die Parameter, die die streamingerfassung steuern, ändern möchten, verwenden Sie vor dem Start der Erfassung die [**\_ \_ Set \_ Sequence- \_ Setup**](wm-cap-set-sequence-setup.md) Nachricht.</span><span class="sxs-lookup"><span data-stu-id="08f2b-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="08f2b-113">Standardmäßig lässt das Erfassungsfenster nicht zu, dass andere Anwendungen während der Erfassung weiter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08f2b-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="08f2b-114">Um dies zu überschreiben, legen Sie entweder den **fyield** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) auf **true** fest, oder installieren Sie eine Yield-Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="08f2b-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="08f2b-115">Während der streamingerfassung kann das Erfassungsfenster optional Benachrichtigungen für bestimmte Arten von Bedingungen an Ihre Anwendung ausgeben.</span><span class="sxs-lookup"><span data-stu-id="08f2b-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="08f2b-116">Verwenden Sie zum Installieren von Rückruf Prozeduren für diese Benachrichtigungen die folgenden Meldungen:</span><span class="sxs-lookup"><span data-stu-id="08f2b-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="08f2b-117">**Rückruf Fehler bei WM-Abdeckung \_ \_ festgelegt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08f2b-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="08f2b-118">**Rückruf Status der WM- \_ Obergrenze \_ festlegen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08f2b-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="08f2b-119">**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**</span><span class="sxs-lookup"><span data-stu-id="08f2b-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="08f2b-120">**WM- \_ Abdeckungs \_ Satz \_ Rückruf \_ Videostream**</span><span class="sxs-lookup"><span data-stu-id="08f2b-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="08f2b-121">**WM- \_ Cap- \_ Satz \_ Rückruf \_ WaveStream**</span><span class="sxs-lookup"><span data-stu-id="08f2b-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="08f2b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08f2b-122">Requirements</span></span>



| <span data-ttu-id="08f2b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08f2b-123">Requirement</span></span> | <span data-ttu-id="08f2b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="08f2b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08f2b-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08f2b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="08f2b-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08f2b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="08f2b-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08f2b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="08f2b-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08f2b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="08f2b-129">Header</span><span class="sxs-lookup"><span data-stu-id="08f2b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="08f2b-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="08f2b-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f2b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08f2b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f2b-132">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="08f2b-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="08f2b-133">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="08f2b-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





