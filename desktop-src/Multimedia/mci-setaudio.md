---
title: MCI_SETAUDIO Befehl (MMSYSTEM. h)
description: Der MCI \_ setaudiobefehl legt Werte fest, die mit Audiowiedergabe und-Erfassung verknüpft sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20605ff78c62a8e688778692d5ca8f8e1342a968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213736"
---
# <a name="mci_setaudio-command"></a><span data-ttu-id="186bd-105">MCI \_ setaudiobefehl</span><span class="sxs-lookup"><span data-stu-id="186bd-105">MCI\_SETAUDIO command</span></span>

<span data-ttu-id="186bd-106">Der MCI \_ setaudiobefehl legt Werte fest, die mit Audiowiedergabe und-Erfassung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="186bd-106">The MCI\_SETAUDIO command sets values associated with audio playback and capture.</span></span> <span data-ttu-id="186bd-107">Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="186bd-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="186bd-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="186bd-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
);
```



## <a name="parameters"></a><span data-ttu-id="186bd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="186bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="186bd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="186bd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="186bd-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="186bd-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="186bd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="186bd-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="186bd-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="186bd-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="186bd-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="186bd-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpsetaudiodatei*</span><span class="sxs-lookup"><span data-stu-id="186bd-115"><span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*</span></span>
</dt> <dd>

<span data-ttu-id="186bd-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="186bd-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="186bd-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="186bd-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="186bd-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="186bd-118">Return Value</span></span>

<span data-ttu-id="186bd-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="186bd-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="186bd-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="186bd-120">Remarks</span></span>

<span data-ttu-id="186bd-121">Die folgenden Flags gelten für den **Digitalvideo** -Gerätetyp:</span><span class="sxs-lookup"><span data-stu-id="186bd-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="186bd-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ \_ setaudioalg</span><span class="sxs-lookup"><span data-stu-id="186bd-122"><span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI\_DGV\_SETAUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="186bd-123">Der **lpstrinalgorithmus** -Member der Struktur, die von *lpsetaudioidentifiziert* wird, enthält die Adresse eines Puffers, der den Namen eines Audiokomprimierungs Algorithmus enthält.</span><span class="sxs-lookup"><span data-stu-id="186bd-123">The **lpstrAlgorithm** member of the structure identified by *lpSetAudio* contains an address of a buffer containing the name of an audio compression algorithm.</span></span> <span data-ttu-id="186bd-124">Der Komprimierungs Algorithmus wird von nachfolgenden [MCI- \_ Reserve](mci-reserve.md) -oder [MCI- \_ Daten Satz](mci-record.md) Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="186bd-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="186bd-125">Die verfügbaren Algorithmen sind Geräte abhängig.</span><span class="sxs-lookup"><span data-stu-id="186bd-125">The available algorithms are device dependent.</span></span> <span data-ttu-id="186bd-126">Wenn der Algorithmus nicht mit dem aktuellen Dateiformat kompatibel ist, wird das Dateiformat in das Standardformat für den Algorithmus geändert.</span><span class="sxs-lookup"><span data-stu-id="186bd-126">If the algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ \_ setaudioclocktime</span><span class="sxs-lookup"><span data-stu-id="186bd-127"><span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI\_DGV\_SETAUDIO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="186bd-128">Die angegebene Zeit wird in Millisekunden angegeben und ist die absolute Zeit bei der Verwendung mit MCI \_ DGV \_ \_ setaudioover.</span><span class="sxs-lookup"><span data-stu-id="186bd-128">The time specified is in milliseconds and is absolute time when used with MCI\_DGV\_SETAUDIO\_OVER.</span></span> <span data-ttu-id="186bd-129">(Diese Zeit ist nicht im Schritt der Wiedergabe des Arbeitsbereichs.)</span><span class="sxs-lookup"><span data-stu-id="186bd-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="186bd-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI- \_ DGV \_ - \_ setaudioeingabe</span><span class="sxs-lookup"><span data-stu-id="186bd-130"><span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>MCI\_DGV\_SETAUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="186bd-131">Ändert das Flag für das Bass-, Treble-oder volumenflag, sodass es sich auf das Eingabe Signal auswirkt und ändert, was aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-131">Modifies the bass, treble, or volume flag so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="186bd-132">Wenn möglich, ist dies der Standardwert, wenn die Eingabe überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI- \_ DGV \_ - \_ setaudioelement</span><span class="sxs-lookup"><span data-stu-id="186bd-133"><span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>MCI\_DGV\_SETAUDIO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="186bd-134">Eine audiokonstante wird im **dwitem** -Member der-Struktur angegeben, die von *lpsetaudioangegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-134">An audio constant is specified in the **dwItem** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-135">Die Konstante identifiziert den Wert, der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="186bd-136">Die folgenden Konstanten sind definiert:</span><span class="sxs-lookup"><span data-stu-id="186bd-136">The following constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="186bd-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ \_ setaudioavgbytespersec</span><span class="sxs-lookup"><span data-stu-id="186bd-137"><span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI\_DGV\_SETAUDIO\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="186bd-138">Die durchschnittliche Anzahl von Bytes wird im **dwValue** -Member der-Struktur angegeben, die durch *lpsetaudiobezeichnet* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-138">The average number of bytes is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-139">Mit diesem Wert wird die durchschnittliche Anzahl von Bytes pro Sekunde für die Wiedergabe oder Aufzeichnung im PCM (Pulse Code Modulation) und ADPCM (Adaptive Differential Pulse Code Modulation)-Formate festgelegt.</span><span class="sxs-lookup"><span data-stu-id="186bd-139">This value sets the average number of bytes per second for playing or recording in the PCM (Pulse Code Modulation) and ADPCM (Adaptive Differential Pulse Code Modulation) formats.</span></span> <span data-ttu-id="186bd-140">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="186bd-140">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ \_ setaudiobass</span><span class="sxs-lookup"><span data-stu-id="186bd-141"><span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI\_DGV\_SETAUDIO\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="186bd-142">Der Wert für "audiolow Frequency" wird als Faktor im **dwValue** -Member der durch " *lpsetaudio"* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="186bd-142">The audio low frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ \_ setaudiobitspersample</span><span class="sxs-lookup"><span data-stu-id="186bd-143"><span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI\_DGV\_SETAUDIO\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="186bd-144">Die Anzahl der Bits pro Stichprobe wird im **dwValue** -Member der Struktur angegeben, die durch *lpsetaudiobezeichnet* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-144">The number of bits per sample is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-145">Mit diesem Wert wird die Anzahl der Bits pro Stichprobe festgelegt oder im PCM-Format aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="186bd-145">This value sets the number of bits per sample played or recorded in the PCM format.</span></span> <span data-ttu-id="186bd-146">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="186bd-146">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ \_ setaudioblockalign</span><span class="sxs-lookup"><span data-stu-id="186bd-147"><span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI\_DGV\_SETAUDIO\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="186bd-148">Die Datenblock Ausrichtung wird im **dwValue** -Member der-Struktur angegeben, die durch *lpsetaudiobezeichnet* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-148">The data block alignment is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-149">Dieser Wert legt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe Wellenform Daten fest.</span><span class="sxs-lookup"><span data-stu-id="186bd-149">This value sets the alignment of data blocks relative to the start of input waveform data.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ \_ setaudiosamplespersec</span><span class="sxs-lookup"><span data-stu-id="186bd-150"><span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI\_DGV\_SETAUDIO\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="186bd-151">Die Samplingrate wird im **dwValue** -Member der-Struktur angegeben, die durch *lpsetaudiobezeichnet* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-151">The sample rate is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-152">Dieser Wert legt die Stichprobenrate für die Wiedergabe und Aufzeichnung mit den PCM-und ADPCM-Algorithmen fest.</span><span class="sxs-lookup"><span data-stu-id="186bd-152">This value sets the sample rate for playing and recording with the PCM and ADPCM algorithms.</span></span> <span data-ttu-id="186bd-153">Die Datei wird in diesem Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="186bd-153">The file is saved in this format.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI- \_ DGV \_ - \_ setaudioquelle</span><span class="sxs-lookup"><span data-stu-id="186bd-154"><span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>MCI\_DGV\_SETAUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="186bd-155">Eine-Konstante, die die Quelle der Audioeingabe angibt, ist im **dwValue** -Member der-Struktur enthalten, die von *lpsetaudioidentifiziert* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-155">A constant specifying the source of audio input is included in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-156">Für die Audioeingabequellen sind die folgenden Konstanten definiert:</span><span class="sxs-lookup"><span data-stu-id="186bd-156">The following constants are defined for the audio input sources:</span></span>

<span data-ttu-id="186bd-157">MCI \_ DGV \_ \_ setaudioquelle \_ Durchschnitt</span><span class="sxs-lookup"><span data-stu-id="186bd-157">MCI\_DGV\_SETAUDIO\_SOURCE\_AVERAGE</span></span>

<span data-ttu-id="186bd-158">Der Durchschnitt der linken und rechten Audiokanäle.</span><span class="sxs-lookup"><span data-stu-id="186bd-158">The average of the left and right audio channels.</span></span>

<span data-ttu-id="186bd-159">MCI- \_ DGV \_ - \_ setaudioquelle \_ Links</span><span class="sxs-lookup"><span data-stu-id="186bd-159">MCI\_DGV\_SETAUDIO\_SOURCE\_LEFT</span></span>

<span data-ttu-id="186bd-160">Linker Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="186bd-160">Left audio channel.</span></span>

<span data-ttu-id="186bd-161">MCI \_ DGV \_ \_ setaudioquelle \_ Rechts</span><span class="sxs-lookup"><span data-stu-id="186bd-161">MCI\_DGV\_SETAUDIO\_SOURCE\_RIGHT</span></span>

<span data-ttu-id="186bd-162">Rechter Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="186bd-162">Right audio channel.</span></span>

<span data-ttu-id="186bd-163">MCI \_ DGV \_ \_ setaudioquelle \_ Stereo</span><span class="sxs-lookup"><span data-stu-id="186bd-163">MCI\_DGV\_SETAUDIO\_SOURCE\_STEREO</span></span>

<span data-ttu-id="186bd-164">Stereo.</span><span class="sxs-lookup"><span data-stu-id="186bd-164">Stereo.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI- \_ DGV \_ - \_ setaudiostream</span><span class="sxs-lookup"><span data-stu-id="186bd-165"><span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>MCI\_DGV\_SETAUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="186bd-166">Ein Audiodatenstrom wird im **dwValue** -Member der-Struktur angegeben, die durch *lpsetaudiobezeichnet* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-166">An audio-stream is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-167">Der ganzzahlige Wert gibt den Audiostream an, der vom Arbeitsbereich wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-167">The integer value specifies the audio stream played back from the workspace.</span></span> <span data-ttu-id="186bd-168">Wenn der Stream nicht angegeben wird, wird der erste physisch verschachtelte Audiostream wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="186bd-168">If the stream is not specified, the first physically interleaved audio stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ \_ setaudiotreble</span><span class="sxs-lookup"><span data-stu-id="186bd-169"><span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI\_DGV\_SETAUDIO\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="186bd-170">Der Wert für die hohe Frequenz Frequenz ist als Faktor im **dwValue** -Member der durch *lpsetaudioangabe* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="186bd-170">The audio high-frequency level is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI- \_ DGV \_ - \_ setaudiovolume</span><span class="sxs-lookup"><span data-stu-id="186bd-171"><span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>MCI\_DGV\_SETAUDIO\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="186bd-172">Die Audioebene für einen oder beide Audiokanäle wird als Faktor im **dwValue** -Member der Struktur angegeben, die durch *lpsetaudiobezeichnet* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-172">The audio level for one or both audio channels is specified as a factor in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-173">Wenn das linke und das Rechte Volume auf unterschiedliche Werte festgelegt wurden, ist das Verhältnis von Links zu rechter Volume ungefähr unverändert.</span><span class="sxs-lookup"><span data-stu-id="186bd-173">If the left and right volumes have been set to different values, then the ratio of left to right volume is approximately unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ \_ setaudiolinks</span><span class="sxs-lookup"><span data-stu-id="186bd-174"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="186bd-175">Aktiviert den linken Audiokanal bei Verwendung mit MCI, der \_ auf festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="186bd-175">Enables the left audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="186bd-176">Deaktiviert den linken Audiokanal bei Verwendung mit aktiviertem MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="186bd-176">Disables the left audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="186bd-177">Wenn dieses Flag mit der Kombination aus MCI \_ DGV \_ \_ setaudiovalue und MCI \_ DGV \_ setaudiovolume verwendet wird \_ , wird das Volume des linken Audiokanals festgelegt.</span><span class="sxs-lookup"><span data-stu-id="186bd-177">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the left audio channel.</span></span> <span data-ttu-id="186bd-178">Wenn dieses Flag mit MCI \_ DGV \_ setaudioquelle verwendet wird \_ , gibt es den linken Audiokanal als Quelle für den audioeingabedigitalisierer an.</span><span class="sxs-lookup"><span data-stu-id="186bd-178">When this flag is used with MCI\_DGV\_SETAUDIO\_SOURCE, it specifies the left audio channel as the source for the audio input digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ \_ setaudioover</span><span class="sxs-lookup"><span data-stu-id="186bd-179"><span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI\_DGV\_SETAUDIO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="186bd-180">Ein Übergangs Längen Parameter ist im **dwover** -Member der Struktur enthalten, die von *lpsetaudioidentifiziert* wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-180">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-181">Der Längen Wert gibt an, wie lange (in Einheiten des aktuellen Zeit Formats) benötigt wird, um eine Änderung vorzunehmen, bei der ein Faktor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-181">The length value specifies how long (in units of the current time format) it should take to make a change that uses a factor.</span></span> <span data-ttu-id="186bd-182">Wenn dieses Flag nicht verwendet wird, treten Änderungen sofort auf.</span><span class="sxs-lookup"><span data-stu-id="186bd-182">If this flag is not used, changes occur immediately.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI \_ DGV \_ \_ setaudioqualität</span><span class="sxs-lookup"><span data-stu-id="186bd-183"><span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>MCI\_DGV\_SETAUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="186bd-184">Der **lpstrauquality** -Member der Struktur, die von *lpsetaudioidentifiziert* wird, enthält eine Adresse eines Puffers, der die Audioqualität definiert.</span><span class="sxs-lookup"><span data-stu-id="186bd-184">The **lpstrQuality** member of the structure identified by *lpSetAudio* contains an address of a buffer defining the audio quality.</span></span> <span data-ttu-id="186bd-185">Eine Text Zeichenfolge innerhalb des Puffers gibt die Merkmale des Audiokomprimierungs Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="186bd-185">A text-string within the buffer specifies the characteristics of the audio compression algorithm.</span></span>

<span data-ttu-id="186bd-186">Das MCI \_ DGV \_ \_ setaudioalg-Flag kann verwendet werden, um einen Qualitäts Deskriptor für den angegebenen Algorithmus auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="186bd-186">The MCI\_DGV\_SETAUDIO\_ALG flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="186bd-187">Wenn dieses Flag weggelassen wird, wird der aktuelle Algorithmus verwendet.</span><span class="sxs-lookup"><span data-stu-id="186bd-187">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="186bd-188">Welche Algorithmen und Deskriptornamen verfügbar sind, hängt vom Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="186bd-188">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="186bd-189">Jedes Gerät bietet eine Dokumentation für die verfügbaren Algorithmen und eine Beschreibung der anwendbaren Deskriptornamen.</span><span class="sxs-lookup"><span data-stu-id="186bd-189">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="186bd-190">Mit dem [MCI- \_ Qualitäts](mci-quality.md) Befehl können zusätzliche Deskriptornamen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="186bd-190">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI- \_ DGV \_ - \_ setaudiodatensatz</span><span class="sxs-lookup"><span data-stu-id="186bd-191"><span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>MCI\_DGV\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="186bd-192">Gibt an, ob Audiodaten von der Aufzeichnung eingeschlossen oder ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="186bd-192">Specifies whether recording includes or excludes audio data.</span></span> <span data-ttu-id="186bd-193">In Kombination mit MCI \_ , das auf festgelegt \_ ist, werden Audiodaten aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="186bd-193">When combined with MCI\_SET\_ON, audio data is recorded.</span></span> <span data-ttu-id="186bd-194">In Kombination mit der Deaktivierung von MCI \_ \_ werden Audiodaten ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="186bd-194">When combined with MCI\_SET\_OFF, audio data is excluded.</span></span> <span data-ttu-id="186bd-195">Der Standardwert enthält Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="186bd-195">The default includes audio data.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ \_ setaudioright</span><span class="sxs-lookup"><span data-stu-id="186bd-196"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="186bd-197">Aktiviert den richtigen Audiokanal bei Verwendung mit MCI, der \_ auf festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="186bd-197">Enables the right audio channel when used with MCI\_SET\_ON.</span></span> <span data-ttu-id="186bd-198">Deaktiviert den richtigen Audiokanal bei Verwendung mit aktiviertem MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="186bd-198">Disables the right audio channel when used with MCI\_SET\_OFF.</span></span> <span data-ttu-id="186bd-199">Wenn dieses Flag mit der Kombination aus MCI \_ DGV \_ \_ setaudiovalue und MCI \_ DGV \_ setaudiovolume verwendet wird \_ , wird das Volume des richtigen Audiokanals festgelegt.</span><span class="sxs-lookup"><span data-stu-id="186bd-199">When this flag is used with the combination of MCI\_DGV\_SETAUDIO\_VALUE and MCI\_DGV\_SETAUDIO\_VOLUME, it sets the volume of the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI- \_ DGV \_ - \_ setaudiowert</span><span class="sxs-lookup"><span data-stu-id="186bd-200"><span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>MCI\_DGV\_SETAUDIO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="186bd-201">Im **dwValue** -Member der-Struktur, die durch *lpsetaudiobezeichnet* wird, wird ein Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="186bd-201">A value is specified in the **dwValue** member of the structure identified by *lpSetAudio*.</span></span> <span data-ttu-id="186bd-202">Die Bedeutung des Werts wird durch die Konstante angegeben, die für das MCI- \_ DGV \_ -setaudioelementflag definiert ist \_ .</span><span class="sxs-lookup"><span data-stu-id="186bd-202">The meaning of the value is specified by the constant defined for the MCI\_DGV\_SETAUDIO\_ITEM flag.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="186bd-203"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="186bd-204">Deaktiviert den angegebenen Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="186bd-204">Disables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf</span><span class="sxs-lookup"><span data-stu-id="186bd-205"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="186bd-206">Aktiviert den angegebenen Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="186bd-206">Enables the specified audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="186bd-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI- \_ \_ setaudioausgabe</span><span class="sxs-lookup"><span data-stu-id="186bd-207"><span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>MCI\_SETAUDIO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="186bd-208">Ändert das Flag für das Bass-, Treble-oder volumenflag, sodass nur das geübte Signal geändert wird und nicht das, was aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-208">Modifies the bass, treble, or volume flag so that it modifies only the played signal and not what is recorded.</span></span> <span data-ttu-id="186bd-209">Wenn möglich, ist dies der Standardwert, wenn die Eingabe überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="186bd-209">If possible, this is the default when monitoring the input.</span></span>

</dd> </dl>

<span data-ttu-id="186bd-210">Für Digital Video-Geräte zeigt der *lpsetaudioparameter* auf eine [**MCI \_ DGV- \_ setaudioparameterstruktur \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="186bd-210">For digital-video devices, the *lpSetAudio* parameter points to an [**MCI\_DGV\_SETAUDIO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) structure.</span></span>

<span data-ttu-id="186bd-211">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="186bd-211">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="186bd-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI- \_ VCR \_ - \_ setaudiodatensatz</span><span class="sxs-lookup"><span data-stu-id="186bd-212"><span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>MCI\_VCR\_SETAUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="186bd-213">Legt die Audioaufzeichnung auf ein oder aus fest, das in Verbindung mit einem der folgenden Flags verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="186bd-213">Sets the audio recording to on or off, which is used in conjunction with one of following flags:</span></span>

<span data-ttu-id="186bd-214">MCI \_ festgelegt \_ auf</span><span class="sxs-lookup"><span data-stu-id="186bd-214">MCI\_SET\_ON</span></span>

<span data-ttu-id="186bd-215">Audioaufzeichnung in.</span><span class="sxs-lookup"><span data-stu-id="186bd-215">Audio recording on.</span></span>

<span data-ttu-id="186bd-216">MCI- \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="186bd-216">MCI\_SET\_OFF</span></span>

<span data-ttu-id="186bd-217">Audioaufzeichnung aus.</span><span class="sxs-lookup"><span data-stu-id="186bd-217">Audio recording off.</span></span> <span data-ttu-id="186bd-218">Möglicherweise ist es erforderlich, zuerst die Assemblierung zu deaktivieren (mit dem Befehl [MCI \_ ](mci-set.md) -Befehl, bei dem das \_ Flag assemblierungsdatensatz für MCI VCR \_ fest \_ \_ gelegt ist), bevor die Audioaufzeichnung ausgeschaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="186bd-218">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the MCI\_VCR\_SET\_ASSEMBLE\_RECORD flag set to off) before the audio recording can be turned off.</span></span>

<span data-ttu-id="186bd-219">MCI- \_ Track</span><span class="sxs-lookup"><span data-stu-id="186bd-219">MCI\_TRACK</span></span>

<span data-ttu-id="186bd-220">Der **dwtrack** -Member der-Struktur, die von *lpsetaudioidentifiziert* wird, gibt an, welcher Titel vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="186bd-220">The **dwTrack** member of the structure identified by *lpSetAudio* specifies which track is affected by the command.</span></span>

<span data-ttu-id="186bd-221">MCI \_ VCR \_ - \_ setaudioquelle</span><span class="sxs-lookup"><span data-stu-id="186bd-221">MCI\_VCR\_SETAUDIO\_SOURCE</span></span>

<span data-ttu-id="186bd-222">Legt die Audioquelle fest.</span><span class="sxs-lookup"><span data-stu-id="186bd-222">Sets the audio source.</span></span> <span data-ttu-id="186bd-223">Dieses Flag muss mit dem MCI \_ VCR \_ - \_ setaudioflag zum Markieren von verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="186bd-223">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="186bd-224">MCI \_ VCR \_ - \_ setaudiomonitor</span><span class="sxs-lookup"><span data-stu-id="186bd-224">MCI\_VCR\_SETAUDIO\_MONITOR</span></span>

<span data-ttu-id="186bd-225">Legt den audioquellmonitor fest.</span><span class="sxs-lookup"><span data-stu-id="186bd-225">Sets the audio source monitor.</span></span> <span data-ttu-id="186bd-226">Dieses Flag muss mit dem MCI \_ VCR \_ - \_ setaudioflag zum Markieren von verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="186bd-226">This flag must be used with the MCI\_VCR\_SETAUDIO\_TO flag.</span></span>

<span data-ttu-id="186bd-227">MCI \_ VCR \_ \_ setaudioto</span><span class="sxs-lookup"><span data-stu-id="186bd-227">MCI\_VCR\_SETAUDIO\_TO</span></span>

<span data-ttu-id="186bd-228">Der **dwto** -Member der Struktur, die von *lpsetaudioidentifiziert* wird, enthält eine Konstante, die den Typ der Eingabe oder der überwachten Eingabe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="186bd-228">The **dwTo** member of the structure identified by *lpSetAudio* contains a constant describing the type of input or monitored input.</span></span> <span data-ttu-id="186bd-229">Dabei muss es sich um einen der folgenden handeln:</span><span class="sxs-lookup"><span data-stu-id="186bd-229">It must be one of the following:</span></span>

<span data-ttu-id="186bd-230"><dl> <dd></span><span class="sxs-lookup"><span data-stu-id="186bd-230"><dl> <dd></span></span>

<span data-ttu-id="186bd-231">MCI \_ VCR- \_ src- \_ \_ typtuner</span><span class="sxs-lookup"><span data-stu-id="186bd-231">MCI\_VCR\_SRC\_TYPE\_TUNER</span></span>

<span data-ttu-id="186bd-232">Typ: Tuner</span><span class="sxs-lookup"><span data-stu-id="186bd-232">Type is tuner.</span></span>

</dd> <dd>

<span data-ttu-id="186bd-233">MCI \_ VCR- \_ src- \_ \_ typzeile</span><span class="sxs-lookup"><span data-stu-id="186bd-233">MCI\_VCR\_SRC\_TYPE\_LINE</span></span>

<span data-ttu-id="186bd-234">Der Typ ist "Line".</span><span class="sxs-lookup"><span data-stu-id="186bd-234">Type is line.</span></span>

</dd> <dd>

<span data-ttu-id="186bd-235">MCI \_ VCR \_ src \_ Type \_ aux</span><span class="sxs-lookup"><span data-stu-id="186bd-235">MCI\_VCR\_SRC\_TYPE\_AUX</span></span>

<span data-ttu-id="186bd-236">Typ ist "Hilfstyp".</span><span class="sxs-lookup"><span data-stu-id="186bd-236">Type is auxiliary.</span></span>

</dd> <dd>

<span data-ttu-id="186bd-237">MCI \_ VCR- \_ src- \_ Typ \_ generisch</span><span class="sxs-lookup"><span data-stu-id="186bd-237">MCI\_VCR\_SRC\_TYPE\_GENERIC</span></span>

<span data-ttu-id="186bd-238">Der Typ ist generisch.</span><span class="sxs-lookup"><span data-stu-id="186bd-238">Type is generic.</span></span>

</dd> <dd>

<span data-ttu-id="186bd-239">MCI \_ VCR- \_ src- \_ Typ \_ stumm schalten</span><span class="sxs-lookup"><span data-stu-id="186bd-239">MCI\_VCR\_SRC\_TYPE\_MUTE</span></span>

<span data-ttu-id="186bd-240">Typ ist stumm.</span><span class="sxs-lookup"><span data-stu-id="186bd-240">Type is mute.</span></span> <span data-ttu-id="186bd-241">Dies kann nur mit dem MCI \_ VCR \_ \_ setaudioquellflag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="186bd-241">This can be used only with the MCI\_VCR\_SETAUDIO\_SOURCE flag.</span></span>

</dd> <dd>

<span data-ttu-id="186bd-242">Ausgabe des MCI- \_ VCR- \_ src- \_ Typs \_</span><span class="sxs-lookup"><span data-stu-id="186bd-242">MCI\_VCR\_SRC\_TYPE\_OUTPUT</span></span>

<span data-ttu-id="186bd-243">Der Typ ist "Output".</span><span class="sxs-lookup"><span data-stu-id="186bd-243">Type is output.</span></span>

</dd> <dd>

<span data-ttu-id="186bd-244">MCI \_ VCR \_ - \_ setaudionummer</span><span class="sxs-lookup"><span data-stu-id="186bd-244">MCI\_VCR\_SETAUDIO\_NUMBER</span></span>

<span data-ttu-id="186bd-245">Der dwnumber-Member der Struktur, die von lpsetaudioidentifiziert wird, enthält die Audioeingabe (des Typs, der im dwto-Member angegeben ist), der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="186bd-245">The dwNumber member of the structure identified by lpSetAudio contains the audio input (of the type specified in the dwTo member) to use.</span></span>

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="186bd-246">Bei VCR-Geräten verweist der *lpsetaudioparameter* auf eine [**MCI \_ VCR- \_ setaudioparameterstruktur \_**](mci-vcr-setaudio-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="186bd-246">For VCR devices, the *lpSetAudio* parameter points to an [**MCI\_VCR\_SETAUDIO\_PARMS**](mci-vcr-setaudio-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="186bd-247">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="186bd-247">Requirements</span></span>



| <span data-ttu-id="186bd-248">Anforderung</span><span class="sxs-lookup"><span data-stu-id="186bd-248">Requirement</span></span> | <span data-ttu-id="186bd-249">Wert</span><span class="sxs-lookup"><span data-stu-id="186bd-249">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186bd-250">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="186bd-250">Minimum supported client</span></span><br/> | <span data-ttu-id="186bd-251">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="186bd-251">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="186bd-252">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="186bd-252">Minimum supported server</span></span><br/> | <span data-ttu-id="186bd-253">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="186bd-253">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="186bd-254">Header</span><span class="sxs-lookup"><span data-stu-id="186bd-254">Header</span></span><br/>                   | <dl> <span data-ttu-id="186bd-255"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="186bd-255"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="186bd-256">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="186bd-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186bd-257">MCI</span><span class="sxs-lookup"><span data-stu-id="186bd-257">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="186bd-258">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="186bd-258">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

