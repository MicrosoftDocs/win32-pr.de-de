---
description: Die linemediamode- \_ Konstanten beschreiben Medientypen (oder Modi) einer Kommunikationssitzung oder eines Aufrufes.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: LINEMEDIAMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354706"
---
# <a name="linemediamode_-constants"></a><span data-ttu-id="880b0-103">Linemediamode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="880b0-103">LINEMEDIAMODE\_ Constants</span></span>

<span data-ttu-id="880b0-104">Die **linemediamode \_** -Konstanten beschreiben Medientypen (oder Modi) einer Kommunikationssitzung oder eines Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="880b0-104">The **LINEMEDIAMODE\_** constants describe media types (or modes)of a communications session or call.</span></span>

<dl> <dt>

<span data-ttu-id="880b0-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**linemediamode \_ automatedvoice**</span><span class="sxs-lookup"><span data-stu-id="880b0-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE\_AUTOMATEDVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-106">Beim Anruf wurde Voice Energy erkannt, und die Stimme wird lokal von einer automatisierten Anwendung wie z. b. mit einer antwortenden Computeranwendung behandelt.</span><span class="sxs-lookup"><span data-stu-id="880b0-106">Voice energy was detected on the call, and the voice is locally handled by an automated application such as with an answering machine application.</span></span> <span data-ttu-id="880b0-107">Wenn ein Dienstanbieter bei einem eingehenden Anruf nicht zwischen interaktiver und automatisierter Stimme unterscheiden kann, wird der Anruf als interaktive Stimme gemeldet.</span><span class="sxs-lookup"><span data-stu-id="880b0-107">When a service provider cannot distinguish between interactive and automated voice on an incoming call, it will report the call as interactive voice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**linemediamode \_ datamoder**</span><span class="sxs-lookup"><span data-stu-id="880b0-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE\_DATAMODEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-109">Eine Datenmodem Sitzung für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="880b0-109">A data modem session on the call.</span></span> <span data-ttu-id="880b0-110">Aktuelle Modem Protokolle erfordern, dass die aufgerufene Station den Handshake initiiert.</span><span class="sxs-lookup"><span data-stu-id="880b0-110">Current modem protocols require the called station to initiate the handshake.</span></span> <span data-ttu-id="880b0-111">Für einen eingehenden Datenmodem Anrufe kann die Anwendung normalerweise keine positive Erkennung durchführen.</span><span class="sxs-lookup"><span data-stu-id="880b0-111">For an incoming data modem call, the application can typically make no positive detection.</span></span> <span data-ttu-id="880b0-112">Wie der Dienstanbieter diese Bestimmung trifft, ist seine Wahl.</span><span class="sxs-lookup"><span data-stu-id="880b0-112">How the service provider makes this determination is its choice.</span></span> <span data-ttu-id="880b0-113">So kann z. b. ein Ruhe Zeitraum nur nach dem Beantworten eines eingehenden Aufrufes als Heuristik verwendet werden, um zu entscheiden, dass dies ein Datenmodem Anruf sein könnte.</span><span class="sxs-lookup"><span data-stu-id="880b0-113">For example, a period of silence just after answering an incoming call can be used as a heuristic to decide that this might be a data modem call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**linemediamode \_ ADSI**</span><span class="sxs-lookup"><span data-stu-id="880b0-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE\_ADSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-115">Eine ADSI-Sitzung (Analog Display Services Interface) für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="880b0-115">An ADSI (Analog Display Services Interface) session on the call.</span></span> <span data-ttu-id="880b0-116">ADSI erweitert Sprachanrufe mit alphanumerischen Informationen, die auf das Telefon heruntergeladen wurden, und verwendet weiche Schaltflächen auf dem Telefon.</span><span class="sxs-lookup"><span data-stu-id="880b0-116">ADSI enhances voice calls with alphanumeric information downloaded to the phone and the use of soft buttons on the phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**linemediamode \_ digitaldata**</span><span class="sxs-lookup"><span data-stu-id="880b0-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE\_DIGITALDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-118">Ein digitaler Datenstrom des nicht angegebenen Formats.</span><span class="sxs-lookup"><span data-stu-id="880b0-118">A digital data stream of unspecified format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**Linemediamode \_ G3FAX**</span><span class="sxs-lookup"><span data-stu-id="880b0-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE\_G3FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-120">Ein Fax der Gruppe 3 wird über den-Befehl gesendet oder empfangen.</span><span class="sxs-lookup"><span data-stu-id="880b0-120">A group 3 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**Linemediamode \_ G4FAX**</span><span class="sxs-lookup"><span data-stu-id="880b0-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE\_G4FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-122">Ein Fax der Gruppe 4 wird über den-Befehl gesendet oder empfangen.</span><span class="sxs-lookup"><span data-stu-id="880b0-122">A group 4 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**linemediamode \_ interactivevoice**</span><span class="sxs-lookup"><span data-stu-id="880b0-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE\_INTERACTIVEVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-124">Beim Anruf wurde Voice Energy erkannt, und der Anruf wird als interaktiver Sprachanruf mit Menschen an beiden Enden behandelt.</span><span class="sxs-lookup"><span data-stu-id="880b0-124">Voice energy was detected on the call, and the call is handled as an interactive voice call with humans on both ends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**"linemediamode" \_ gemischt**</span><span class="sxs-lookup"><span data-stu-id="880b0-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE\_MIXED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-126">Eine gemischte Sitzung beim-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="880b0-126">A mixed session on the call.</span></span> <span data-ttu-id="880b0-127">Gemischt ist einer der ISDN-telematischen Dienste.</span><span class="sxs-lookup"><span data-stu-id="880b0-127">Mixed is one of the ISDN telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**linemediamode- \_ TDD**</span><span class="sxs-lookup"><span data-stu-id="880b0-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE\_TDD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-129">Eine TDD-Sitzung (Telefoniegeräte für gehörlos) für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="880b0-129">A TDD (Telephony Devices for the Deaf) session on the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**linemediamode- \_ Teletex**</span><span class="sxs-lookup"><span data-stu-id="880b0-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE\_TELETEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-131">Eine Teletex-Sitzung des Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="880b0-131">A teletex session on the call.</span></span> <span data-ttu-id="880b0-132">Der Teletex ist einer der telematischen Dienste.</span><span class="sxs-lookup"><span data-stu-id="880b0-132">Teletex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**linemediamode \_ Telex**</span><span class="sxs-lookup"><span data-stu-id="880b0-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE\_TELEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-134">Eine Telex-Sitzung für den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="880b0-134">A telex session on the call.</span></span> <span data-ttu-id="880b0-135">Telex ist einer der telematischen Dienste.</span><span class="sxs-lookup"><span data-stu-id="880b0-135">Telex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**linemediamode- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="880b0-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE\_VIDEO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-137">Der Medientyp des Aufrufes ist Video.</span><span class="sxs-lookup"><span data-stu-id="880b0-137">The media type of the call is video.</span></span> <span data-ttu-id="880b0-138">(TAPI-Versionen 2,1 und höher)</span><span class="sxs-lookup"><span data-stu-id="880b0-138">(TAPI versions 2.1 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**linemediamode- \_ Videotex**</span><span class="sxs-lookup"><span data-stu-id="880b0-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE\_VIDEOTEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-140">Eine Videotex-Sitzung des Aufrufs.</span><span class="sxs-lookup"><span data-stu-id="880b0-140">A videotex session on the call.</span></span> <span data-ttu-id="880b0-141">Videotex ist eine der telematischen Dienste.</span><span class="sxs-lookup"><span data-stu-id="880b0-141">Videotex is one the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**linemediamode \_ VoiceView**</span><span class="sxs-lookup"><span data-stu-id="880b0-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE\_VOICEVIEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-143">Der Medientyp des Aufrufes ist VoiceView.</span><span class="sxs-lookup"><span data-stu-id="880b0-143">The media type of the call is VoiceView.</span></span> <span data-ttu-id="880b0-144">(TAPI-Versionen 1,4 und höher)</span><span class="sxs-lookup"><span data-stu-id="880b0-144">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="880b0-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**linemediamode \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="880b0-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="880b0-146">Ein Mediendaten Strom ist vorhanden, aber sein Modus ist zurzeit nicht bekannt und kann später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="880b0-146">A media stream exists but its mode is not currently known and may become known later.</span></span> <span data-ttu-id="880b0-147">Dies entspricht einem-Befehl mit einem nicht klassifizierten Medientyp.</span><span class="sxs-lookup"><span data-stu-id="880b0-147">This would correspond to a call with an unclassified media type.</span></span> <span data-ttu-id="880b0-148">In typischen analogen Telefonieumgebungen ist der Medientyp eines eingehenden Anrufes möglicherweise unbekannt, bis der-Befehl beantwortet wurde und der Mediendaten Strom gefiltert wurde, um eine Entscheidung zu treffen.</span><span class="sxs-lookup"><span data-stu-id="880b0-148">In typical analog telephony environments, an incoming call's media type may be unknown until after the call has been answered and the media stream has been filtered to make a determination.</span></span>

