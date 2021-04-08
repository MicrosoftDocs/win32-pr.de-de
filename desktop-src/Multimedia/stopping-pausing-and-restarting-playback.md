---
title: Beenden, anhalten und erneutes Starten der Wiedergabe
description: Beenden, anhalten und erneutes Starten der Wiedergabe
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- Wellenform-Audiodatei, Beenden der Wiedergabe
- Waveform-Audioschnittstelle, Beenden der Wiedergabe
- Wiedergabe von Waveform-Audiodateien, Beenden der Wiedergabe
- Wellenform-Audiodatei, Anhalten der Wiedergabe
- Waveform-Audioschnittstelle, Anhalten der Wiedergabe
- Wiedergabe von Waveform-Audiodateien, Anhalten der Wiedergabe
- Wellenform-Audiodatei, Wiedergabe neu starten
- Waveform-Audioschnittstelle, Neustarten der Wiedergabe
- Wiedergeben von Waveform-Audiodateien, erneutes Starten der Wiedergabe
- waveoutpause-Funktion
- Wave-Set-Funktion
- Wave-Start-Funktion
- Beenden der Waveform-Audiowiedergabe
- Anhalten der Waveform-Audiowiedergabe
- Neustarten der Waveform-Audiowiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101491"
---
# <a name="stopping-pausing-and-restarting-playback"></a><span data-ttu-id="4ca1e-118">Beenden, anhalten und erneutes Starten der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="4ca1e-118">Stopping, Pausing, and Restarting Playback</span></span>

<span data-ttu-id="4ca1e-119">Sie können die Wiedergabe anhalten oder anhalten, während das Wellenform-Audioformat abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-119">You can stop or pause playback while waveform audio is playing.</span></span> <span data-ttu-id="4ca1e-120">Nachdem die Wiedergabe angehalten wurde, können Sie Sie neu starten.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-120">After playback has been paused, you can restart it.</span></span> <span data-ttu-id="4ca1e-121">Windows stellt die folgenden Funktionen zum Steuern der Waveform-Audiowiedergabe bereit.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-121">Windows provides the following functions for controlling waveform-audio playback.</span></span>



| <span data-ttu-id="4ca1e-122">Funktion</span><span class="sxs-lookup"><span data-stu-id="4ca1e-122">Function</span></span>                                 | <span data-ttu-id="4ca1e-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ca1e-123">Description</span></span>                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ca1e-124">**waveoutpause**</span><span class="sxs-lookup"><span data-stu-id="4ca1e-124">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | <span data-ttu-id="4ca1e-125">Hält die Wiedergabe auf einem Waveform-Audioausgabegerät an.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-125">Pauses playback on a waveform-audio output device.</span></span>                                          |
| [<span data-ttu-id="4ca1e-126">**waveeinset**</span><span class="sxs-lookup"><span data-stu-id="4ca1e-126">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | <span data-ttu-id="4ca1e-127">Beendet die Wiedergabe auf einem Waveform-Audioausgabegerät und markiert alle ausstehenden Datenblöcke als abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-127">Stops playback on a waveform-audio output device and marks all pending data blocks as done.</span></span> |
| [<span data-ttu-id="4ca1e-128">**wavestartstart**</span><span class="sxs-lookup"><span data-stu-id="4ca1e-128">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | <span data-ttu-id="4ca1e-129">Nimmt die Wiedergabe auf einem angehaltenen Waveform-Audioausgabegerät wieder auf.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-129">Resumes playback on a paused waveform-audio output device.</span></span>                                  |



 

<span data-ttu-id="4ca1e-130">Das Anhalten eines Waveform-Audiogeräts mithilfe von [**waveoutpause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) ist möglicherweise nicht sofort. der Treiber kann das Abspielen des aktuellen Blocks beenden, bevor die Wiedergabe angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-130">Pausing a waveform-audio device by using [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) might not be instantaneous; the driver may finish playing the current block before pausing playback.</span></span>

<span data-ttu-id="4ca1e-131">Im allgemeinen beginnt, sobald der erste Waveform-audiodatenblock mithilfe der [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) -Funktion gesendet wird, das Waveform-Audiogerät zu spielen.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-131">Generally, as soon as the first waveform-audio data block is sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function, the waveform-audio device begins playing.</span></span> <span data-ttu-id="4ca1e-132">Wenn Sie nicht möchten, dass der Sound sofort abgespielt wird, rufen Sie **waveoutpause** auf, bevor Sie **waveOutWrite** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-132">If you do not want the sound to start playing immediately, call **waveOutPause** before calling **waveOutWrite**.</span></span> <span data-ttu-id="4ca1e-133">Wenn Sie dann mit der Wiedergabe von Waveform-Audiodaten beginnen möchten, wenden Sie [**wavestartstart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)an.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-133">Then, when you want to begin playing waveform-audio data, call [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span></span>

<span data-ttu-id="4ca1e-134">Sie können **wavestartstart** nicht verwenden, um ein Gerät neu zu starten, das mit [**waveeinset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)beendet wurde. Sie müssen " **waveOutWrite** " verwenden, um den ersten Datenblock zu senden, um die Wiedergabe auf dem Gerät wieder aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="4ca1e-134">You cannot use **waveOutRestart** to restart a device that has been stopped with [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); you must use **waveOutWrite** to send the first data block to resume playback on the device.</span></span>

 

 