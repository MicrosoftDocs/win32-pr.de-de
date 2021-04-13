---
title: MIDI-Referenz
description: MIDI-Referenz
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Windows Multimedia, Digital Instrumentation Digital Interface (MIDI)
- Multimedia, Digital Instrumentation Digital Interface (MIDI)
- Multimedia-Audiodatei, Digital Instrumentation Digital Interface (MIDI)
- Audioschnittstelle (Digital Instrumentation Digital Interface, MIDI)
- Windows Multimedia, MIDI-Referenz
- Multimedia, MIDI-Referenz
- Multimedia-Audiodatei, MIDI-Referenz
- Audiodatei, MIDI-Referenz
- Digital Instrumentation Digital Interface (MIDI), Referenz
- MIDI (Digital Interface Digital Interface), Referenz
- Referenz für "MIDI", Informationen zu
- MIDI-Referenz, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390263"
---
# <a name="midi-reference"></a><span data-ttu-id="4ce03-115">MIDI-Referenz</span><span class="sxs-lookup"><span data-stu-id="4ce03-115">MIDI Reference</span></span>

<span data-ttu-id="4ce03-116">In diesem Abschnitt werden die Funktionen, Makros, Meldungen und Strukturen beschrieben, die der digitalen Schnittstelle (Digital Instrumentation Digital Interface, MIDI) zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4ce03-116">This section describes the functions, macros, messages, and structures associated with the Musical Instrument Digital Interface (MIDI).</span></span> <span data-ttu-id="4ce03-117">Diese Elemente werden wie folgt gruppiert.</span><span class="sxs-lookup"><span data-stu-id="4ce03-117">These elements are grouped as follows.</span></span>

## <a name="allocating-and-managing-buffers"></a><span data-ttu-id="4ce03-118">Zuordnen und Verwalten von Puffern</span><span class="sxs-lookup"><span data-stu-id="4ce03-118">Allocating and Managing Buffers</span></span>

