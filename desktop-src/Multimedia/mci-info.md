---
title: MCI_INFO Befehl (MMSYSTEM. h)
description: Der MCI- \_ Info-Befehl ruft Zeichen folgen Informationen von einem Gerät ab.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105710"
---
# <a name="mci_info-command"></a><span data-ttu-id="26eb9-104">MCI- \_ Info-Befehl</span><span class="sxs-lookup"><span data-stu-id="26eb9-104">MCI\_INFO command</span></span>

<span data-ttu-id="26eb9-105">Der MCI- \_ Info-Befehl ruft Zeichen folgen Informationen von einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-105">The MCI\_INFO command retrieves string information from a device.</span></span> <span data-ttu-id="26eb9-106">Alle Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="26eb9-106">All devices recognize this command.</span></span> <span data-ttu-id="26eb9-107">Informationen werden im **lpstraureturn** -Member der Struktur zurückgegeben, die von *lpInfo* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="26eb9-107">Information is returned in the **lpstrReturn** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="26eb9-108">Der **dwretsize** -Member gibt die Pufferlänge für die zurückgegebenen Daten an.</span><span class="sxs-lookup"><span data-stu-id="26eb9-108">The **dwRetSize** member specifies the buffer length for the returned data.</span></span>

<span data-ttu-id="26eb9-109">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="26eb9-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
);
```



## <a name="parameters"></a><span data-ttu-id="26eb9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26eb9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26eb9-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="26eb9-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-112">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="26eb9-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="26eb9-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-114">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="26eb9-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="26eb9-115">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="26eb9-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*Puffer lpInfo*</span><span class="sxs-lookup"><span data-stu-id="26eb9-116"><span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-117">Zeiger auf eine [**MCI \_ - \_ Info**](mci-info-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="26eb9-117">Pointer to an [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure.</span></span> <span data-ttu-id="26eb9-118">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="26eb9-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26eb9-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26eb9-119">Return Value</span></span>

<span data-ttu-id="26eb9-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="26eb9-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="26eb9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26eb9-121">Remarks</span></span>

<span data-ttu-id="26eb9-122">Das folgende zusätzliche Standard-und Befehls spezifische Flag gilt für alle Geräte, die MCI-Informationen unterstützen \_ :</span><span class="sxs-lookup"><span data-stu-id="26eb9-122">The following additional standard and command-specific flag applies to all devices supporting MCI\_INFO:</span></span>

<dl> <dt>

<span data-ttu-id="26eb9-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI- \_ Informations \_ Produkt</span><span class="sxs-lookup"><span data-stu-id="26eb9-123"><span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>MCI\_INFO\_PRODUCT</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-124">Ruft eine Beschreibung der Hardware ab, die einem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26eb9-124">Obtains a description of the hardware associated with a device.</span></span> <span data-ttu-id="26eb9-125">Geräte sollten eine Beschreibung angeben, mit der sowohl der Treiber als auch die verwendete Hardware identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="26eb9-125">Devices should supply a description that identifies both the driver and the hardware used.</span></span>

</dd> </dl>

<span data-ttu-id="26eb9-126">Die folgenden zusätzlichen Flags gelten für den **CDAudio** -Gerätetyp:</span><span class="sxs-lookup"><span data-stu-id="26eb9-126">The following additional flags apply to the **cdaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26eb9-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI- \_ Info \_ Medien \_ Identität</span><span class="sxs-lookup"><span data-stu-id="26eb9-127"><span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>MCI\_INFO\_MEDIA\_IDENTITY</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-128">Erzeugt einen eindeutigen Bezeichner für die AudioCD, die derzeit in dem abgefragten Player geladen wird.</span><span class="sxs-lookup"><span data-stu-id="26eb9-128">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span> <span data-ttu-id="26eb9-129">Dieses Flag gibt eine Zeichenfolge mit 16 hexadezimalen Ziffern zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-129">This flag returns a string of 16 hexadecimal digits.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI- \_ Info \_ Medien ( \_ UPC)</span><span class="sxs-lookup"><span data-stu-id="26eb9-130"><span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI\_INFO\_MEDIA\_UPC</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-131">Erzeugt den universellen Produkt Code (Universal Product Code, UPC), der auf einer AudioCD codiert ist.</span><span class="sxs-lookup"><span data-stu-id="26eb9-131">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="26eb9-132">Der UPC ist eine Zeichenfolge mit Ziffern.</span><span class="sxs-lookup"><span data-stu-id="26eb9-132">The UPC is a string of digits.</span></span> <span data-ttu-id="26eb9-133">Sie ist möglicherweise nicht für alle CDs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26eb9-133">It might not be available for all CDs.</span></span>

</dd> </dl>

<span data-ttu-id="26eb9-134">Die folgenden zusätzlichen Flags gelten für den **Digitalvideo** -Gerätetyp:</span><span class="sxs-lookup"><span data-stu-id="26eb9-134">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26eb9-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI- \_ DGV- \_ Info \_ Element</span><span class="sxs-lookup"><span data-stu-id="26eb9-135"><span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>MCI\_DGV\_INFO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-136">Eine-Konstante, die angibt, dass die gewünschten Informationen im **dwitem** -Member der durch *lpInfo* identifizierten-Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="26eb9-136">A constant indicating the information desired is included in the **dwItem** member of the structure identified by *lpInfo*.</span></span> <span data-ttu-id="26eb9-137">Die folgenden Konstanten sind für Digital Video-Geräte definiert:</span><span class="sxs-lookup"><span data-stu-id="26eb9-137">The following constants are defined for digital-video devices:</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ Info \_ \_ audioalg</span><span class="sxs-lookup"><span data-stu-id="26eb9-138"><span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI\_DGV\_INFO\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-139">Gibt den Namen für den aktuellen Audiokomprimierungs Algorithmus zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-139">Returns the name for the current audio compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ \_ -DGV \_ -Info- \_ Audioqualität</span><span class="sxs-lookup"><span data-stu-id="26eb9-140"><span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI\_DGV\_INFO\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-141">Gibt den Namen für den aktuellen audioqualitätsdeskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-141">Returns the name for the current audio quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI- \_ DGV- \_ Informationen sind \_ immer noch \_ alg</span><span class="sxs-lookup"><span data-stu-id="26eb9-142"><span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>MCI\_DGV\_INFO\_STILL\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-143">Gibt den Namen für den aktuellen immer noch Bild Komprimierungs Algorithmus zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-143">Returns the name for the current still image compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI- \_ DGV- \_ Informationen \_ weiterhin \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="26eb9-144"><span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>MCI\_DGV\_INFO\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-145">Gibt den Namen für den aktuellen immer noch Bild Qualitäts Deskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-145">Returns the name for the current still image quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI- \_ DGV- \_ Informations \_ Verwendung</span><span class="sxs-lookup"><span data-stu-id="26eb9-146"><span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>MCI\_DGV\_INFO\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-147">Gibt eine Zeichenfolge zurück, in der die Nutzungseinschränkungen beschrieben werden, die möglicherweise vom Besitzer der visuellen oder hörbaren Daten im Arbeitsbereich auferlegt werden.</span><span class="sxs-lookup"><span data-stu-id="26eb9-147">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audible data in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI \_ DGV \_ Info \_ Video \_ alg</span><span class="sxs-lookup"><span data-stu-id="26eb9-148"><span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>MCI\_DGV\_INFO\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-149">Gibt den Namen für den aktuellen Video Komprimierungs Algorithmus zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-149">Returns the name for the current video compression algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI- \_ DGV- \_ \_ Video \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="26eb9-150"><span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>MCI\_DGV\_INFO\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-151">Gibt den Namen für den aktuellen Video Qualitäts Deskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-151">Returns the name for the current video quality descriptor.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI- \_ Informations \_ Version</span><span class="sxs-lookup"><span data-stu-id="26eb9-152"><span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>MCI\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-153">Gibt die releaseebene des Gerätetreibers und der Hardware zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-153">Returns the release level of the device driver and hardware.</span></span> <span data-ttu-id="26eb9-154">Gerätetreiber Entwickler müssen die Syntax der zurückgegebenen Zeichenfolge dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="26eb9-154">Device driver developers must document the syntax of the returned string.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI- \_ DGV- \_ Info \_ Text</span><span class="sxs-lookup"><span data-stu-id="26eb9-155"><span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>MCI\_DGV\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-156">Ruft die Beschriftung des Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-156">Obtains the window caption.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ - \_ Infodatei</span><span class="sxs-lookup"><span data-stu-id="26eb9-157"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-158">Ruft den Pfad und den Dateinamen der letzten mit dem Befehl " [MCI \_ Öffnen](mci-open.md) " oder " [MCI \_ Laden](mci-load.md) " angegebenen Datei ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-158">Obtains the path and filename of the last file specified with the [MCI\_OPEN](mci-open.md) or [MCI\_LOAD](mci-load.md) command.</span></span> <span data-ttu-id="26eb9-159">Wenn keine Datei angegeben wurde, gibt das Gerät eine NULL-terminierte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="26eb9-159">If a file has not been specified, the device returns a null-terminated string.</span></span> <span data-ttu-id="26eb9-160">Dieses Flag wird nur von Geräten unterstützt, die " **true** " zurückgeben, um das MCI- \_ Flag "getdevcaps \_ verwendet Dateien" \_ des Befehls [MCI \_ getdevcaps](mci-getdevcaps.md) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="26eb9-160">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

<span data-ttu-id="26eb9-161">Für Digital Video-Geräte verweist *lpInfo* auf eine [**MCI- \_ DGV \_ - \_ Informations**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="26eb9-161">For digital-video devices, *lpInfo* points to an [**MCI\_DGV\_INFO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) structure.</span></span>

<span data-ttu-id="26eb9-162">Die folgenden zusätzlichen Flags gelten für den Typ des **Sequencer** -Geräts:</span><span class="sxs-lookup"><span data-stu-id="26eb9-162">The following additional flags apply to the **sequencer** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26eb9-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI- \_ Informationen \_ Copyright</span><span class="sxs-lookup"><span data-stu-id="26eb9-163"><span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>MCI\_INFO\_COPYRIGHT</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-164">Ruft den Urheberrechts Hinweis der MIDI-Datei aus dem Copyright-Meta-Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-164">Obtains the MIDI file copyright notice from the copyright meta event.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ - \_ Infodatei</span><span class="sxs-lookup"><span data-stu-id="26eb9-165"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-166">Ruft den Dateinamen der aktuellen Datei ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-166">Obtains the filename of the current file.</span></span> <span data-ttu-id="26eb9-167">Dieses Flag wird nur von Geräten unterstützt, die " **true** " zurückgeben, wenn Sie den [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl mit dem Flag "MCI \_ getdevcaps \_ verwendet Files" aufrufen \_ .</span><span class="sxs-lookup"><span data-stu-id="26eb9-167">This flag is supported only by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI- \_ Informations \_ Name</span><span class="sxs-lookup"><span data-stu-id="26eb9-168"><span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>MCI\_INFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-169">Ruft den Sequenznamen aus dem Meta-Ereignis für das Sequenz-/Track-Name ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-169">Obtains the sequence name from the sequence/track name meta event.</span></span>

</dd> </dl>

<span data-ttu-id="26eb9-170">Das folgende zusätzliche Flag gilt für den **VCR** -Gerätetyp:</span><span class="sxs-lookup"><span data-stu-id="26eb9-170">The following additional flag applies to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26eb9-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI \_ VCR- \_ Informations \_ Version</span><span class="sxs-lookup"><span data-stu-id="26eb9-171"><span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>MCI\_VCR\_INFO\_VERSION</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-172">Legt den **lpstraureturn** -Member der [**MCI- \_ Info- \_**](mci-info-parms.md) Parameter-Struktur auf die Versionsnummer fest.</span><span class="sxs-lookup"><span data-stu-id="26eb9-172">Sets **lpstrReturn** member of the [**MCI\_INFO\_PARMS**](mci-info-parms.md) structure to point to the version number.</span></span> <span data-ttu-id="26eb9-173">Legt außerdem den **dwretsize** -Member auf die Länge der Zeichenfolge fest, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="26eb9-173">Also sets the **dwRetSize** member equal to the length of the string pointed to.</span></span>

</dd> </dl>

<span data-ttu-id="26eb9-174">Die folgenden zusätzlichen Flags gelten für den **Überlagerungs** Gerätetyp:</span><span class="sxs-lookup"><span data-stu-id="26eb9-174">The following additional flags apply to the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26eb9-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ - \_ Infodatei</span><span class="sxs-lookup"><span data-stu-id="26eb9-175"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-176">Ruft den Dateinamen der aktuellen Datei ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-176">Obtains the filename of the current file.</span></span> <span data-ttu-id="26eb9-177">Dieses Flag wird nur von Geräten unterstützt, die " **true** " zurückgeben, um das MCI- \_ Flag "getdevcaps \_ verwendet Dateien" \_ des Befehls [MCI \_ getdevcaps](mci-getdevcaps.md) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="26eb9-177">This flag is supported only by devices that return **TRUE** to the MCI\_GETDEVCAPS\_USES\_FILES flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI- \_ OVLY- \_ Info \_ Text</span><span class="sxs-lookup"><span data-stu-id="26eb9-178"><span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>MCI\_OVLY\_INFO\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-179">Ruft die Beschriftung des Fensters ab, das dem Video Überlagerungs Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="26eb9-179">Obtains the caption of the window associated with the video-overlay device.</span></span>

</dd> </dl>

<span data-ttu-id="26eb9-180">Die folgenden zusätzlichen Flags gelten für den **waveaudiogerätetyp** :</span><span class="sxs-lookup"><span data-stu-id="26eb9-180">The following additional flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="26eb9-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI \_ - \_ Infodatei</span><span class="sxs-lookup"><span data-stu-id="26eb9-181"><span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>MCI\_INFO\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-182">Ruft den Dateinamen der aktuellen Datei ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-182">Obtains the filename of the current file.</span></span> <span data-ttu-id="26eb9-183">Dieses Flag wird von Geräten unterstützt, die " **true** " zurückgeben, wenn Sie den [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl mit dem Flag "MCI \_ getdevcaps \_ verwendet Files" aufrufen \_ .</span><span class="sxs-lookup"><span data-stu-id="26eb9-183">This flag is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_USES\_FILES flag.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI- \_ Wave- \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="26eb9-184"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-185">Ruft den Produktnamen der aktuellen Eingabe ab.</span><span class="sxs-lookup"><span data-stu-id="26eb9-185">Obtains the product name of the current input.</span></span>

</dd> <dt>

<span data-ttu-id="26eb9-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI- \_ Wave- \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="26eb9-186"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="26eb9-187">Ruft den Produktnamen der aktuellen Ausgabe ab, und sein Wert ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="26eb9-187">Obtains the product name of the current output and its value is device specific.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26eb9-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26eb9-188">Requirements</span></span>



| <span data-ttu-id="26eb9-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26eb9-189">Requirement</span></span> | <span data-ttu-id="26eb9-190">Wert</span><span class="sxs-lookup"><span data-stu-id="26eb9-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26eb9-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26eb9-191">Minimum supported client</span></span><br/> | <span data-ttu-id="26eb9-192">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26eb9-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="26eb9-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26eb9-193">Minimum supported server</span></span><br/> | <span data-ttu-id="26eb9-194">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26eb9-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="26eb9-195">Header</span><span class="sxs-lookup"><span data-stu-id="26eb9-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="26eb9-196"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26eb9-196"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26eb9-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26eb9-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26eb9-198">MCI</span><span class="sxs-lookup"><span data-stu-id="26eb9-198">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="26eb9-199">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="26eb9-199">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

