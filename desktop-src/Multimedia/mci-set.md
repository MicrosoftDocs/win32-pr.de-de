---
title: MCI_SET Befehl (MMSYSTEM. h)
description: Der MCI- \_ set-Befehl legt Geräteinformationen fest. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk, Video-Overlay und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- MCI_SET Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1da0da94c0d970b607a29548c773fa9302d26d
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "106373393"
---
# <a name="mci_set-command"></a><span data-ttu-id="5bd55-105">Befehl "MCI- \_ Set"</span><span class="sxs-lookup"><span data-stu-id="5bd55-105">MCI\_SET command</span></span>

> [!NOTE]
> <span data-ttu-id="5bd55-106">Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5bd55-106">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="5bd55-107">In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-107">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="5bd55-108">Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-108">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="5bd55-109">Dieser Wortlaut wird verwendet, da es sich zurzeit um den in den Befehlen verwendeten Wortlaut handelt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-109">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="5bd55-110">Aus Konsistenz Gründen enthält dieses Dokument dieses Wort.</span><span class="sxs-lookup"><span data-stu-id="5bd55-110">For consistency, this document contains this word.</span></span> <span data-ttu-id="5bd55-111">Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument als Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="5bd55-111">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="5bd55-112">Der MCI- \_ set-Befehl legt Geräteinformationen fest.</span><span class="sxs-lookup"><span data-stu-id="5bd55-112">The MCI\_SET command sets device information.</span></span> <span data-ttu-id="5bd55-113">CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk, Video-Overlay und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="5bd55-113">CD audio, digital-video, MIDI sequencer, VCR, videodisc, video-overlay, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="5bd55-114">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="5bd55-114">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
);
```



## <a name="parameters"></a><span data-ttu-id="5bd55-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bd55-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd55-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="5bd55-116"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-117">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="5bd55-117">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5bd55-118"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-119">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="5bd55-119">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="5bd55-120">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5bd55-120">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpset*</span><span class="sxs-lookup"><span data-stu-id="5bd55-121"><span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-122">Zeiger auf eine Struktur für einen [**MCI- \_ Satz von \_ Parametern**](mci-set-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="5bd55-122">Pointer to an [**MCI\_SET\_PARMS**](mci-set-parms.md) structure.</span></span> <span data-ttu-id="5bd55-123">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="5bd55-123">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd55-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bd55-124">Return Value</span></span>

<span data-ttu-id="5bd55-125">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="5bd55-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd55-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bd55-126">Remarks</span></span>

<span data-ttu-id="5bd55-127">Die folgenden zusätzlichen Flags gelten für alle Geräte, die die MCI-Gruppe unterstützen \_ :</span><span class="sxs-lookup"><span data-stu-id="5bd55-127">The following additional flags apply to all devices supporting MCI\_SET:</span></span>

<dl> <dt>

<span data-ttu-id="5bd55-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ \_ -Set-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="5bd55-128"><span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI\_SET\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-129">Im dwaudiomember der durch *lpset* identifizierten Struktur ist eine audiokanalnummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="5bd55-129">An audio channel number is included in the dwAudio member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-130">Dieses Flag muss verwendet werden, wenn MCI \_ \_ auf on oder MCI Set Off festgelegt ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5bd55-130">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="5bd55-131">Verwenden Sie eine der folgenden Konstanten, um die Kanalnummer anzugeben:</span><span class="sxs-lookup"><span data-stu-id="5bd55-131">Use one of the following constants to indicate the channel number:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI \_ Set \_ \_ audioall</span><span class="sxs-lookup"><span data-stu-id="5bd55-132"><span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI\_SET\_AUDIO\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-133">Alle audiochannels.</span><span class="sxs-lookup"><span data-stu-id="5bd55-133">All audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI \_ \_ -Set-Audiodatei \_ Links</span><span class="sxs-lookup"><span data-stu-id="5bd55-134"><span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI\_SET\_AUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-135">Linker Kanal.</span><span class="sxs-lookup"><span data-stu-id="5bd55-135">Left channel.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ \_ - \_ audiorecht festlegen</span><span class="sxs-lookup"><span data-stu-id="5bd55-136"><span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI\_SET\_AUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-137">Rechter Kanal.</span><span class="sxs-lookup"><span data-stu-id="5bd55-137">Right channel.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI- \_ Einrichtung wurde \_ \_ geschlossen</span><span class="sxs-lookup"><span data-stu-id="5bd55-138"><span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>MCI\_SET\_DOOR\_CLOSED</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-139">Schließt die Medien Abdeckung (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="5bd55-139">Closes the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI- \_ fest \_ gelegungstür \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="5bd55-140"><span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>MCI\_SET\_DOOR\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-141">Öffnet die Medien Abdeckung (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="5bd55-141">Opens the media cover (if any).</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-142"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-143">Deaktiviert das angegebene Video oder den Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="5bd55-143">Disables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf</span><span class="sxs-lookup"><span data-stu-id="5bd55-144"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-145">Aktiviert das angegebene Video oder den Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="5bd55-145">Enables the specified video or audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI- \_ fest \_ gelegzeit \_ Format</span><span class="sxs-lookup"><span data-stu-id="5bd55-146"><span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>MCI\_SET\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-147">Ein Zeitformat Parameter ist im **dwtimeformat** -Member der durch *lpset* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="5bd55-147">A time format parameter is included in the **dwTimeFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-148">Die folgenden Flags werden mit diesem Flag verwendet:</span><span class="sxs-lookup"><span data-stu-id="5bd55-148">The following flags are used with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI- \_ Format ( \_ Bytes)</span><span class="sxs-lookup"><span data-stu-id="5bd55-149"><span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>MCI\_FORMAT\_BYTES</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-150">In einem PCM-Datenformat (Pulse Code-Modulation) ändert die Beschreibung für das Zeitelement in Bytes für die Eingabe oder Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5bd55-150">Within a PCM (Pulse Code Modulation) data format, changes the time member description to bytes for input or output.</span></span> <span data-ttu-id="5bd55-151">Wird vom **waveaudiogerätetyp** erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-151">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI- \_ Formatierungs \_ Frames</span><span class="sxs-lookup"><span data-stu-id="5bd55-152"><span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>MCI\_FORMAT\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-153">In nachfolgenden Befehlen werden Frames verwendet.</span><span class="sxs-lookup"><span data-stu-id="5bd55-153">Subsequent commands will use frames.</span></span> <span data-ttu-id="5bd55-154">Wird von den Gerätetypen **Digitalvideo**, **VCR** und **Videodisc** erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-154">Recognized by the **digitalvideo**, **vcr**, and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI- \_ Format \_ HMS</span><span class="sxs-lookup"><span data-stu-id="5bd55-155"><span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>MCI\_FORMAT\_HMS</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-156">Ändert das Uhrzeit Format in Stunden, Minuten und Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-156">Changes the time format to hours, minutes, and seconds.</span></span> <span data-ttu-id="5bd55-157">Wird von den Gerätetypen **VCR** und **Videodisk** erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-157">Recognized by the **vcr** and **videodisc** device types.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI- \_ Format ( \_ Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="5bd55-158"><span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>MCI\_FORMAT\_MILLISECONDS</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-159">Ändert das Zeitformat in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-159">Changes the time format to milliseconds.</span></span> <span data-ttu-id="5bd55-160">Wird von allen Gerätetypen erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-160">Recognized by all device types.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI- \_ Format \_ MSF</span><span class="sxs-lookup"><span data-stu-id="5bd55-161"><span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>MCI\_FORMAT\_MSF</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-162">Ändert das Zeitformat in Minuten, Sekunden und Frames.</span><span class="sxs-lookup"><span data-stu-id="5bd55-162">Changes the time format to minutes, seconds, and frames.</span></span> <span data-ttu-id="5bd55-163">Wird von den Gerätetypen **CDAudio** und **VCR** erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-163">Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI- \_ Format \_ Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bd55-164"><span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>MCI\_FORMAT\_SAMPLES</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-165">Ändert das Uhrzeit Format in Samplings für Eingabe oder Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5bd55-165">Changes the time format to samples for input or output.</span></span> <span data-ttu-id="5bd55-166">Wird vom **waveaudiogerätetyp** erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-166">Recognized by the **waveaudio** device type.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI \_ \_ -Format SMPTE \_ 24, MCI \_ \_ -Format SMPTE \_ 25 und MCI- \_ Format \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="5bd55-167"><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>MCI\_FORMAT\_SMPTE\_24, MCI\_FORMAT\_SMPTE\_25, and MCI\_FORMAT\_SMPTE\_30</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-168">Legt das Zeitformat auf 24, 25 und 30 Frame-SMPTE (Struktur von Bewegungsbild-und Fernseh Technikern) fest.</span><span class="sxs-lookup"><span data-stu-id="5bd55-168">Sets the time format to 24, 25, and 30 frame SMPTE (Society of Motion Picture and Television Engineers), respectively.</span></span> <span data-ttu-id="5bd55-169">Wird von den- **Sequencer** -und **VCR** -Gerätetypen erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-169">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI- \_ Format \_ SMPTE \_ 30drop</span><span class="sxs-lookup"><span data-stu-id="5bd55-170"><span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>MCI\_FORMAT\_SMPTE\_30DROP</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-171">Legt das Zeitformat auf 30 Drop-Frame-SMPTE fest.</span><span class="sxs-lookup"><span data-stu-id="5bd55-171">Sets the time format to 30 drop-frame SMPTE.</span></span> <span data-ttu-id="5bd55-172">Wird von den- **Sequencer** -und **VCR** -Gerätetypen erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-172">Recognized by the **sequencer** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI- \_ Format- \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="5bd55-173"><span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>MCI\_FORMAT\_TMSF</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-174">Ändert das Zeitformat in nachverfolgt, Minuten, Sekunden und Frames.</span><span class="sxs-lookup"><span data-stu-id="5bd55-174">Changes the time format to tracks, minutes, seconds, and frames.</span></span> <span data-ttu-id="5bd55-175">(MCI verwendet kontinuierliche Nachverfolgung.) Wird von den Gerätetypen **CDAudio** und **VCR** erkannt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-175">(MCI uses continuous track numbers.) Recognized by the **cdaudio** and **vcr** device types.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI- \_ Set- \_ Video</span><span class="sxs-lookup"><span data-stu-id="5bd55-176"><span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>MCI\_SET\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-177">Legt das Videosignal ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="5bd55-177">Sets the video signal on or off.</span></span> <span data-ttu-id="5bd55-178">Dieses Flag muss verwendet werden, wenn MCI \_ \_ auf on oder MCI \_ \_ Off Off festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5bd55-178">This flag must be used with either MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="5bd55-179">Geräte, die nicht über Video verfügen, geben eine nicht unterstützte mcierr- \_ \_ Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="5bd55-179">Devices that do not have video return MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="5bd55-180">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="5bd55-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5bd55-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ Set \_ File Format</span><span class="sxs-lookup"><span data-stu-id="5bd55-181"><span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI\_DGV\_SET\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-182">Ein Dateiformat Parameter ist im **dwfileformat** -Member der durch *lpset* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="5bd55-182">A file format parameter is included in the **dwFileFormat** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-183">Für Digital Video-Geräte wird das Dateiformat für Befehle zum Speichern oder erfassen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5bd55-183">For digital-video devices, the file format is used for save or capture commands.</span></span> <span data-ttu-id="5bd55-184">Wenn der Wert nicht angegeben wird, wird standardmäßig ein Gerätetreiber definiertes Format festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-184">If omitted, this might default to a device driver defined format.</span></span> <span data-ttu-id="5bd55-185">Wenn das angegebene Dateiformat mit dem aktuell ausgewählten Algorithmus und der ausgewählten Qualität in Konflikt steht, werden diese in die Standardwerte für das Dateiformat geändert.</span><span class="sxs-lookup"><span data-stu-id="5bd55-185">If the specified file format conflicts with the currently selected algorithm and quality, then they are changed to the defaults for the file format.</span></span> <span data-ttu-id="5bd55-186">Die folgenden Dateiformat Konstanten sind definiert:</span><span class="sxs-lookup"><span data-stu-id="5bd55-186">The following file format constants are defined:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI</span><span class="sxs-lookup"><span data-stu-id="5bd55-187"><span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI\_DGV\_FF\_AVI</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-188">AVI-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd55-188">AVI format.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ avss</span><span class="sxs-lookup"><span data-stu-id="5bd55-189"><span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI\_DGV\_FF\_AVSS</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-190">Avss-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd55-190">AVSS format.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB</span><span class="sxs-lookup"><span data-stu-id="5bd55-191"><span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI\_DGV\_FF\_DIB</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-192">DIB-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd55-192">DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ jff</span><span class="sxs-lookup"><span data-stu-id="5bd55-193"><span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI\_DGV\_FF\_JFIF</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-194">Jff-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd55-194">JFIF format.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG</span><span class="sxs-lookup"><span data-stu-id="5bd55-195"><span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI\_DGV\_FF\_JPEG</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-196">JPEG-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd55-196">JPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG</span><span class="sxs-lookup"><span data-stu-id="5bd55-197"><span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI\_DGV\_FF\_MPEG</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-198">MPEG-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd55-198">MPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ rdib</span><span class="sxs-lookup"><span data-stu-id="5bd55-199"><span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI\_DGV\_FF\_RDIB</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-200">RLE-DIB-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd55-200">RLE DIB format.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ rjpeg</span><span class="sxs-lookup"><span data-stu-id="5bd55-201"><span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI\_DGV\_FF\_RJPEG</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-202">Rjpeg-Format.</span><span class="sxs-lookup"><span data-stu-id="5bd55-202">RJPEG format.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI- \_ DGV- \_ Set- \_ Suche \_ genau</span><span class="sxs-lookup"><span data-stu-id="5bd55-203"><span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>MCI\_DGV\_SET\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-204">Legt das für die Positionierung verwendete Format fest.</span><span class="sxs-lookup"><span data-stu-id="5bd55-204">Sets the format used for positioning.</span></span> <span data-ttu-id="5bd55-205">Dieses Flag muss verwendet werden, wenn MCI \_ \_ auf on oder MCI Set Off festgelegt ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5bd55-205">This flag must be used with MCI\_SET\_ON or MCI\_SET\_OFF.</span></span> <span data-ttu-id="5bd55-206">Wenn MCI \_ für festgelegt \_ wird, wird durch die Wiedergabe oder Aufzeichnung genau auf den Frame zugegriffen, der mit dem MCI- \_ Flag from angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5bd55-206">If MCI\_SET\_ON is specified, playing or recording precisely accesses the frame specified with the MCI\_FROM flag.</span></span> <span data-ttu-id="5bd55-207">Dadurch kann es zu einer zusätzlichen Verzögerung kommen, wenn der angeforderte Frame kein Keyframe ist.</span><span class="sxs-lookup"><span data-stu-id="5bd55-207">This might add some extra delay if the requested frame is not a key frame.</span></span> <span data-ttu-id="5bd55-208">Wenn MCI \_ \_ auf OFF festgelegt ist, sucht das Gerät nach einem Key-Frame-Bild, das dem angeforderten Frame vorangestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-208">If MCI\_SET\_OFF is specified, the device will seek to a key-frame image that precedes the requested frame.</span></span> <span data-ttu-id="5bd55-209">Bei einigen Dateien und Geräten ist dies möglicherweise der erste Frame der Datei.</span><span class="sxs-lookup"><span data-stu-id="5bd55-209">For some files and devices, this might be the first frame of the file.</span></span> <span data-ttu-id="5bd55-210">Der Standardwert für dieses Flag ist Geräte abhängig.</span><span class="sxs-lookup"><span data-stu-id="5bd55-210">The default for this flag is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI- \_ DGV- \_ festgelegte \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="5bd55-211"><span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>MCI\_DGV\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-212">Ein Geschwindigkeitsparameter ist im **dwspeed** -Member der durch *lpset* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="5bd55-212">A speed parameter is included in the **dwSpeed** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-213">Die Geschwindigkeit wird als Verhältnis zwischen der nominalen Frame Rate und der gewünschten Frame Rate angegeben, bei der die nominale frametrate als 1000 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-213">Speed is specified as a ratio between the nominal frame rate and the desired frame rate where the nominal frame rate is designated as 1000.</span></span> <span data-ttu-id="5bd55-214">Die halbe Geschwindigkeit ist 500, und die doppelte Geschwindigkeit ist 2000.</span><span class="sxs-lookup"><span data-stu-id="5bd55-214">Half speed is 500 and double speed is 2000.</span></span> <span data-ttu-id="5bd55-215">Der zulässige Geschwindigkeitsbereich ist auch abhängig vom Gerät und möglicherweise von der Datei.</span><span class="sxs-lookup"><span data-stu-id="5bd55-215">The allowable speed range is dependent on the device and possibly the file, too.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI- \_ DGV- \_ Satz \_ weiterhin</span><span class="sxs-lookup"><span data-stu-id="5bd55-216"><span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>MCI\_DGV\_SET\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-217">Bei Verwendung mit MCI \_ DGV \_ Set \_ FileFormat legt die MCI- \_ Gruppe das für Aufzeichnungs Befehle verwendete Dateiformat fest.</span><span class="sxs-lookup"><span data-stu-id="5bd55-217">When used with MCI\_DGV\_SET\_FILEFORMAT, MCI\_SET sets the file format used for capture commands.</span></span>

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="5bd55-218">Für Digital Video-Geräte verweist der *lpset* -Parameter auf eine [**MCI- \_ DGV- \_ Set \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="5bd55-218">For digital-video devices, the *lpSet* parameter points to an [**MCI\_DGV\_SET\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) structure.</span></span>

<span data-ttu-id="5bd55-219">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp des **Sequencers** verwendet:</span><span class="sxs-lookup"><span data-stu-id="5bd55-219">The following additional flags are used with the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5bd55-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI-Format für das Setup- \_ \_ Format \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-220"><span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI\_SEQ\_FORMAT\_SONGPTR</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-221">Legt das Zeitformat auf die Zeiger Einheiten des Titels fest.</span><span class="sxs-lookup"><span data-stu-id="5bd55-221">Sets the time format to song pointer units.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI \_ Seq- \_ Satz \_ Master</span><span class="sxs-lookup"><span data-stu-id="5bd55-222"><span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>MCI\_SEQ\_SET\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-223">Legt den Sequencer als Quelle der Synchronisierungs Daten fest und gibt an, dass der Synchronisierungstyp im **dwmaster** -Member der durch *lpset* identifizierten Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-223">Sets the sequencer as a source of synchronization data and indicates that the type of synchronization is specified in the **dwMaster** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-224">Mcisq gibt eine nicht unterstützte mcierr- \_ \_ Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="5bd55-224">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="5bd55-225">Die folgenden Konstanten sind für den Synchronisierungstyp definiert:</span><span class="sxs-lookup"><span data-stu-id="5bd55-225">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ -Integration \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-226"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-227">Vom Sequencer werden Synchronisierungs Daten im Format "MIDI" gesendet.</span><span class="sxs-lookup"><span data-stu-id="5bd55-227">The sequencer will send MIDI format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI- \_ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="5bd55-228"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-229">Vom Sequencer werden Synchronisierungs Daten im SMPTE-Format gesendet.</span><span class="sxs-lookup"><span data-stu-id="5bd55-229">The sequencer will send SMPTE format synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI-nicht verfügbar \_ \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-230"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-231">Vom Sequencer werden keine Synchronisierungs Daten gesendet.</span><span class="sxs-lookup"><span data-stu-id="5bd55-231">The sequencer will not send synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI \_ Seq- \_ Satz \_ Offset</span><span class="sxs-lookup"><span data-stu-id="5bd55-232"><span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>MCI\_SEQ\_SET\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-233">Ändert den SMPTE-Offset einer Sequenz in den, der vom **dwOffset** -Member der durch *lpset* identifizierten-Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-233">Changes the SMPTE offset of a sequence to that specified by the **dwOffset** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-234">Dies wirkt sich nur auf Sequenzen mit einem SMPTE-Divisions Typ aus.</span><span class="sxs-lookup"><span data-stu-id="5bd55-234">This affects only sequences with a SMPTE division type.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI \_ Seq- \_ Set- \_ Port</span><span class="sxs-lookup"><span data-stu-id="5bd55-235"><span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>MCI\_SEQ\_SET\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-236">Legt den Ausgabe-MIDI-Port einer Sequenz auf die fest, die durch den Typ der MIDI-Gerätekennung im **dwport** -Member der durch *lpset* identifizierten Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-236">Sets the output MIDI port of a sequence to that specified by the MIDI device identifier in the **dwPort** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-237">Das Gerät schließt den vorherigen Port (sofern vorhanden) und versucht, den neuen Port zu öffnen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-237">The device closes the previous port (if any), and attempts to open and use the new port.</span></span> <span data-ttu-id="5bd55-238">Wenn dies nicht möglich ist, wird ein Fehler zurückgegeben, und der zuvor verwendete Port (sofern vorhanden) wird erneut geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5bd55-238">If it fails, it returns an error and reopens the previously used port (if any).</span></span> <span data-ttu-id="5bd55-239">Für die Ports sind die folgenden Konstanten definiert:</span><span class="sxs-lookup"><span data-stu-id="5bd55-239">The following constants are defined for the ports:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI-nicht verfügbar \_ \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-240"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-241">Schließt den zuvor verwendeten Port (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="5bd55-241">Closes the previously used port (if any).</span></span> <span data-ttu-id="5bd55-242">Der Sequencer verhält sich genau so, als ob ein Port geöffnet wäre, es sei denn, es wird eine MIDI-Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="5bd55-242">The sequencer behaves exactly the same as if a port were open, except no MIDI message is sent.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI- \_ Mapper</span><span class="sxs-lookup"><span data-stu-id="5bd55-243"><span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>MIDI\_MAPPER</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-244">Legt den Port fest, der für den MIDI-Mapper geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="5bd55-244">Sets the port opened to the MIDI mapper.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ Seq \_ Set \_ Slave</span><span class="sxs-lookup"><span data-stu-id="5bd55-245"><span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI\_SEQ\_SET\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-246">Legt fest, dass der Sequencer Synchronisierungs Daten empfängt, und gibt an, dass der Synchronisierungstyp im **dwslave** -Member der durch *lpset* identifizierten Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-246">Sets the sequencer to receive synchronization data and indicates that the type of synchronization is specified in the **dwSlave** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-247">Mcisq gibt eine nicht unterstützte mcierr- \_ \_ Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="5bd55-247">MCISEQ returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="5bd55-248">Die folgenden Konstanten sind für den Synchronisierungstyp definiert:</span><span class="sxs-lookup"><span data-stu-id="5bd55-248">The following constants are defined for the synchronization type:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI- \_ \_ Datei</span><span class="sxs-lookup"><span data-stu-id="5bd55-249"><span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>MCI\_SEQ\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-250">Der Sequencer wird so festgelegt, dass die Synchronisierungs Daten in der-Datei mit der Datei</span><span class="sxs-lookup"><span data-stu-id="5bd55-250">Sets the sequencer to receive synchronization data contained in the MIDI file.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ -Integration \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-251"><span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI\_SEQ\_MIDI</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-252">Legt fest, dass der Sequencer Daten zur Datensynchronisierung empfängt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-252">Sets the sequencer to receive MIDI synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI-nicht verfügbar \_ \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-253"><span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI\_SEQ\_NONE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-254">Legt fest, dass der Sequencer Synchronisierungs Daten in einem MIDI-Stream ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5bd55-254">Sets the sequencer to ignore synchronization data in a MIDI stream.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI- \_ \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="5bd55-255"><span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI\_SEQ\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-256">Legt fest, dass der Sequencer SMPTE-Synchronisierungs Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-256">Sets the sequencer to receive SMPTE synchronization data.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI \_ Seq- \_ Set- \_ Tempo</span><span class="sxs-lookup"><span data-stu-id="5bd55-257"><span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>MCI\_SEQ\_SET\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-258">Ändert das Tempo der MIDI-Sequenz in, das vom **dwtempo** -Member der-Struktur angegeben wird, auf die von *lpset* gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-258">Changes the tempo of the MIDI sequence to that specified by the **dwTempo** member of the structure pointed to by *lpSet*.</span></span> <span data-ttu-id="5bd55-259">Für Sequenzen mit dem Divisions Datentyp ppqn wird das Tempo in Beats pro Minute angegeben; für Sequenzen mit dem Divisions Typ SMPTE wird das Tempo in Frames pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="5bd55-259">For sequences with division type PPQN, tempo is specified in beats per minute; for sequences with division type SMPTE, tempo is specified in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="5bd55-260">Für Sequencer-Geräte verweist der *lpset* -Parameter auf eine [**MCI \_ Seq \_ Set \_**](mci-seq-set-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="5bd55-260">For sequencer devices, the *lpSet* parameter points to an [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure.</span></span>

<span data-ttu-id="5bd55-261">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="5bd55-261">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5bd55-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI \_ VCR \_ Set \_ \_ assemblierungsdatensatz</span><span class="sxs-lookup"><span data-stu-id="5bd55-262"><span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>MCI\_VCR\_SET\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-263">Legt fest, dass das Gerät im Assemblierungs-oder Einfügemodus aufgezeichnet wird (wenn assembliert ist, INSERT auf ON festgelegt ist und umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="5bd55-263">Sets the device to record in assemble or insert modes (when assemble is off, insert is on, and vice-versa).</span></span> <span data-ttu-id="5bd55-264">Verwenden Sie mit einem der folgenden Flags:</span><span class="sxs-lookup"><span data-stu-id="5bd55-264">Use with one of the following flag:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf</span><span class="sxs-lookup"><span data-stu-id="5bd55-265"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-266">Legt den assemblierungsdatensatz auf fest und schaltet INSERT-Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="5bd55-266">Sets assemble record on, and turns insert record off.</span></span> <span data-ttu-id="5bd55-267">Zeichnet alle Video-, Audio-und Zeit Leitzahl-Spuren auf.</span><span class="sxs-lookup"><span data-stu-id="5bd55-267">Records all video, audio and timecode tracks.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-268"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-269">Setzt assemblierungsdatensatz aus und schaltet INSERT-Datensatz ein.</span><span class="sxs-lookup"><span data-stu-id="5bd55-269">Sets assemble record off, and turns insert record on.</span></span> <span data-ttu-id="5bd55-270">Wenn assemblierungsdatensatz auf OFF festgelegt ist, können einzelne Titel von Video, Audiodaten und Zeitcode für die Aufzeichnung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-270">When assemble record is off, individual tracks of video, audio, and timecode can be selected for recording.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI \_ VCR- \_ festgelegte \_ Uhr</span><span class="sxs-lookup"><span data-stu-id="5bd55-271"><span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>MCI\_VCR\_SET\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-272">Der **dwclock** -Member der durch *lpset* identifizierten Struktur enthält die neue Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="5bd55-272">The **dwClock** member of the structure identified by *lpSet* contains the new clock time.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI \_ VCR- \_ Satz-gegen-Satz- \_ \_ forma</span><span class="sxs-lookup"><span data-stu-id="5bd55-273"><span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>MCI\_VCR\_SET\_COUNTER\_FORMA</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-274">Der **dwcounter Format** -Member der durch *lpset* identifizierten-Struktur enthält eine-Konstante, die das neue vom Status Indikator zu verwendende Indikator Zeitformat angibt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-274">The **dwCounterFormat** member of the structure identified by *lpSet* contains a constant specifying the new counter-time format to be used by the status counter.</span></span> <span data-ttu-id="5bd55-275">Eine Liste gültiger Konstanten finden Sie unter MCI- \_ festgelegter \_ Zeit \_ Format in der Liste der zusätzlichen Flags für diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="5bd55-275">For a list of valid constants, see MCI\_SET\_TIME\_FORMAT in the list of additional flags for this command.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI \_ VCR \_ festlegen \_ des \_ Leistungs Zählers</span><span class="sxs-lookup"><span data-stu-id="5bd55-276"><span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>MCI\_VCR\_SET\_COUNTER\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-277">Der **dwcountervalue** -Member der durch *lpset* identifizierten Struktur enthält den neuen Indikator Wert.</span><span class="sxs-lookup"><span data-stu-id="5bd55-277">The **dwCounterValue** member of the structure identified by *lpSet* contains the new counter value.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI- \_ VCR- \_ Satz \_ Index</span><span class="sxs-lookup"><span data-stu-id="5bd55-278"><span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>MCI\_VCR\_SET\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-279">Der **dwIndex** -Member der durch *lpset* identifizierten Struktur enthält eine Konstante, die den Inhalt der Bildschirm Anzeige angibt und einen der folgenden Werte aufweisen muss:</span><span class="sxs-lookup"><span data-stu-id="5bd55-279">The **dwIndex** member of the structure identified by *lpSet* contains a constant indicating the contents of the on-screen display and must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI- \_ VCR- \_ Index Indikator \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-280"><span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>MCI\_VCR\_INDEX\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-281">Zeigt den Counter an.</span><span class="sxs-lookup"><span data-stu-id="5bd55-281">Displays counter.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>Datum des MCI- \_ VCR- \_ Indexes \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-282"><span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>MCI\_VCR\_INDEX\_DATE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-283">Zeigt das Datum an.</span><span class="sxs-lookup"><span data-stu-id="5bd55-283">Displays date.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI- \_ VCR- \_ Index \_ Zeit</span><span class="sxs-lookup"><span data-stu-id="5bd55-284"><span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>MCI\_VCR\_INDEX\_TIME</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-285">Zeigt die Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="5bd55-285">Displays time.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI- \_ VCR- \_ Index \_ Zeit Code</span><span class="sxs-lookup"><span data-stu-id="5bd55-286"><span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>MCI\_VCR\_INDEX\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-287">Zeigt Timecode an.</span><span class="sxs-lookup"><span data-stu-id="5bd55-287">Displays timecode.</span></span>

<span data-ttu-id="5bd55-288">Weitere Informationen finden Sie unter dem [MCI- \_ Index](mci-index.md) Befehl.</span><span class="sxs-lookup"><span data-stu-id="5bd55-288">For more information, see the [MCI\_INDEX](mci-index.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI \_ VCR \_ Set \_ Pause \_ Timeout</span><span class="sxs-lookup"><span data-stu-id="5bd55-289"><span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>MCI\_VCR\_SET\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-290">Der **dwpausetimeout** -Member der durch *lpset* identifizierten Struktur enthält die maximale Dauer eines Pause-Befehls in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-290">The **dwPauseTimeout** member of the structure identified by *lpSet* contains the maximum duration, in milliseconds, of a pause command.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI \_ VCR \_ Festlegen der \_ Postroll \_ Dauer</span><span class="sxs-lookup"><span data-stu-id="5bd55-291"><span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>MCI\_VCR\_SET\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-292">Der **dwpostrollduration** -Member der Struktur, die von *lpset* identifiziert wird, enthält die videtape-Länge im aktuellen Zeitformat, die zum Bremsen des VCR-Transports erforderlich ist, wenn ein Befehl zum Beenden oder anhalten ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-292">The **dwPostrollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to brake the VCR transport when a stop or pause command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI \_ VCR \_ Set \_ Power</span><span class="sxs-lookup"><span data-stu-id="5bd55-293"><span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>MCI\_VCR\_SET\_POWER</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-294">Legt den einschalten oder deaktivieren fest.</span><span class="sxs-lookup"><span data-stu-id="5bd55-294">Sets the power on or off.</span></span> <span data-ttu-id="5bd55-295">Muss mit einem der folgenden Flags verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="5bd55-295">Must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-296"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-297">Schaltet ausschalten.</span><span class="sxs-lookup"><span data-stu-id="5bd55-297">Turns power off.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf</span><span class="sxs-lookup"><span data-stu-id="5bd55-298"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-299">Schaltet Einschalten ein.</span><span class="sxs-lookup"><span data-stu-id="5bd55-299">Turns power on.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>Dauer der Vorabversion von MCI \_ VCR \_ festgelegt \_ \_</span><span class="sxs-lookup"><span data-stu-id="5bd55-300"><span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>MCI\_VCR\_SET\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-301">Der **dwprerollduration** -Member der Struktur, die von *lpset* identifiziert wird, enthält die im aktuellen Zeitformat für die Stabilisierung der VCR-Ausgabe erforderliche videobandlänge.</span><span class="sxs-lookup"><span data-stu-id="5bd55-301">The **dwPrerollDuration** member of the structure identified by *lpSet* contains the videotape length, in the current time format, needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI \_ VCR \_ - \_ Daten Satz \_ Format festlegen</span><span class="sxs-lookup"><span data-stu-id="5bd55-302"><span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>MCI\_VCR\_SET\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-303">Der **dwrecordformat** -Member der-Struktur, die von *lpset* identifiziert wird, enthält eine-Konstante, die die Daten Satz Geschwindigkeit beschreibt. diese muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="5bd55-303">The **dwRecordFormat** member of the structure identified by *lpSet* contains a constant describing the record speed, which must be one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI \_ VCR- \_ Format \_ EP</span><span class="sxs-lookup"><span data-stu-id="5bd55-304"><span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>MCI\_VCR\_FORMAT\_EP</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-305">Datensätze mit langsamer Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="5bd55-305">Records at slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI \_ VCR- \_ Format- \_ LP</span><span class="sxs-lookup"><span data-stu-id="5bd55-306"><span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>MCI\_VCR\_FORMAT\_LP</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-307">Datensätze mit mittlerer und langsamer Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="5bd55-307">Records at medium-slow speed.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI \_ VCR- \_ Format \_ SP</span><span class="sxs-lookup"><span data-stu-id="5bd55-308"><span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI\_VCR\_FORMAT\_SP</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-309">Datensätze mit Standardgeschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="5bd55-309">Records at standard speed.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI \_ VCR- \_ festgelegte \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="5bd55-310"><span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>MCI\_VCR\_SET\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-311">Der **dwspeed** -Member der Struktur, die von *lpset* identifiziert wird, enthält die neue Geschwindigkeitseinstellung, wobei 1000 eine normale Geschwindigkeit, 2000 die doppelte Geschwindigkeit und 500 eine halbe Geschwindigkeit ist usw.</span><span class="sxs-lookup"><span data-stu-id="5bd55-311">The **dwSpeed** member of the structure identified by *lpSet* contains the new speed setting, where 1000 is normal speed, 2000 is double speed, and 500 is half speed, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI \_ VCR \_ festlegen \_ der \_ Bandlänge</span><span class="sxs-lookup"><span data-stu-id="5bd55-312"><span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>MCI\_VCR\_SET\_TAPE\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-313">Der **dwtapelength** -Member der durch *lpset* identifizierten Struktur enthält die neue Bandlänge, vorausgesetzt, die Bandlänge ist nicht erkennbar.</span><span class="sxs-lookup"><span data-stu-id="5bd55-313">The **dwTapeLength** member of the structure identified by *lpSet* contains the new length of the tape, provided that the length of the tape is undetectable.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI \_ VCR- \_ festgelegte \_ Zeit \_ Modus</span><span class="sxs-lookup"><span data-stu-id="5bd55-314"><span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>MCI\_VCR\_SET\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-315">Der **dwtimemode** -Member der durch *lpset* identifizierten Struktur enthält eine Konstante, die den neuen Positions Zeit Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-315">The **dwTimeMode** member of the structure identified by *lpSet* contains a constant indicating the new positional time mode.</span></span> <span data-ttu-id="5bd55-316">Die folgenden Konstanten sind gültig:</span><span class="sxs-lookup"><span data-stu-id="5bd55-316">The following constants are valid:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI- \_ VCR- \_ Zeit ( \_ Counter)</span><span class="sxs-lookup"><span data-stu-id="5bd55-317"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-318">Erzwingt, dass das Gerät den Counter exklusiv verwendet.</span><span class="sxs-lookup"><span data-stu-id="5bd55-318">Forces the device to use counter exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI- \_ VCR- \_ Zeit \_ Erkennung</span><span class="sxs-lookup"><span data-stu-id="5bd55-319"><span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>MCI\_VCR\_TIME\_DETECT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-320">Jedes Mal, wenn ein neues Videoband in das Gerät eingefügt wird oder sich der Modus von nicht bereit in bereit befindet, sollte das Gerät versuchen, festzustellen, ob auf dem Videoband Zeitcode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5bd55-320">Each time a new videotape is inserted into the device, or the mode changes from not ready to ready, the device should attempt to determine if there is timecode available on the videotape.</span></span> <span data-ttu-id="5bd55-321">Wenn Zeitcode verfügbar ist, verwenden Sie Zeitcode in allen nachfolgenden Befehlen, die Positionen angeben.</span><span class="sxs-lookup"><span data-stu-id="5bd55-321">If timecode is available, use timecode in all subsequent commands that specify positions.</span></span> <span data-ttu-id="5bd55-322">Andernfalls verwenden Sie den-Wert.</span><span class="sxs-lookup"><span data-stu-id="5bd55-322">Otherwise, use the counter.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI- \_ VCR- \_ Zeit ( \_ Timecode)</span><span class="sxs-lookup"><span data-stu-id="5bd55-323"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-324">Erzwingt die ausschließliche Verwendung von Zeitcode durch das Gerät.</span><span class="sxs-lookup"><span data-stu-id="5bd55-324">Forces the device to use timecode exclusively.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI \_ VCR-Set-nach \_ \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="5bd55-325"><span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>MCI\_VCR\_SET\_TRACKING</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-326">Optimiert die Geschwindigkeit des VCR-Band Transports mit einer fein Anpassung und muss mit einem der folgenden Flags verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="5bd55-326">Tunes the speed of the VCR tape transport with a fine adjustment, and must be used with one of the following flags:</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI \_ VCR \_ Plus</span><span class="sxs-lookup"><span data-stu-id="5bd55-327"><span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>MCI\_VCR\_PLUS</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-328">Erhöht die Band Transportgeschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="5bd55-328">Increases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI \_ VCR \_ minus</span><span class="sxs-lookup"><span data-stu-id="5bd55-329"><span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>MCI\_VCR\_MINUS</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-330">Verringert die Band Transportgeschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="5bd55-330">Decreases the tape transport speed.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI- \_ VCR- \_ zurück Setzung</span><span class="sxs-lookup"><span data-stu-id="5bd55-331"><span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>MCI\_VCR\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-332">Gibt die nach Verfolgungs Anpassung zu 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5bd55-332">Returns the tracking adjustment to zero.</span></span>

</dd> </dl>

<span data-ttu-id="5bd55-333">Bei VCR-Geräten verweist der *lpset* -Parameter auf eine [**MCI- \_ VCR- \_ Set \_**](mci-vcr-set-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="5bd55-333">For VCR devices, the *lpSet* parameter points to an [**MCI\_VCR\_SET\_PARMS**](mci-vcr-set-parms.md) structure.</span></span>

<span data-ttu-id="5bd55-334">Das folgende zusätzliche Flag wird für den **Videodisk** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="5bd55-334">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5bd55-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI- \_ VD- \_ Format \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="5bd55-335"><span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>MCI\_VD\_FORMAT\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-336">Ändert das Zeitformat in nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-336">Changes the time format to tracks.</span></span> <span data-ttu-id="5bd55-337">MCI verwendet kontinuierliche Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="5bd55-337">MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="5bd55-338">Die folgenden zusätzlichen Flags werden mit dem **waveaudiogerätetyp** verwendet:</span><span class="sxs-lookup"><span data-stu-id="5bd55-338">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="5bd55-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI- \_ Wave- \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="5bd55-339"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-340">Legt die Eingabe fest, die für die Aufzeichnung in den **Winput** -Member der durch *lpset* identifizierten Struktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-340">Sets the input used for recording to the **wInput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI- \_ Wave- \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="5bd55-341"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-342">Legt die Ausgabe fest, die für die Wiedergabe mit dem **woutput** -Member der durch *lpset* identifizierten Struktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-342">Sets the output used for playing to the **wOutput** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI- \_ Wellen \_ Satz \_ anyinput</span><span class="sxs-lookup"><span data-stu-id="5bd55-343"><span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>MCI\_WAVE\_SET\_ANYINPUT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-344">Alle mit dem aktuellen Format kompatiblen Wellen Eingaben können für die Aufzeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-344">Any wave input compatible with the current format can be used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI- \_ Wellen \_ Satz \_ anyoutput</span><span class="sxs-lookup"><span data-stu-id="5bd55-345"><span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>MCI\_WAVE\_SET\_ANYOUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-346">Alle mit dem aktuellen Format kompatiblen Wellen Ausgaben können für die Wiedergabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-346">Any wave output compatible with the current format can be used for playing.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI- \_ Wellen \_ Satz \_ avgbytespersec</span><span class="sxs-lookup"><span data-stu-id="5bd55-347"><span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-348">Legt die Bytes pro Sekunde fest, die zum wiedergeben, aufzeichnen und speichern in dem **navgbytespersec** -Member der durch *lpset* identifizierten Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-348">Sets the bytes per second used for playing, recording, and saving to the **nAvgBytesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI- \_ Wellen \_ Satz \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="5bd55-349"><span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-350">Legt die Bits pro Stichprobe fest, die zum wiedergeben, aufzeichnen und Speichern des **nbitspersample** -Members des PCM-Datenformats verwendet werden, das von *lpset* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-350">Sets the bits per sample used for playing, recording, and saving to the **nBitsPerSample** member of the PCM data format identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI- \_ Wellen \_ Satz \_ BlockAlign</span><span class="sxs-lookup"><span data-stu-id="5bd55-351"><span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-352">Legt die Block Ausrichtung fest, die zum Abspielen, aufzeichnen und speichern in dem **nBlockAlign** -Member der durch *lpset* identifizierten Struktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-352">Sets the block alignment used for playing, recording, and saving to the **nBlockAlign** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI- \_ Wellen \_ Satz \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="5bd55-353"><span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>MCI\_WAVE\_SET\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-354">Die Anzahl der Kanäle wird im **nchannels** -Member der durch *lpset* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="5bd55-354">The number of channels is indicated in the **nChannels** member of the structure identified by *lpSet*.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI- \_ Wellen \_ Satz \_ Formattag</span><span class="sxs-lookup"><span data-stu-id="5bd55-355"><span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>MCI\_WAVE\_SET\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-356">Legt den Formattyp fest, der zum Abspielen, aufzeichnen und speichern im **wformattag** -Member der durch *lpset* identifizierten Struktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd55-356">Sets the format type used for playing, recording, and saving to the **wFormatTag** member of the structure identified by *lpSet*.</span></span> <span data-ttu-id="5bd55-357">Durch angeben \_ des Wave-Formats \_ PCM wird das Format in PCM geändert.</span><span class="sxs-lookup"><span data-stu-id="5bd55-357">Specifying WAVE\_FORMAT\_PCM changes the format to PCM.</span></span>

</dd> <dt>

<span data-ttu-id="5bd55-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI- \_ Wellen \_ Satz \_ samplespersec</span><span class="sxs-lookup"><span data-stu-id="5bd55-358"><span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="5bd55-359">Legt die Stichproben pro Sekunde fest, die für die Wiedergabe, Aufzeichnung und Speicherung in dem **nsamplespersec** -Member der durch *lpset* identifizierten Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bd55-359">Sets the samples per second used for playing, recording, and saving to the **nSamplesPerSec** member of the structure identified by *lpSet*.</span></span>

</dd> </dl>

<span data-ttu-id="5bd55-360">Bei Waveform-Audiogeräten verweist der *lpset* -Parameter auf eine [**MCI- \_ Wellen \_ Satz \_**](mci-wave-set-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="5bd55-360">For waveform-audio devices, the *lpSet* parameter points to an [**MCI\_WAVE\_SET\_PARMS**](mci-wave-set-parms.md) structure.</span></span>

<span data-ttu-id="5bd55-361">Wenn die Datei zum Speichern der Daten erstellt wird, werden mehrere Eigenschaften von Waveform-Audiodaten definiert.</span><span class="sxs-lookup"><span data-stu-id="5bd55-361">Several properties of waveform-audio data are defined when the file to store the data is created.</span></span> <span data-ttu-id="5bd55-362">Diese Eigenschaften beschreiben, wie die Daten innerhalb der Datei strukturiert sind und nicht geändert werden können, wenn die Aufzeichnung beginnt.</span><span class="sxs-lookup"><span data-stu-id="5bd55-362">These properties describe how the data is structured within the file and cannot be changed once recording begins.</span></span> <span data-ttu-id="5bd55-363">Die folgenden Eigenschaften werden in der folgenden Liste von Flags identifiziert:</span><span class="sxs-lookup"><span data-stu-id="5bd55-363">The following list of flags identifies these properties:</span></span>

-   <span data-ttu-id="5bd55-364">MCI- \_ Wellen \_ Satz \_ avgbytespersec</span><span class="sxs-lookup"><span data-stu-id="5bd55-364">MCI\_WAVE\_SET\_AVGBYTESPERSEC</span></span>
-   <span data-ttu-id="5bd55-365">MCI- \_ Wellen \_ Satz \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="5bd55-365">MCI\_WAVE\_SET\_BITSPERSAMPLE</span></span>
-   <span data-ttu-id="5bd55-366">MCI- \_ Wellen \_ Satz \_ BlockAlign</span><span class="sxs-lookup"><span data-stu-id="5bd55-366">MCI\_WAVE\_SET\_BLOCKALIGN</span></span>
-   <span data-ttu-id="5bd55-367">MCI- \_ Wellen \_ Satz \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="5bd55-367">MCI\_WAVE\_SET\_CHANNELS</span></span>
-   <span data-ttu-id="5bd55-368">MCI- \_ Wellen \_ Satz \_ Formattag</span><span class="sxs-lookup"><span data-stu-id="5bd55-368">MCI\_WAVE\_SET\_FORMATTAG</span></span>
-   <span data-ttu-id="5bd55-369">MCI- \_ Wellen \_ Satz \_ samplespersec</span><span class="sxs-lookup"><span data-stu-id="5bd55-369">MCI\_WAVE\_SET\_SAMPLESPERSEC</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd55-370">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bd55-370">Requirements</span></span>



| <span data-ttu-id="5bd55-371">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bd55-371">Requirement</span></span> | <span data-ttu-id="5bd55-372">Wert</span><span class="sxs-lookup"><span data-stu-id="5bd55-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd55-373">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bd55-373">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd55-374">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bd55-374">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5bd55-375">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bd55-375">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd55-376">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bd55-376">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5bd55-377">Header</span><span class="sxs-lookup"><span data-stu-id="5bd55-377">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bd55-378"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd55-378"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd55-379">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bd55-379">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd55-380">MCI</span><span class="sxs-lookup"><span data-stu-id="5bd55-380">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5bd55-381">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="5bd55-381">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