<span data-ttu-id="880b0-149">Wenn das unbekannte Medien Modus-Flag festgelegt ist, können auch andere medienflags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="880b0-149">If the unknown media-mode flag is set, other media flags can also be set.</span></span> <span data-ttu-id="880b0-150">Dies wird verwendet, um anzugeben, dass das Medium unbekannt ist, aber wahrscheinlich einem der anderen ausgewählten Medientypen entspricht.</span><span class="sxs-lookup"><span data-stu-id="880b0-150">This is used to signify that the media is unknown but that it is likely to be one of the other selected media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="880b0-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="880b0-151">Remarks</span></span>

<span data-ttu-id="880b0-152">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="880b0-152">All 32 bits are reserved.</span></span>

<span data-ttu-id="880b0-153">Beachten Sie, dass bearermodus und Medientyp unterschiedliche Vorstellungen sind.</span><span class="sxs-lookup"><span data-stu-id="880b0-153">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="880b0-154">Der bearermodus eines Aufrufes ist ein Hinweis auf die Qualität der Telefonverbindung, die in erster Linie vom Netzwerk bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="880b0-154">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="880b0-155">Der Medientyp eines Aufrufes ist ein Hinweis auf den Typ des Informationsdaten Stroms, der über diesen Befehl ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="880b0-155">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="880b0-156">Gruppe 3: Fax-oder Datenmodem sind Medientypen, die einen Anruf mit einem 3,1 kHz-sprach Träger Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="880b0-156">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

<span data-ttu-id="880b0-157">Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diesen linemediamode-Wert nicht zu verwenden, wenn er von \_ der ausgehandelten Version nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="880b0-157">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEMEDIAMODE\_ value if not supported on the negotiated version.</span></span>

## <a name="requirements"></a><span data-ttu-id="880b0-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="880b0-158">Requirements</span></span>



| <span data-ttu-id="880b0-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="880b0-159">Requirement</span></span> | <span data-ttu-id="880b0-160">Wert</span><span class="sxs-lookup"><span data-stu-id="880b0-160">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="880b0-161">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="880b0-161">TAPI version</span></span><br/> | <span data-ttu-id="880b0-162">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="880b0-162">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="880b0-163">Header</span><span class="sxs-lookup"><span data-stu-id="880b0-163">Header</span></span><br/>       | <dl> <span data-ttu-id="880b0-164"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="880b0-164"><dt>Tapi.h</dt></span></span> </dl> |



 

 