-   [<span data-ttu-id="4ce03-119">**Midihdr**</span><span class="sxs-lookup"><span data-stu-id="4ce03-119">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [<span data-ttu-id="4ce03-120">**midiinaddbuffer**</span><span class="sxs-lookup"><span data-stu-id="4ce03-120">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [<span data-ttu-id="4ce03-121">**midiinprepareheader**</span><span class="sxs-lookup"><span data-stu-id="4ce03-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [<span data-ttu-id="4ce03-122">**midiinunprepareheader**</span><span class="sxs-lookup"><span data-stu-id="4ce03-122">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [<span data-ttu-id="4ce03-123">**midioutprepareheader**</span><span class="sxs-lookup"><span data-stu-id="4ce03-123">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [<span data-ttu-id="4ce03-124">**midioutunprepareheader**</span><span class="sxs-lookup"><span data-stu-id="4ce03-124">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a><span data-ttu-id="4ce03-125">Rückruffunktionen</span><span class="sxs-lookup"><span data-stu-id="4ce03-125">Callback Functions</span></span>

-   <span data-ttu-id="4ce03-126">[**Midiinproc**](/previous-versions//dd798460(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ce03-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span></span>
-   <span data-ttu-id="4ce03-127">[**Midioutproc**](/previous-versions//dd798478(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ce03-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="4ce03-128">Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="4ce03-128">Device Capabilities</span></span>

-   [<span data-ttu-id="4ce03-129">**Midiincaps**</span><span class="sxs-lookup"><span data-stu-id="4ce03-129">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [<span data-ttu-id="4ce03-130">**midiingetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="4ce03-130">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [<span data-ttu-id="4ce03-131">**midiingetid**</span><span class="sxs-lookup"><span data-stu-id="4ce03-131">**midiInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [<span data-ttu-id="4ce03-132">**midiingetnumentvs**</span><span class="sxs-lookup"><span data-stu-id="4ce03-132">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [<span data-ttu-id="4ce03-133">**Midioutcaps**</span><span class="sxs-lookup"><span data-stu-id="4ce03-133">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [<span data-ttu-id="4ce03-134">**midioutgetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="4ce03-134">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [<span data-ttu-id="4ce03-135">**midioutgetid**</span><span class="sxs-lookup"><span data-stu-id="4ce03-135">**midiOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [<span data-ttu-id="4ce03-136">**midioutgetnumentvs**</span><span class="sxs-lookup"><span data-stu-id="4ce03-136">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [<span data-ttu-id="4ce03-137">**Midistraumbuffver**</span><span class="sxs-lookup"><span data-stu-id="4ce03-137">**MIDISTRMBUFFVER**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a><span data-ttu-id="4ce03-138">Fehlerverarbeitung</span><span class="sxs-lookup"><span data-stu-id="4ce03-138">Error Processing</span></span>

-   [<span data-ttu-id="4ce03-139">**midiingeterrortext**</span><span class="sxs-lookup"><span data-stu-id="4ce03-139">**midiInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [<span data-ttu-id="4ce03-140">**midioutgeterrortext**</span><span class="sxs-lookup"><span data-stu-id="4ce03-140">**midiOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [<span data-ttu-id="4ce03-141">**MIM- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="4ce03-141">**MIM\_ERROR**</span></span>](mim-error.md)
-   [<span data-ttu-id="4ce03-142">**MIM \_ longerror**</span><span class="sxs-lookup"><span data-stu-id="4ce03-142">**MIM\_LONGERROR**</span></span>](mim-longerror.md)
-   [<span data-ttu-id="4ce03-143">**MM \_ MIM- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="4ce03-143">**MM\_MIM\_ERROR**</span></span>](mm-mim-error.md)
-   [<span data-ttu-id="4ce03-144">**MM \_ MIM \_ longerror**</span><span class="sxs-lookup"><span data-stu-id="4ce03-144">**MM\_MIM\_LONGERROR**</span></span>](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a><span data-ttu-id="4ce03-145">Verwalten von MIDI-Streams</span><span class="sxs-lookup"><span data-stu-id="4ce03-145">Managing MIDI Streams</span></span>

-   [<span data-ttu-id="4ce03-146">**midistreamclose**</span><span class="sxs-lookup"><span data-stu-id="4ce03-146">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [<span data-ttu-id="4ce03-147">**midistreamopen**</span><span class="sxs-lookup"><span data-stu-id="4ce03-147">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [<span data-ttu-id="4ce03-148">**midistreamout**</span><span class="sxs-lookup"><span data-stu-id="4ce03-148">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="4ce03-149">**midistreampause**</span><span class="sxs-lookup"><span data-stu-id="4ce03-149">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="4ce03-150">**midistreamposition**</span><span class="sxs-lookup"><span data-stu-id="4ce03-150">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [<span data-ttu-id="4ce03-151">**midistreamproperty**</span><span class="sxs-lookup"><span data-stu-id="4ce03-151">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [<span data-ttu-id="4ce03-152">**midistreamrestart**</span><span class="sxs-lookup"><span data-stu-id="4ce03-152">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="4ce03-153">**midistreamstoppt**</span><span class="sxs-lookup"><span data-stu-id="4ce03-153">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a><span data-ttu-id="4ce03-154">Öffnen und Schließen von Geräten</span><span class="sxs-lookup"><span data-stu-id="4ce03-154">Opening and Closing Devices</span></span>

-   [<span data-ttu-id="4ce03-155">**midiinclose**</span><span class="sxs-lookup"><span data-stu-id="4ce03-155">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [<span data-ttu-id="4ce03-156">**midiinopen**</span><span class="sxs-lookup"><span data-stu-id="4ce03-156">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [<span data-ttu-id="4ce03-157">**midioutclose**</span><span class="sxs-lookup"><span data-stu-id="4ce03-157">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [<span data-ttu-id="4ce03-158">**midioutopen**</span><span class="sxs-lookup"><span data-stu-id="4ce03-158">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [<span data-ttu-id="4ce03-159">**MIM \_ Close**</span><span class="sxs-lookup"><span data-stu-id="4ce03-159">**MIM\_CLOSE**</span></span>](mim-close.md)
-   [<span data-ttu-id="4ce03-160">**MIM \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="4ce03-160">**MIM\_OPEN**</span></span>](mim-open.md)
-   [<span data-ttu-id="4ce03-161">**MM \_ MIM \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="4ce03-161">**MM\_MIM\_CLOSE**</span></span>](mm-mim-close.md)
-   [<span data-ttu-id="4ce03-162">**MM \_ MIM \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="4ce03-162">**MM\_MIM\_OPEN**</span></span>](mm-mim-open.md)
-   [<span data-ttu-id="4ce03-163">**Schließen von mm \_ MOM \_**</span><span class="sxs-lookup"><span data-stu-id="4ce03-163">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md)
-   [<span data-ttu-id="4ce03-164">**MM \_ MOM \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="4ce03-164">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)
-   [<span data-ttu-id="4ce03-165">**MOM \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="4ce03-165">**MOM\_CLOSE**</span></span>](mom-close.md)
-   [<span data-ttu-id="4ce03-166">**MOM \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="4ce03-166">**MOM\_OPEN**</span></span>](mom-open.md)

## <a name="output-devices"></a><span data-ttu-id="4ce03-167">Ausgabegeräte</span><span class="sxs-lookup"><span data-stu-id="4ce03-167">Output Devices</span></span>

-   [<span data-ttu-id="4ce03-168">Keyarray</span><span class="sxs-lookup"><span data-stu-id="4ce03-168">KEYARRAY</span></span>](keyarray.md)
-   [<span data-ttu-id="4ce03-169">**midioutcachedrumpatches**</span><span class="sxs-lookup"><span data-stu-id="4ce03-169">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [<span data-ttu-id="4ce03-170">**midioutcachepatches**</span><span class="sxs-lookup"><span data-stu-id="4ce03-170">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [<span data-ttu-id="4ce03-171">**midioutgetvolume**</span><span class="sxs-lookup"><span data-stu-id="4ce03-171">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [<span data-ttu-id="4ce03-172">**midioutsetvolume**</span><span class="sxs-lookup"><span data-stu-id="4ce03-172">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [<span data-ttu-id="4ce03-173">Patcharray</span><span class="sxs-lookup"><span data-stu-id="4ce03-173">PATCHARRAY</span></span>](patcharray.md)

## <a name="playing-a-message-or-messages"></a><span data-ttu-id="4ce03-174">Wiedergeben einer Nachricht oder Nachrichten</span><span class="sxs-lookup"><span data-stu-id="4ce03-174">Playing a Message or Messages</span></span>

-   [<span data-ttu-id="4ce03-175">**mevt \_ EventParser**</span><span class="sxs-lookup"><span data-stu-id="4ce03-175">**MEVT\_EVENTPARM**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [<span data-ttu-id="4ce03-176">**mevt \_ eventType**</span><span class="sxs-lookup"><span data-stu-id="4ce03-176">**MEVT\_EVENTTYPE**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [<span data-ttu-id="4ce03-177">**MidiEvent**</span><span class="sxs-lookup"><span data-stu-id="4ce03-177">**MIDIEVENT**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [<span data-ttu-id="4ce03-178">**midioutlongmsg**</span><span class="sxs-lookup"><span data-stu-id="4ce03-178">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [<span data-ttu-id="4ce03-179">**falsch einwählsatz**</span><span class="sxs-lookup"><span data-stu-id="4ce03-179">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [<span data-ttu-id="4ce03-180">**midioutshortmsg**</span><span class="sxs-lookup"><span data-stu-id="4ce03-180">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [<span data-ttu-id="4ce03-181">**midistreamout**</span><span class="sxs-lookup"><span data-stu-id="4ce03-181">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="4ce03-182">**midistreampause**</span><span class="sxs-lookup"><span data-stu-id="4ce03-182">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="4ce03-183">**midistreamrestart**</span><span class="sxs-lookup"><span data-stu-id="4ce03-183">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="4ce03-184">**midistreamstoppt**</span><span class="sxs-lookup"><span data-stu-id="4ce03-184">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [<span data-ttu-id="4ce03-185">**MM- \_ MOM \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="4ce03-185">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)
-   [<span data-ttu-id="4ce03-186">**MM \_ MOM \_ positioncb**</span><span class="sxs-lookup"><span data-stu-id="4ce03-186">**MM\_MOM\_POSITIONCB**</span></span>](mm-mom-positioncb.md)
-   [<span data-ttu-id="4ce03-187">**MOM \_ abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="4ce03-187">**MOM\_DONE**</span></span>](mom-done.md)
-   [<span data-ttu-id="4ce03-188">**MOM- \_ positioncb**</span><span class="sxs-lookup"><span data-stu-id="4ce03-188">**MOM\_POSITIONCB**</span></span>](mom-positioncb.md)

## <a name="recording"></a><span data-ttu-id="4ce03-189">Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="4ce03-189">Recording</span></span>

-   [<span data-ttu-id="4ce03-190">**midiconnect**</span><span class="sxs-lookup"><span data-stu-id="4ce03-190">**midiConnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [<span data-ttu-id="4ce03-191">**mididisconnect**</span><span class="sxs-lookup"><span data-stu-id="4ce03-191">**midiDisconnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [<span data-ttu-id="4ce03-192">**midiinreset**</span><span class="sxs-lookup"><span data-stu-id="4ce03-192">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [<span data-ttu-id="4ce03-193">**midiinstart**</span><span class="sxs-lookup"><span data-stu-id="4ce03-193">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [<span data-ttu-id="4ce03-194">**midiinstop**</span><span class="sxs-lookup"><span data-stu-id="4ce03-194">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [<span data-ttu-id="4ce03-195">**Midiproptempo**</span><span class="sxs-lookup"><span data-stu-id="4ce03-195">**MIDIPROPTEMPO**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [<span data-ttu-id="4ce03-196">**Midiproptimediv**</span><span class="sxs-lookup"><span data-stu-id="4ce03-196">**MIDIPROPTIMEDIV**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [<span data-ttu-id="4ce03-197">**MIM- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="4ce03-197">**MIM\_DATA**</span></span>](mim-data.md)
-   [<span data-ttu-id="4ce03-198">**MIM \_ longdata**</span><span class="sxs-lookup"><span data-stu-id="4ce03-198">**MIM\_LONGDATA**</span></span>](mim-longdata.md)
-   [<span data-ttu-id="4ce03-199">**MIM \_ MoreData**</span><span class="sxs-lookup"><span data-stu-id="4ce03-199">**MIM\_MOREDATA**</span></span>](mim-moredata.md)
-   [<span data-ttu-id="4ce03-200">**MM \_ MIM- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="4ce03-200">**MM\_MIM\_DATA**</span></span>](mm-mim-data.md)
-   [<span data-ttu-id="4ce03-201">**MM \_ MIM \_ MoreData**</span><span class="sxs-lookup"><span data-stu-id="4ce03-201">**MM\_MIM\_MOREDATA**</span></span>](mm-mim-moredata.md)
-   [<span data-ttu-id="4ce03-202">**MM \_ MIM \_ longdata**</span><span class="sxs-lookup"><span data-stu-id="4ce03-202">**MM\_MIM\_LONGDATA**</span></span>](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a><span data-ttu-id="4ce03-203">Senden von Nachrichten an Geräte</span><span class="sxs-lookup"><span data-stu-id="4ce03-203">Sending Messages to Devices</span></span>

-   [<span data-ttu-id="4ce03-204">**midiinmessage**</span><span class="sxs-lookup"><span data-stu-id="4ce03-204">**midiInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [<span data-ttu-id="4ce03-205">**midioutmessage**</span><span class="sxs-lookup"><span data-stu-id="4ce03-205">**midiOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a><span data-ttu-id="4ce03-206">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ce03-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ce03-207">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="4ce03-207">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 