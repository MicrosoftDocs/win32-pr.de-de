---
title: Avicap-Rückruf Funktionen
description: Avicap-Rückruf Funktionen
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Avicap-Klasse, Rückruf Funktionen
- Avicap-Rückruf Funktionen, Informationen zu
- WM_CAP_SET_CALLBACK_CAPCONTROL Meldung
- WM_CAP_SET_CALLBACK_ERROR Meldung
- WM_CAP_SET_CALLBACK_FRAME Meldung
- WM_CAP_SET_CALLBACK_STATUS Meldung
- WM_CAP_SET_CALLBACK_VIDEOSTREAM Meldung
- WM_CAP_SET_CALLBACK_WAVESTREAM Meldung
- WM_CAP_SET_CALLBACK_YIELD Meldung
- capsetcallbackoncapcontrol-Makro
- capsetcallbackonerrormacro
- capsetcallbackonframe-Makro
- capsetcallbackonstatus-Makro
- capsetcallbackonvideostream-Makro
- capsetcallbackonwavestream-Makro
- capsetcallbackonyield-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948049"
---
# <a name="avicap-callback-functions"></a><span data-ttu-id="cd408-119">Avicap-Rückruf Funktionen</span><span class="sxs-lookup"><span data-stu-id="cd408-119">AVICap Callback Functions</span></span>

<span data-ttu-id="cd408-120">Die Anwendung kann Rückruf Funktionen mit einem Aufzeichnungs Fenster registrieren, damit die Anwendung benachrichtigt wird, wenn sich der Status ändert, wenn Fehler auftreten, wenn Video Frame-und Audiopuffer verfügbar werden und während der streamingerfassung eine Rendite erzielt wird.</span><span class="sxs-lookup"><span data-stu-id="cd408-120">Your application can register callback functions with a capture window to have it notify your application when the status changes, when errors occur, when video frame and audio buffers become available, and to yield during streaming capture.</span></span> <span data-ttu-id="cd408-121">Die Rückruffunktion wird in den folgenden Meldungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cd408-121">The following messages set the callback function.</span></span>



| <span data-ttu-id="cd408-122">`Message`</span><span class="sxs-lookup"><span data-stu-id="cd408-122">Message</span></span>                                                                        | <span data-ttu-id="cd408-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd408-123">Description</span></span>                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd408-124">**WM- \_ Cap- \_ Satz Rückruf ( \_ \_ capcontrol)**</span><span class="sxs-lookup"><span data-stu-id="cd408-124">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)   | <span data-ttu-id="cd408-125">Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, um das Starten und Beenden der Erfassung präzise zu steuern.</span><span class="sxs-lookup"><span data-stu-id="cd408-125">Specifies the callback function in the application called to give precise control over capture start and end.</span></span> <span data-ttu-id="cd408-126">Sie können auch das " [**capsetcallbackoncapcontrol**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) "-Makro verwenden, um diese Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="cd408-126">You can also use the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro to send this message.</span></span>                   |
| [<span data-ttu-id="cd408-127">**Rückruf Fehler bei WM-Abdeckung \_ \_ festgelegt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd408-127">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)             | <span data-ttu-id="cd408-128">Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="cd408-128">Specifies the callback function in the application called when an error occurs.</span></span> <span data-ttu-id="cd408-129">Sie können auch das [**capsetcallbackonerror**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) -Makro verwenden, um diese Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="cd408-129">You can also use the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro to send this message.</span></span>                                                           |
| [<span data-ttu-id="cd408-130">**\_ \_ \_ Rückruf \_ Rahmen für WM-Cap-Satz**</span><span class="sxs-lookup"><span data-stu-id="cd408-130">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)             | <span data-ttu-id="cd408-131">Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn Vorschau Rahmen aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="cd408-131">Specifies the callback function in the application called when preview frames are captured.</span></span> <span data-ttu-id="cd408-132">Sie können auch das " [**capsetcallbackonframe**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) "-Makro verwenden, um diese Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="cd408-132">You can also use the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro to send this message.</span></span>                                               |
| [<span data-ttu-id="cd408-133">**Rückruf Status der WM- \_ Obergrenze \_ festlegen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd408-133">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)           | <span data-ttu-id="cd408-134">Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn sich der Status ändert.</span><span class="sxs-lookup"><span data-stu-id="cd408-134">Specifies the callback function in the application called when the status changes.</span></span> <span data-ttu-id="cd408-135">Sie können auch das " [**capsetcallbackonstatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) "-Makro verwenden, um diese Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="cd408-135">You can also use the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro to send this message.</span></span>                                                      |
| [<span data-ttu-id="cd408-136">**WM- \_ Abdeckungs \_ Satz \_ Rückruf \_ Videostream**</span><span class="sxs-lookup"><span data-stu-id="cd408-136">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md) | <span data-ttu-id="cd408-137">Gibt die Rückruffunktion in der Anwendung an, die während der streamingerfassung aufgerufen wird, wenn ein neuer Video Puffer verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="cd408-137">Specifies the callback function in the application called during streaming capture when a new video buffer becomes available.</span></span> <span data-ttu-id="cd408-138">Sie können auch das " [**capsetcallbackonvideostream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) "-Makro verwenden, um diese Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="cd408-138">You can also use the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro to send this message.</span></span> |
| [<span data-ttu-id="cd408-139">**WM- \_ Cap- \_ Satz \_ Rückruf \_ WaveStream**</span><span class="sxs-lookup"><span data-stu-id="cd408-139">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)   | <span data-ttu-id="cd408-140">Gibt die Rückruffunktion in der Anwendung an, die während der streamingerfassung aufgerufen wird, wenn ein neuer Audiopuffer verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="cd408-140">Specifies the callback function in the application called during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="cd408-141">Sie können auch das " [**capsetcallbackonwavestream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) "-Makro verwenden, um diese Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="cd408-141">You can also use the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro to send this message.</span></span>   |
| [<span data-ttu-id="cd408-142">**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**</span><span class="sxs-lookup"><span data-stu-id="cd408-142">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)             | <span data-ttu-id="cd408-143">Gibt die Rückruffunktion in der Anwendung an, die aufgerufen wird, wenn Sie während der streamingerfassung</span><span class="sxs-lookup"><span data-stu-id="cd408-143">Specifies the callback function in the application called when yielding during streaming capture.</span></span> <span data-ttu-id="cd408-144">Sie können auch das [**capsetcallbackonyield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) -Makro verwenden, um diese Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="cd408-144">You can also use the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro to send this message.</span></span>                                         |



 

<span data-ttu-id="cd408-145">In den folgenden Themen werden die verschiedenen Rückruf Funktionen, die an die Funktionen gesendeten Benachrichtigungen und deren Verwendungszwecke beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cd408-145">The following topics describe the different callback functions, the notifications sent to the functions, and their uses.</span></span>

 

 




