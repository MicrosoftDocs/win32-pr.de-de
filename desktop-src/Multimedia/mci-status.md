---
title: MCI_STATUS Befehl (MMSYSTEM. h)
description: Der MCI- \_ Status Befehl ruft Informationen zu einem MCI-Gerät ab. Alle Geräte erkennen diesen Befehl. Informationen werden im dwreturn-Member der Struktur zurückgegeben, die durch den lpstatus-Parameter identifiziert wird.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- MCI_STATUS Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "104350689"
---
# <a name="mci_status-command"></a><span data-ttu-id="fe79c-106">Befehl "MCI- \_ Status"</span><span class="sxs-lookup"><span data-stu-id="fe79c-106">MCI\_STATUS command</span></span>

> [!NOTE]
> <span data-ttu-id="fe79c-107">Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.</span><span class="sxs-lookup"><span data-stu-id="fe79c-107">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="fe79c-108">In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-108">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="fe79c-109">Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-109">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="fe79c-110">Dieser Wortlaut wird verwendet, da es sich zurzeit um den in den Befehlen verwendeten Wortlaut handelt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-110">This wording is used as it is currently the wording used within the commands.</span></span> <span data-ttu-id="fe79c-111">Aus Konsistenz Gründen enthält dieses Dokument dieses Wort.</span><span class="sxs-lookup"><span data-stu-id="fe79c-111">For consistency, this document contains this word.</span></span> <span data-ttu-id="fe79c-112">Wenn dieses Wort in den Befehlen geändert wird, korrigieren wir dieses Dokument als Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="fe79c-112">When this word is altered in the commands, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="fe79c-113">Der MCI- \_ Status Befehl ruft Informationen zu einem MCI-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="fe79c-113">The MCI\_STATUS command retrieves information about an MCI device.</span></span> <span data-ttu-id="fe79c-114">Alle Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="fe79c-114">All devices recognize this command.</span></span> <span data-ttu-id="fe79c-115">Informationen werden im **dwreturn** -Member der Struktur zurückgegeben, die durch den *lpstatus* -Parameter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-115">Information is returned in the **dwReturn** member of the structure identified by the *lpStatus* parameter.</span></span>

<span data-ttu-id="fe79c-116">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="fe79c-116">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a><span data-ttu-id="fe79c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe79c-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="fe79c-118"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-119">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="fe79c-119">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="fe79c-120"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-121">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="fe79c-121">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="fe79c-122">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fe79c-122">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpstatus*</span><span class="sxs-lookup"><span data-stu-id="fe79c-123"><span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-124">Zeiger auf eine [**MCI \_ - \_ statusparametstruktur**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="fe79c-124">Pointer to an [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure.</span></span> <span data-ttu-id="fe79c-125">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="fe79c-125">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe79c-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe79c-126">Return Value</span></span>

<span data-ttu-id="fe79c-127">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="fe79c-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe79c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe79c-128">Remarks</span></span>

<span data-ttu-id="fe79c-129">Die folgenden zusätzlichen Standard-und Befehls spezifischen Flags gelten für alle Geräte, die den MCI-Status unterstützen \_ :</span><span class="sxs-lookup"><span data-stu-id="fe79c-129">The following additional standard and command-specific flags apply to all devices supporting MCI\_STATUS:</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI- \_ Status \_ Element</span><span class="sxs-lookup"><span data-stu-id="fe79c-130"><span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>MCI\_STATUS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-131">Gibt an, dass der **dwitem** -Member der durch *lpstatus* identifizierten Struktur eine Konstante enthält, die das abzurufende Status Element angibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-131">Specifies that the **dwItem** member of the structure identified by *lpStatus* contains a constant specifying which status item to obtain.</span></span> <span data-ttu-id="fe79c-132">Die folgenden Konstanten definieren, welches Status Element im **dwreturn** -Member der-Struktur zurückgegeben werden soll:</span><span class="sxs-lookup"><span data-stu-id="fe79c-132">The following constants define which status item to return in the **dwReturn** member of the structure:</span></span>

<span data-ttu-id="fe79c-133">MCI- \_ Status, \_ aktueller \_ Titel</span><span class="sxs-lookup"><span data-stu-id="fe79c-133">MCI\_STATUS\_CURRENT\_TRACK</span></span>

<span data-ttu-id="fe79c-134">Der **dwreturn** -Member wird auf die aktuelle Nachverfolgung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-134">The **dwReturn** member is set to the current track number.</span></span> <span data-ttu-id="fe79c-135">MCI verwendet kontinuierliche Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="fe79c-135">MCI uses continuous track numbers.</span></span>

<span data-ttu-id="fe79c-136">MCI- \_ Status \_ Länge</span><span class="sxs-lookup"><span data-stu-id="fe79c-136">MCI\_STATUS\_LENGTH</span></span>

<span data-ttu-id="fe79c-137">Der **dwreturn** -Member ist auf die Gesamt Medien Länge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-137">The **dwReturn** member is set to the total media length.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI- \_ Status \_ Modus</span><span class="sxs-lookup"><span data-stu-id="fe79c-138"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-139">Der **dwreturn** -Member ist auf den aktuellen Modus des Geräts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-139">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="fe79c-140">Die Modi umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fe79c-140">The modes include the following:</span></span>

-   <span data-ttu-id="fe79c-141">MCI- \_ Modus \_ nicht \_ bereit</span><span class="sxs-lookup"><span data-stu-id="fe79c-141">MCI\_MODE\_NOT\_READY</span></span>
-   <span data-ttu-id="fe79c-142">MCI- \_ Modus anhalten \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-142">MCI\_MODE\_PAUSE</span></span>
-   <span data-ttu-id="fe79c-143">MCI- \_ Modus \_ abspielen</span><span class="sxs-lookup"><span data-stu-id="fe79c-143">MCI\_MODE\_PLAY</span></span>
-   <span data-ttu-id="fe79c-144">MCI- \_ Modus wird \_ beendet</span><span class="sxs-lookup"><span data-stu-id="fe79c-144">MCI\_MODE\_STOP</span></span>
-   <span data-ttu-id="fe79c-145">MCI- \_ Modus \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="fe79c-145">MCI\_MODE\_OPEN</span></span>
-   <span data-ttu-id="fe79c-146">MCI- \_ Modus- \_ Datensatz</span><span class="sxs-lookup"><span data-stu-id="fe79c-146">MCI\_MODE\_RECORD</span></span>
-   <span data-ttu-id="fe79c-147">MCI- \_ Modus- \_ Suche</span><span class="sxs-lookup"><span data-stu-id="fe79c-147">MCI\_MODE\_SEEK</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI- \_ Status \_ Anzahl \_ von \_ Spuren</span><span class="sxs-lookup"><span data-stu-id="fe79c-148"><span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>MCI\_STATUS\_NUMBER\_OF\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-149">Der **dwreturn** -Member ist auf die Gesamtzahl der Wiedergabe baren Spuren festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-149">The **dwReturn** member is set to the total number of playable tracks.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI- \_ Status \_ Position</span><span class="sxs-lookup"><span data-stu-id="fe79c-150"><span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>MCI\_STATUS\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-151">Der **dwreturn** -Member wird auf die aktuelle Position festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-151">The **dwReturn** member is set to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI- \_ Status ist \_ bereit</span><span class="sxs-lookup"><span data-stu-id="fe79c-152"><span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>MCI\_STATUS\_READY</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-153">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät bereit ist. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-153">The **dwReturn** member is set to **TRUE** if the device is ready; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI- \_ Status \_ Zeit \_ Format</span><span class="sxs-lookup"><span data-stu-id="fe79c-154"><span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>MCI\_STATUS\_TIME\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-155">Der **dwreturn** -Member wird auf das aktuelle Zeitformat des Geräts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-155">The **dwReturn** member is set to the current time format of the device.</span></span> <span data-ttu-id="fe79c-156">Zu den Zeitformaten gehören:</span><span class="sxs-lookup"><span data-stu-id="fe79c-156">The time formats include:</span></span>

-   <span data-ttu-id="fe79c-157">MCI- \_ Format ( \_ Bytes)</span><span class="sxs-lookup"><span data-stu-id="fe79c-157">MCI\_FORMAT\_BYTES</span></span>
-   <span data-ttu-id="fe79c-158">MCI- \_ Formatierungs \_ Frames</span><span class="sxs-lookup"><span data-stu-id="fe79c-158">MCI\_FORMAT\_FRAMES</span></span>
-   <span data-ttu-id="fe79c-159">MCI- \_ Format \_ HMS</span><span class="sxs-lookup"><span data-stu-id="fe79c-159">MCI\_FORMAT\_HMS</span></span>
-   <span data-ttu-id="fe79c-160">MCI- \_ Format ( \_ Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="fe79c-160">MCI\_FORMAT\_MILLISECONDS</span></span>
-   <span data-ttu-id="fe79c-161">MCI- \_ Format \_ MSF</span><span class="sxs-lookup"><span data-stu-id="fe79c-161">MCI\_FORMAT\_MSF</span></span>
-   <span data-ttu-id="fe79c-162">MCI- \_ Format \_ Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe79c-162">MCI\_FORMAT\_SAMPLES</span></span>
-   <span data-ttu-id="fe79c-163">MCI- \_ Format- \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="fe79c-163">MCI\_FORMAT\_TMSF</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI- \_ Status \_ Start</span><span class="sxs-lookup"><span data-stu-id="fe79c-164"><span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>MCI\_STATUS\_START</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-165">Ruft die Anfangsposition des Mediums ab.</span><span class="sxs-lookup"><span data-stu-id="fe79c-165">Obtains the starting position of the media.</span></span> <span data-ttu-id="fe79c-166">Um die Anfangsposition abzurufen, kombinieren Sie dieses Flag mit dem MCI \_ \_ -Status Element, und legen Sie das **dwitem** -Member der durch *lpstatus* identifizierten Struktur auf die MCI- \_ Status Position fest \_ .</span><span class="sxs-lookup"><span data-stu-id="fe79c-166">To get the starting position, combine this flag with MCI\_STATUS\_ITEM and set the **dwItem** member of the structure identified by *lpStatus* to MCI\_STATUS\_POSITION.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI- \_ Track</span><span class="sxs-lookup"><span data-stu-id="fe79c-167"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-168">Gibt an, dass ein Status Nachverfolgung-Parameter im **dwtrack** -Member der durch *lpstatus* identifizierten Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-168">Indicates a status track parameter is included in the **dwTrack** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="fe79c-169">Sie müssen dieses Flag mit der MCI- \_ Status \_ Position oder den MCI- \_ Status \_ Längen Konstanten verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-169">You must use this flag with the MCI\_STATUS\_POSITION or MCI\_STATUS\_LENGTH constants.</span></span> <span data-ttu-id="fe79c-170">Bei Verwendung mit der MCI- \_ Status \_ Position erhält die MCI- \_ Verfolgung die Anfangs Position des angegebenen Titels. Bei Verwendung mit der MCI- \_ Status \_ Länge erhält die MCI-nach \_ Verfolgung die Länge des angegebenen Titels. MCI verwendet kontinuierliche Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="fe79c-170">When used with MCI\_STATUS\_POSITION, MCI\_TRACK obtains the starting position of the specified track. When used with MCI\_STATUS\_LENGTH, MCI\_TRACK obtains the length of the specified track. MCI uses continuous track numbers.</span></span>

</dd> </dl>

<span data-ttu-id="fe79c-171">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp **CDAudio** verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-171">The following additional flags are used with the **cdaudio** device type.</span></span> <span data-ttu-id="fe79c-172">Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-172">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI- \_ CDA- \_ \_ Statustyp \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="fe79c-173"><span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>MCI\_CDA\_STATUS\_TYPE\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-174">Der **dwreturn** -Member ist auf einen der folgenden Werte festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fe79c-174">The **dwReturn** member is set to one of the following values:</span></span>

-   <span data-ttu-id="fe79c-175">MCI \_ \_ -CDA \_ -trackaudiodatei</span><span class="sxs-lookup"><span data-stu-id="fe79c-175">MCI\_CDA\_TRACK\_AUDIO</span></span>
-   <span data-ttu-id="fe79c-176">MCI-CDA-nach \_ \_ Verfolgung \_ anderer</span><span class="sxs-lookup"><span data-stu-id="fe79c-176">MCI\_CDA\_TRACK\_OTHER</span></span>

<span data-ttu-id="fe79c-177">Um dieses Flag zu verwenden, muss das MCI \_ -trackflag festgelegt werden, und das **dwtrack** -Element der durch *lpstatus* identifizierten Struktur muss eine gültige Nachverfolgung enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe79c-177">To use this flag, the MCI\_TRACK flag must be set, and the **dwTrack** member of the structure identified by *lpStatus* must contain a valid track number.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fe79c-178"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-179">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-179">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="fe79c-180">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="fe79c-180">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI \_ DGV- \_ Status \_ diskspace</span><span class="sxs-lookup"><span data-stu-id="fe79c-181"><span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>MCI\_DGV\_STATUS\_DISKSPACE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-182">Der **lpstraudrive** -Member der Struktur, die von *lpstatus* identifiziert wird, gibt ein Laufwerk oder in einigen Implementierungen einen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="fe79c-182">The **lpstrDrive** member of the structure identified by *lpStatus* specifies a disk drive or, in some implementations, a path.</span></span> <span data-ttu-id="fe79c-183">Der MCI- \_ Status Befehl gibt die ungefähre Menge an Speicherplatz zurück, die durch den [MCI- \_ Reserve](mci-reserve.md) Befehl im **dwreturn** -Member der durch *lpstatus* identifizierten Struktur abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe79c-183">The MCI\_STATUS command returns the approximate amount of disk space that could be obtained by the [MCI\_RESERVE](mci-reserve.md) command in the **dwReturn** member of the structure identified by *lpStatus*.</span></span> <span data-ttu-id="fe79c-184">Der Speicherplatz wird in Einheiten des aktuellen Zeit Formats gemessen.</span><span class="sxs-lookup"><span data-stu-id="fe79c-184">The disk space is measured in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI- \_ DGV- \_ Status \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe79c-185"><span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>MCI\_DGV\_STATUS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-186">Die vom **lengertem** -Member der durch *lpstatus* identifizierte-Konstante gilt für die Eingabe.</span><span class="sxs-lookup"><span data-stu-id="fe79c-186">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the input.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI- \_ DGV- \_ Status \_ Links</span><span class="sxs-lookup"><span data-stu-id="fe79c-187"><span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>MCI\_DGV\_STATUS\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-188">Die vom **lengertem** -Member der durch *lpstatus* identifizierte-Konstante gilt für den linken Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="fe79c-188">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI \_ DGV- \_ Status \_ nominell</span><span class="sxs-lookup"><span data-stu-id="fe79c-189"><span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>MCI\_DGV\_STATUS\_NOMINAL</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-190">Die durch den **lengertem** -Member der-Struktur angegebene Konstante, die von *lpstatus* identifiziert wird, fordert den nominalen Wert anstelle des aktuellen Werts an.</span><span class="sxs-lookup"><span data-stu-id="fe79c-190">The constant specified by the **dwItem** member of the structure identified by *lpStatus* requests the nominal value rather than the current value.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI- \_ DGV- \_ Status \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fe79c-191"><span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>MCI\_DGV\_STATUS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-192">Die vom **lengertem** -Member der durch *lpstatus* identifizierte-Konstante gilt für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="fe79c-192">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the output.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI- \_ DGV- \_ Status \_ Daten Satz</span><span class="sxs-lookup"><span data-stu-id="fe79c-193"><span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>MCI\_DGV\_STATUS\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-194">Die für das MCI \_ DGV-statusraten-Flag zurückgegebene Frame Rate \_ \_ \_ ist die für die Komprimierung verwendete Rate.</span><span class="sxs-lookup"><span data-stu-id="fe79c-194">The frame rate returned for the MCI\_DGV\_STATUS\_FRAME\_RATE flag is the rate used for compression.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI \_ DGV- \_ Status \_ Referenz</span><span class="sxs-lookup"><span data-stu-id="fe79c-195"><span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>MCI\_DGV\_STATUS\_REFERENCE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-196">Der **dwreturn** -Member der Struktur, die von *lpstatus* identifiziert wird, gibt das nächste Keyframe-Bild zurück, das dem im **dwreference** -Member angegebenen Frame vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-196">The **dwReturn** member of the structure identified by *lpStatus* returns the nearest key-frame image that precedes the frame specified in the **dwReference** member.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI- \_ DGV- \_ Status \_ Recht</span><span class="sxs-lookup"><span data-stu-id="fe79c-197"><span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>MCI\_DGV\_STATUS\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-198">Die vom **lengertem** -Member der durch *lpstatus* identifizierte-Konstante gilt für den richtigen Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="fe79c-198">The constant specified by the **dwItem** member of the structure identified by *lpStatus* applies to the right audio channel.</span></span>

</dd> </dl>

<span data-ttu-id="fe79c-199">Die folgenden Konstanten werden mit dem **Digitalvideo** -Gerätetyp im **dwitem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-199">The following constants are used with the **digitalvideo** device type in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI \_ \_ -AVI \_ -Status- \_ audioumbrüche</span><span class="sxs-lookup"><span data-stu-id="fe79c-200"><span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>MCI\_AVI\_STATUS\_AUDIO\_BREAKS</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-201">Der **dwreturn** -Member gibt an, wie oft der Audioteil der letzten AVI-Sequenz abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="fe79c-201">The **dwReturn** member returns the number of times the audio portion of the last AVI sequence broke up.</span></span> <span data-ttu-id="fe79c-202">Das System zählt immer dann eine audiopause, wenn versucht wird, Audiodaten in den Gerätetreiber zu schreiben und feststellt, dass der Treiber bereits alle verfügbaren Daten wiedergegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fe79c-202">The system counts an audio break whenever it attempts to write audio data to the device driver and discovers that the driver has already played all of the available data.</span></span> <span data-ttu-id="fe79c-203">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-203">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI \_ AVI- \_ Status \_ Frames \_ übersprungen</span><span class="sxs-lookup"><span data-stu-id="fe79c-204"><span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>MCI\_AVI\_STATUS\_FRAMES\_SKIPPED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-205">Der **dwreturn** -Member gibt die Anzahl der Frames zurück, die beim Abspielen der letzten AVI-Sequenz nicht gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-205">The **dwReturn** member returns the number of frames that were not drawn when the last AVI sequence was played.</span></span> <span data-ttu-id="fe79c-206">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-206">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI \_ AVI \_ Status \_ Letzte \_ Wiedergabe \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="fe79c-207"><span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>MCI\_AVI\_STATUS\_LAST\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-208">Der **dwreturn** -Member gibt einen Wert zurück, der angibt, wie genau die tatsächliche Wiedergabezeit der letzten AVI-Sequenz mit der Ziel Wiedergabezeit übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-208">The **dwReturn** member returns a value representing how closely the actual playing time of the last AVI sequence matched the target playing time.</span></span> <span data-ttu-id="fe79c-209">Der Wert 1000 gibt an, dass die Zielzeit und die tatsächliche zeitgleich sind.</span><span class="sxs-lookup"><span data-stu-id="fe79c-209">The value 1000 indicates that the target time and the actual time were the same.</span></span> <span data-ttu-id="fe79c-210">Der Wert 2000 gibt z. b. an, dass die AVI-Sequenz zweimal so lange gedauert hat, wie Sie vorhanden sein sollte.</span><span class="sxs-lookup"><span data-stu-id="fe79c-210">A value of 2000, for example, would indicate that the AVI sequence took twice as long to play as it should have.</span></span> <span data-ttu-id="fe79c-211">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-211">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI \_ DGV \_ \_ -statusaudiodatei</span><span class="sxs-lookup"><span data-stu-id="fe79c-212"><span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>MCI\_DGV\_STATUS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-213">Der **dwreturn** -Member gibt MCI \_ on oder MCI \_ aus, abhängig von der aktuellen MCI \_ Set \_ -Audiooption für den [MCI \_ Set](mci-set.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="fe79c-213">The **dwReturn** member returns MCI\_ON or MCI\_OFF depending on the most recent MCI\_SET\_AUDIO option for the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="fe79c-214">Sie gibt MCI \_ für zurück, wenn entweder oder beide Redner aktiviert sind, andernfalls MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="fe79c-214">It returns MCI\_ON if either or both speakers are enabled, and MCI\_OFF otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI \_ \_ -DGV \_ -Status- \_ Audioeingabe</span><span class="sxs-lookup"><span data-stu-id="fe79c-215"><span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>MCI\_DGV\_STATUS\_AUDIO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-216">Der **dwreturn** -Member gibt die ungefähre sofortige Audioebene des analogen Audiosignals zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-216">The **dwReturn** member returns the approximate instantaneous audio level of the analog audio signal.</span></span> <span data-ttu-id="fe79c-217">Ein Wert größer als 1000 impliziert, dass eine clippingverzerrung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-217">A value greater than 1000 implies there is clipping distortion.</span></span> <span data-ttu-id="fe79c-218">Einige Geräte können diesen Wert nur beim Aufzeichnen von Audiodaten bestimmen.</span><span class="sxs-lookup"><span data-stu-id="fe79c-218">Some devices can determine this value only while recording audio.</span></span> <span data-ttu-id="fe79c-219">Diesem Statuswert ist kein zugeordneter **MCI- \_ Satz** oder [MCI \_ -setaudiobefehl](mci-setaudio.md) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-219">This status value has no associated **MCI\_SET** or [MCI\_SETAUDIO](mci-setaudio.md) command.</span></span> <span data-ttu-id="fe79c-220">Dieser Wert bezieht sich auf die MCI-Wave-Status Ebene des Waveform-audiobefehls, die jedoch anders normalisiert ist \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fe79c-220">This value is related to, but normalized differently from, the waveform-audio command MCI\_WAVE\_STATUS\_LEVEL.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI \_ \_ -DGV \_ -Status- \_ audiodatensatz</span><span class="sxs-lookup"><span data-stu-id="fe79c-221"><span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>MCI\_DGV\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-222">Der **dwreturn** -Member gibt MCI \_ on oder MCI off zurück, wobei \_ der Status des MCI \_ DGV \_ \_ setaudiodatensatz-Flags des **MCI \_ setaudiobefehls** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-222">The **dwReturn** member returns MCI\_ON or MCI\_OFF reflecting the state set by the MCI\_DGV\_SETAUDIO\_RECORD flag of the **MCI\_SETAUDIO** command.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI \_ \_ -DGV \_ -statusaudioquelle \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-223"><span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>MCI\_DGV\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-224">Der **dwreturn** -Member gibt die aktuelle audiodigitalisierungs Quelle zurück:</span><span class="sxs-lookup"><span data-stu-id="fe79c-224">The **dwReturn** member returns the current audio digitizer source:</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI- \_ DGV \_ - \_ setaudiodurchschnitt</span><span class="sxs-lookup"><span data-stu-id="fe79c-225"><span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>MCI\_DGV\_SETAUDIO\_AVERAGE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-226">Gibt den Durchschnitt des linken und rechten Audiokanals an.</span><span class="sxs-lookup"><span data-stu-id="fe79c-226">Specifies the average of the left and right audio channels.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ \_ setaudiolinks</span><span class="sxs-lookup"><span data-stu-id="fe79c-227"><span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI\_DGV\_SETAUDIO\_LEFT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-228">Gibt den linken Audiokanal an.</span><span class="sxs-lookup"><span data-stu-id="fe79c-228">Specifies the left audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ \_ setaudioright</span><span class="sxs-lookup"><span data-stu-id="fe79c-229"><span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI\_DGV\_SETAUDIO\_RIGHT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-230">Gibt den richtigen Audiokanal an.</span><span class="sxs-lookup"><span data-stu-id="fe79c-230">Specifies the right audio channel.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ \_ setaudiostereo</span><span class="sxs-lookup"><span data-stu-id="fe79c-231"><span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI\_DGV\_SETAUDIO\_STEREO</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-232">Gibt Stereo an.</span><span class="sxs-lookup"><span data-stu-id="fe79c-232">Specifies stereo.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI \_ \_ -DGV \_ -statusaudiostream \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-233"><span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>MCI\_DGV\_STATUS\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-234">Der **dwreturn** -Member gibt die aktuelle audiostreamnummer zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-234">The **dwReturn** member returns the current audio-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI \_ DGV- \_ Status \_ avgbytespersec</span><span class="sxs-lookup"><span data-stu-id="fe79c-235"><span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>MCI\_DGV\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-236">Der **dwreturn** -Member gibt die durchschnittliche Anzahl der Bytes zurück, die pro Sekunde für die Aufzeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-236">The **dwReturn** member returns the average number of bytes per second used for recording.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI \_ DGV- \_ Status- \_ Bass</span><span class="sxs-lookup"><span data-stu-id="fe79c-237"><span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>MCI\_DGV\_STATUS\_BASS</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-238">Der **dwreturn** -Member gibt die aktuelle audiobass-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-238">The **dwReturn** member returns the current audio bass level.</span></span> <span data-ttu-id="fe79c-239">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-239">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI \_ DGV- \_ Status \_ BitsPerPel</span><span class="sxs-lookup"><span data-stu-id="fe79c-240"><span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>MCI\_DGV\_STATUS\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-241">Das **dwreturn** -Element gibt die Anzahl der Bits pro Pixel zurück, die zum Speichern von aufgezeichneten oder aufgezeichneten Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-241">The **dwReturn** member returns the number of bits per pixel used for saving captured or recorded data.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI \_ DGV- \_ Status \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="fe79c-242"><span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>MCI\_DGV\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-243">Das **dwreturn** -Element gibt die Anzahl der Bits pro Stichprobe zurück, die vom Gerät für die Aufzeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-243">The **dwReturn** member returns the number of bits per sample the device uses for recording.</span></span> <span data-ttu-id="fe79c-244">Dies gilt nur für Geräte, die das PCM-Format unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fe79c-244">This applies only to devices supporting the PCM format.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI- \_ DGV- \_ Status \_ BlockAlign</span><span class="sxs-lookup"><span data-stu-id="fe79c-245"><span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>MCI\_DGV\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-246">Der **dwreturn** -Member gibt die Ausrichtung von Datenblöcken relativ zum Anfang der Eingabe Wellenform zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-246">The **dwReturn** member returns the alignment of data blocks relative to the start of the input waveform.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI- \_ DGV- \_ Status \_ Helligkeit</span><span class="sxs-lookup"><span data-stu-id="fe79c-247"><span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>MCI\_DGV\_STATUS\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-248">Der **dwreturn** -Member gibt die aktuelle videohelligkeits Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-248">The **dwReturn** member returns the current video brightness level.</span></span> <span data-ttu-id="fe79c-249">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-249">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI \_ DGV- \_ Status \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="fe79c-250"><span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>MCI\_DGV\_STATUS\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-251">Der **dwreturn** -Member gibt die aktuelle Farb Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-251">The **dwReturn** member returns the current color level.</span></span> <span data-ttu-id="fe79c-252">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-252">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI- \_ DGV- \_ Status \_ Kontrast</span><span class="sxs-lookup"><span data-stu-id="fe79c-253"><span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>MCI\_DGV\_STATUS\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-254">Der **dwreturn** -Member gibt die aktuelle Kontrast Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-254">The **dwReturn** member returns the current contrast level.</span></span> <span data-ttu-id="fe79c-255">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-255">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI \_ DGV- \_ Status \_ Dateiformat</span><span class="sxs-lookup"><span data-stu-id="fe79c-256"><span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>MCI\_DGV\_STATUS\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-257">Der **dwreturn** -Member gibt das aktuelle Dateiformat für die Aufzeichnung oder Speicherung zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-257">The **dwReturn** member returns the current file format for recording or saving.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI- \_ DGV- \_ Status \_ Datei \_ Modus</span><span class="sxs-lookup"><span data-stu-id="fe79c-258"><span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>MCI\_DGV\_STATUS\_FILE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-259">Der **dwreturn** -Member gibt den Status des Datei Vorgangs zurück:</span><span class="sxs-lookup"><span data-stu-id="fe79c-259">The **dwReturn** member returns the state of the file operation:</span></span>

<span data-ttu-id="fe79c-260">MCI- \_ DGV- \_ dateimodusbearbeitung \_ \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-260">MCI\_DGV\_FILE\_MODE\_EDITING</span></span>

<span data-ttu-id="fe79c-261">Wird beim Ausschneiden, kopieren, löschen, einfügen und rückgängig-Vorgängen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe79c-261">Returned during cut, copy, delete, paste, and undo operations.</span></span>

<span data-ttu-id="fe79c-262">MCI- \_ DGV- \_ Datei \_ Modus im \_ Leerlauf</span><span class="sxs-lookup"><span data-stu-id="fe79c-262">MCI\_DGV\_FILE\_MODE\_IDLE</span></span>

<span data-ttu-id="fe79c-263">Wird zurückgegeben, wenn die Datei für den nächsten Vorgang bereit ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-263">Returned when the file is ready for the next operation.</span></span>

<span data-ttu-id="fe79c-264">MCI- \_ DGV- \_ Datei \_ Modus wird \_ geladen</span><span class="sxs-lookup"><span data-stu-id="fe79c-264">MCI\_DGV\_FILE\_MODE\_LOADING</span></span>

<span data-ttu-id="fe79c-265">Wird beim Laden der Datei zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe79c-265">Returned while the file is being loaded.</span></span>

<span data-ttu-id="fe79c-266">MCI- \_ DGV- \_ Datei \_ Modus \_ Speichern</span><span class="sxs-lookup"><span data-stu-id="fe79c-266">MCI\_DGV\_FILE\_MODE\_SAVING</span></span>

<span data-ttu-id="fe79c-267">Wird zurückgegeben, während die Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-267">Returned while the file is being saved.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI- \_ DGV- \_ Status \_ Datei \_ Abschluss</span><span class="sxs-lookup"><span data-stu-id="fe79c-268"><span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>MCI\_DGV\_STATUS\_FILE\_COMPLETION</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-269">Der **dwreturn** -Member gibt den geschätzten Prozentsatz für das Laden, speichern, erfassen, Ausschneiden, kopieren, löschen, einfügen oder Rückgängig-Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="fe79c-269">The **dwReturn** member returns the estimated percentage a load, save, capture, cut, copy, delete, paste, or undo operation has progressed.</span></span> <span data-ttu-id="fe79c-270">(Anwendungen können dies verwenden, um einen visuellen Indikator für den Fortschritt bereitzustellen.) Dieses Flag wird nicht von allen Digital-Video-Geräten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-270">(Applications can use this to provide a visual indicator of progress.) This flag is not supported by all digital-video devices.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI- \_ DGV- \_ Status \_ Vorwärts</span><span class="sxs-lookup"><span data-stu-id="fe79c-271"><span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>MCI\_DGV\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-272">Der **dwreturn** -Member gibt **true** zurück, wenn die Geräte Richtung vorwärts oder das Gerät nicht wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-272">The **dwReturn** member returns **TRUE** if the device direction is forward or the device is not playing.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI \_ DGV- \_ Status- \_ Frame \_ Rate</span><span class="sxs-lookup"><span data-stu-id="fe79c-273"><span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>MCI\_DGV\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-274">Das **dwreturn** -Element muss mit dem MCI \_ DGV- \_ Status " \_ nominell", dem MCI \_ DGV- \_ Status \_ Daten Satz oder beidem verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-274">The **dwReturn** member must be used with MCI\_DGV\_STATUS\_NOMINAL, MCI\_DGV\_STATUS\_RECORD, or both.</span></span> <span data-ttu-id="fe79c-275">Bei der Verwendung mit dem MCI \_ DGV- \_ Status \_ Daten Satz wird die aktuelle für die Aufzeichnung verwendete Frame Rate zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe79c-275">When used with MCI\_DGV\_STATUS\_RECORD, the current frame rate used for recording is returned.</span></span> <span data-ttu-id="fe79c-276">Bei Verwendung mit dem MCI \_ DGV \_ \_ -Statusdaten Satz und dem MCI \_ DGV-Status " \_ \_ nominell" wird die nominale Frame Rate zurückgegeben, die dem Eingabe Videosignal zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-276">When used with both MCI\_DGV\_STATUS\_RECORD and MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the input video signal is returned.</span></span> <span data-ttu-id="fe79c-277">Bei Verwendung mit \_ dem nominalen MCI DGV- \_ Status \_ wird die der Datei zugeordnete nominale Frame Rate zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe79c-277">When used with MCI\_DGV\_STATUS\_NOMINAL, the nominal frame rate associated with the file is returned.</span></span> <span data-ttu-id="fe79c-278">In allen Fällen werden die Einheiten in Frames pro Sekunde multipliziert mit 1000.</span><span class="sxs-lookup"><span data-stu-id="fe79c-278">In all cases the units are in frames per second multiplied by 1000.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI \_ DGV- \_ Status \_ Gamma</span><span class="sxs-lookup"><span data-stu-id="fe79c-279"><span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>MCI\_DGV\_STATUS\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-280">Der **dwreturn** -Member gibt den aktuellen Gamma Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-280">The **dwReturn** member returns the current gamma value.</span></span> <span data-ttu-id="fe79c-281">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-281">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI- \_ DGV- \_ Status- \_ hpal</span><span class="sxs-lookup"><span data-stu-id="fe79c-282"><span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>MCI\_DGV\_STATUS\_HPAL</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-283">Der **dwreturn** -Member gibt den ASCII-Dezimalwert für das aktuelle Palettenhandle zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-283">The **dwReturn** member returns the ASCII decimal value for the current palette handle.</span></span> <span data-ttu-id="fe79c-284">Das Handle ist im nieder wertigen Wort des zurückgegebenen Werts enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe79c-284">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI \_ DGV- \_ Status- \_ HWND</span><span class="sxs-lookup"><span data-stu-id="fe79c-285"><span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>MCI\_DGV\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-286">Der **dwreturn** -Member gibt den ASCII-Dezimalwert für das aktuelle explizite oder Standardfenster Handle zurück, das dieser Gerätetreiber Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-286">The **dwReturn** member returns the ASCII decimal value for the current explicit or default window handle associated with this device driver instance.</span></span> <span data-ttu-id="fe79c-287">Das Handle ist im nieder wertigen Wort des zurückgegebenen Werts enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe79c-287">The handle is contained in the low-order word of the returned value.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI- \_ DGV- \_ Status \_ Schlüssel \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="fe79c-288"><span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>MCI\_DGV\_STATUS\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-289">Der **dwreturn** -Member gibt den aktuellen Schlüssel Farbwert zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-289">The **dwReturn** member returns the current key-color value.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI- \_ DGV- \_ Status \_ Schlüssel \_ Index</span><span class="sxs-lookup"><span data-stu-id="fe79c-290"><span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>MCI\_DGV\_STATUS\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-291">Der **dwreturn** -Member gibt den aktuellen Schlüssel Index Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-291">The **dwReturn** member returns the current key-index value.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>Monitor für den MCI- \_ DGV- \_ Status \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-292"><span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>MCI\_DGV\_STATUS\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-293">Der **dwreturn** -Member gibt eine Konstante zurück, die die Quelle der aktuellen Präsentation angibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-293">The **dwReturn** member returns a constant indicating the source of the current presentation.</span></span> <span data-ttu-id="fe79c-294">Die folgenden Konstanten sind definiert:</span><span class="sxs-lookup"><span data-stu-id="fe79c-294">The following constants are defined:</span></span>

<span data-ttu-id="fe79c-295">MCI- \_ DGV- \_ Monitor \_ Datei</span><span class="sxs-lookup"><span data-stu-id="fe79c-295">MCI\_DGV\_MONITOR\_FILE</span></span>

<span data-ttu-id="fe79c-296">Eine Datei ist die Quelle.</span><span class="sxs-lookup"><span data-stu-id="fe79c-296">A file is the source.</span></span>

<span data-ttu-id="fe79c-297">MCI- \_ DGV- \_ Monitor \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe79c-297">MCI\_DGV\_MONITOR\_INPUT</span></span>

<span data-ttu-id="fe79c-298">Die Eingabe ist die Quelle.</span><span class="sxs-lookup"><span data-stu-id="fe79c-298">The input is the source.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI \_ DGV- \_ Status \_ Monitor- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="fe79c-299"><span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>MCI\_DGV\_STATUS\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-300">Der **dwreturn** -Member gibt eine Konstante zurück, die die für die Eingabe Überwachung verwendete Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-300">The **dwReturn** member returns a constant indicating the method used for input monitoring.</span></span> <span data-ttu-id="fe79c-301">Die folgenden Konstanten sind definiert:</span><span class="sxs-lookup"><span data-stu-id="fe79c-301">The following constants are defined:</span></span>

<span data-ttu-id="fe79c-302">MCI \_ DGV- \_ Methode \_ Direct</span><span class="sxs-lookup"><span data-stu-id="fe79c-302">MCI\_DGV\_METHOD\_DIRECT</span></span>

<span data-ttu-id="fe79c-303">Direkte Eingabe Überwachung.</span><span class="sxs-lookup"><span data-stu-id="fe79c-303">Direct input monitoring.</span></span>

<span data-ttu-id="fe79c-304">MCI \_ DGV- \_ Methoden \_ Beitrag</span><span class="sxs-lookup"><span data-stu-id="fe79c-304">MCI\_DGV\_METHOD\_POST</span></span>

<span data-ttu-id="fe79c-305">Überwachung nach der Eingabe.</span><span class="sxs-lookup"><span data-stu-id="fe79c-305">Post-input monitoring.</span></span>

<span data-ttu-id="fe79c-306">MCI \_ DGV- \_ Methode \_ vor</span><span class="sxs-lookup"><span data-stu-id="fe79c-306">MCI\_DGV\_METHOD\_PRE</span></span>

<span data-ttu-id="fe79c-307">Überwachung vor der Eingabe.</span><span class="sxs-lookup"><span data-stu-id="fe79c-307">Pre-input monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI- \_ DGV- \_ Status \_ Pausen \_ Modus</span><span class="sxs-lookup"><span data-stu-id="fe79c-308"><span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>MCI\_DGV\_STATUS\_PAUSE\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-309">Der **dwreturn** -Member gibt die Wiedergabe des MCI \_ -Modus zurück, \_ Wenn das Gerät während der Wiedergabe angehalten wurde, und gibt den MCI- \_ Modus- \_ Datensatz zurück</span><span class="sxs-lookup"><span data-stu-id="fe79c-309">The **dwReturn** member returns MCI\_MODE\_PLAY if the device was paused while playing and returns MCI\_MODE\_RECORD if the device was paused while recording.</span></span> <span data-ttu-id="fe79c-310">Der Befehl gibt die nicht anwendbare mcierr- \_ \_ Funktion als Fehlerrückgabe zurück, wenn das Gerät nicht angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="fe79c-310">The command returns MCIERR\_NONAPPLICABLE\_FUNCTION as an error return if the device is not paused.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI \_ DGV- \_ Status \_ SamplesPerSecond</span><span class="sxs-lookup"><span data-stu-id="fe79c-311"><span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>MCI\_DGV\_STATUS\_SAMPLESPERSECOND</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-312">Das **dwreturn** -Element gibt die Anzahl der Stichproben pro Sekunde zurück, die aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-312">The **dwReturn** member returns the number of samples per second recorded.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI \_ DGV- \_ Status \_ Suche \_ genau</span><span class="sxs-lookup"><span data-stu-id="fe79c-313"><span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>MCI\_DGV\_STATUS\_SEEK\_EXACTLY</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-314">Der **dwreturn** -Member gibt **true** oder **false** zurück, um anzugeben, ob das Such genaue Format festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-314">The **dwReturn** member returns **TRUE** or **FALSE** indicating whether or not the seek exactly format is set.</span></span> <span data-ttu-id="fe79c-315">(Anwendungen können dieses Format mithilfe des Befehls [MCI Set \_ ](mci-set.md) mit dem Flag MCI \_ DGV \_ Set \_ Seek exakt festlegen \_ .)</span><span class="sxs-lookup"><span data-stu-id="fe79c-315">(Applications can set this format by using the [MCI\_SET](mci-set.md) command with the MCI\_DGV\_SET\_SEEK\_EXACTLY flag.)</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI \_ DGV- \_ Status \_ Schärfe</span><span class="sxs-lookup"><span data-stu-id="fe79c-316"><span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>MCI\_DGV\_STATUS\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-317">Der **dwreturn** -Member gibt die aktuelle Schärfe Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-317">The **dwReturn** member returns the current sharpness level.</span></span> <span data-ttu-id="fe79c-318">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-318">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI- \_ DGV- \_ Status \_ Größe</span><span class="sxs-lookup"><span data-stu-id="fe79c-319"><span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>MCI\_DGV\_STATUS\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-320">Der **dwreturn** -Member gibt die ungefähre Wiedergabedauer von komprimierten Daten zurück, die der reservierte Arbeitsbereich enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-320">The **dwReturn** member returns the approximate playback duration of compressed data that the reserved workspace will hold.</span></span> <span data-ttu-id="fe79c-321">Die Dauer Einheiten liegen im aktuellen Zeitformat vor.</span><span class="sxs-lookup"><span data-stu-id="fe79c-321">The duration units are in the current time format.</span></span> <span data-ttu-id="fe79c-322">Wenn kein reservierter Speicherplatz vorhanden ist, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe79c-322">It returns zero if there is no reserved disk space.</span></span> <span data-ttu-id="fe79c-323">Die zurückgegebene Größe ist ungefähre Werte, da der genaue Speicherplatz für komprimierte Daten im allgemeinen erst vorhergesagt werden kann, nachdem die Daten komprimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-323">The size returned is approximate since the precise disk space for compressed data cannot, in general, be predicted until after the data has been compressed.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI- \_ DGV- \_ Status ( \_ SMPTE)</span><span class="sxs-lookup"><span data-stu-id="fe79c-324"><span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>MCI\_DGV\_STATUS\_SMPTE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-325">Der **dwreturn** -Member gibt den SMPTE-Zeit Code zurück, der der aktuellen Position im Arbeitsbereich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-325">The **dwReturn** member returns the SMPTE time code associated with the current position in the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI \_ DGV- \_ Status \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="fe79c-326"><span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>MCI\_DGV\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-327">Der **dwreturn** -Member gibt die aktuelle Wiedergabegeschwindigkeit zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-327">The **dwReturn** member returns the current playback speed.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI- \_ DGV- \_ Status \_ weiterhin \_ Fileformat</span><span class="sxs-lookup"><span data-stu-id="fe79c-328"><span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>MCI\_DGV\_STATUS\_STILL\_FILEFORMAT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-329">Der **dwreturn** -Member gibt das aktuelle Dateiformat für den [MCI- \_ Erfassungs](mci-capture.md) Befehl zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-329">The **dwReturn** member returns the current file format for the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI \_ DGV- \_ Status \_ tint</span><span class="sxs-lookup"><span data-stu-id="fe79c-330"><span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>MCI\_DGV\_STATUS\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-331">Der **dwreturn** -Member gibt die aktuelle Video-Tönungs-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-331">The **dwReturn** member returns the current video tint level.</span></span> <span data-ttu-id="fe79c-332">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-332">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI- \_ DGV- \_ Status \_ Treble</span><span class="sxs-lookup"><span data-stu-id="fe79c-333"><span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>MCI\_DGV\_STATUS\_TREBLE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-334">Der **dwreturn** -Member gibt die aktuelle audiotreble-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-334">The **dwReturn** member returns the current audio treble level.</span></span> <span data-ttu-id="fe79c-335">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-335">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI- \_ DGV- \_ Status \_ nicht gespeichert</span><span class="sxs-lookup"><span data-stu-id="fe79c-336"><span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>MCI\_DGV\_STATUS\_UNSAVED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-337">Der **dwreturn** -Member gibt **true** zurück, wenn im Arbeitsbereich aufgezeichnete Daten verloren gehen, die als Ergebnis eines [MCI \_](mci-close.md)-Schließ Vorgangs, einer [MCI- \_ Auslastung](mci-load.md), eines [MCI-Daten \_ Satzes](mci-record.md), einer [MCI- \_ Reserve](mci-reserve.md), eines [MCI- \_ Ausschnitts](mci-cut.md), einer [MCI- \_ Delete](mci-delete.md)-oder einer [MCI \_](mci-paste.md) -Befehls</span><span class="sxs-lookup"><span data-stu-id="fe79c-337">The **dwReturn** member returns **TRUE** if there is recorded data in the workspace that might be lost as a result of a [MCI\_CLOSE](mci-close.md), [MCI\_LOAD](mci-load.md), [MCI\_RECORD](mci-record.md), [MCI\_RESERVE](mci-reserve.md), [MCI\_CUT](mci-cut.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="fe79c-338">Der Member gibt andernfalls **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-338">The member returns **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>Video zum MCI- \_ DGV- \_ Status \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-339"><span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>MCI\_DGV\_STATUS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-340">Der **dwreturn** -Member gibt MCI in zurück, \_ Wenn das Video aktiviert ist, oder \_ Wenn es deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-340">The **dwReturn** member returns MCI\_ON if video is enabled or MCI\_OFF if it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI- \_ DGV- \_ Status- \_ Video \_ Daten Satz</span><span class="sxs-lookup"><span data-stu-id="fe79c-341"><span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>MCI\_DGV\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-342">Der **dwreturn** -Member gibt MCI \_ on oder MCI \_ Off zurück und gibt den Status an, der vom MCI \_ DGV \_ setvideo-Datensatz- \_ Flag des Befehls [MCI \_ setvideo](mci-setvideo.md) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-342">The **dwReturn** member returns MCI\_ON or MCI\_OFF, reflecting the state set by the MCI\_DGV\_SETVIDEO\_RECORD flag of the [MCI\_SETVIDEO](mci-setvideo.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI- \_ DGV- \_ Status- \_ Video \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="fe79c-343"><span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>MCI\_DGV\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-344">Der **dwreturn** -Member gibt eine Konstante zurück, die den Typ der Videoquelle angibt, die vom MCI \_ DGV \_ setvideo \_ Source-Flag des **MCI \_ setvideo** -Befehls festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe79c-344">The **dwReturn** member returns a constant indicating the type of video source set by the MCI\_DGV\_SETVIDEO\_SOURCE flag of the **MCI\_SETVIDEO** command.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI \_ DGV- \_ Status \_ Video \_ src \_ NUM</span><span class="sxs-lookup"><span data-stu-id="fe79c-345"><span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>MCI\_DGV\_STATUS\_VIDEO\_SRC\_NUM</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-346">Der **dwreturn** -Member gibt die Zahl innerhalb seines Typs der derzeit aktiven Videoeingabe Quelle zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-346">The **dwReturn** member returns the number within its type of the video-input source currently active.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI- \_ DGV- \_ Status- \_ \_ Videostream</span><span class="sxs-lookup"><span data-stu-id="fe79c-347"><span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>MCI\_DGV\_STATUS\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-348">Der **dwreturn** -Member gibt die aktuelle videostreamnummer zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-348">The **dwReturn** member returns the current video-stream number.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI \_ DGV \_ - \_ statusvolume</span><span class="sxs-lookup"><span data-stu-id="fe79c-349"><span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>MCI\_DGV\_STATUS\_VOLUME</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-350">Der **dwreturn** -Member gibt den Durchschnitt des Volumes an den linken und den rechten Redner zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-350">The **dwReturn** member returns the average of the volume to the left and right speakers.</span></span> <span data-ttu-id="fe79c-351">Verwenden \_ Sie den MCI DGV- \_ Status \_ nominell mit diesem Flag zum Abrufen der nominalen Ebene.</span><span class="sxs-lookup"><span data-stu-id="fe79c-351">Use MCI\_DGV\_STATUS\_NOMINAL with this flag to obtain the nominal level.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI- \_ DGV- \_ Status \_ Fenster \_ sichtbar</span><span class="sxs-lookup"><span data-stu-id="fe79c-352"><span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>MCI\_DGV\_STATUS\_WINDOW\_VISIBLE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-353">Der **dwreturn** -Member gibt **true** zurück, wenn das Fenster nicht ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-353">The **dwReturn** member returns **TRUE** if the window is not hidden.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI- \_ DGV- \_ Status \_ Fenster \_ minimiert</span><span class="sxs-lookup"><span data-stu-id="fe79c-354"><span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>MCI\_DGV\_STATUS\_WINDOW\_MINIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-355">Der **dwreturn** -Member gibt **true** zurück, wenn das Fenster minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-355">The **dwReturn** member returns **TRUE** if the window is minimized.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI- \_ DGV- \_ Status \_ Fenster \_ maximiert</span><span class="sxs-lookup"><span data-stu-id="fe79c-356"><span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>MCI\_DGV\_STATUS\_WINDOW\_MAXIMIZED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-357">Der **dwreturn** -Member gibt **true** zurück, wenn das Fenster maximiert ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-357">The **dwReturn** member returns **TRUE** if the window is maximized.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fe79c-358"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-359">Der **dwreturn** -Member gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-359">The **dwReturn** member returns **TRUE**.</span></span>

</dd> </dl>

<span data-ttu-id="fe79c-360">Für Digital Video-Geräte zeigt der *lpstatus* -Parameter auf eine [**MCI \_ DGV- \_ statusparameterstruktur \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="fe79c-360">For digital-video devices, the *lpStatus* parameter points to an [**MCI\_DGV\_STATUS\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) structure.</span></span>

<span data-ttu-id="fe79c-361">Die folgenden zusätzlichen Flags werden beim **Sequencer** -Gerätetyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-361">The following additional flags are used with the **sequencer** device type.</span></span> <span data-ttu-id="fe79c-362">Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-362">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI- \_ \_ Statustyp "Status \_ "</span><span class="sxs-lookup"><span data-stu-id="fe79c-363"><span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>MCI\_SEQ\_STATUS\_DIVTYPE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-364">Der **dwreturn** -Member wird auf einen der folgenden Werte festgelegt, der den aktuellen Divisions Typ einer Sequenz angibt:</span><span class="sxs-lookup"><span data-stu-id="fe79c-364">The **dwReturn** member is set to one of the following values indicating the current division type of a sequence:</span></span>

-   <span data-ttu-id="fe79c-365">MCI \ \_ \_ div \_ ppqn</span><span class="sxs-lookup"><span data-stu-id="fe79c-365">MCI\_SEQ\_DIV\_PPQN</span></span>
-   <span data-ttu-id="fe79c-366">MCI \ \_ \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="fe79c-366">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>
-   <span data-ttu-id="fe79c-367">MCI Server \_ \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="fe79c-367">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>
-   <span data-ttu-id="fe79c-368">MCI Server \_ \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="fe79c-368">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>
-   <span data-ttu-id="fe79c-369">MCI-Server \ \_ \_ div \_ SMPTE \_ 30drop</span><span class="sxs-lookup"><span data-stu-id="fe79c-369">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI- \_ \_ Status \_ Master</span><span class="sxs-lookup"><span data-stu-id="fe79c-370"><span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>MCI\_SEQ\_STATUS\_MASTER</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-371">Der **dwreturn** -Member ist auf den für den Master Vorgang verwendeten Synchronisierungstyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-371">The **dwReturn** member is set to the synchronization type used for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>Status Offset für MCI- \_ \_ Status \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-372"><span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>MCI\_SEQ\_STATUS\_OFFSET</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-373">Der **dwreturn** -Member wird auf den aktuellen SMPTE-Offset einer Sequenz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-373">The **dwReturn** member is set to the current SMPTE offset of a sequence.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI- \_ \_ \_ Statusport</span><span class="sxs-lookup"><span data-stu-id="fe79c-374"><span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>MCI\_SEQ\_STATUS\_PORT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-375">Der **dwreturn** -Member wird für den aktuellen Port, der von der Sequenz verwendet wird, auf den-ID-Geräte Bezeichner festgelegt</span><span class="sxs-lookup"><span data-stu-id="fe79c-375">The **dwReturn** member is set to the MIDI device identifier for the current port used by the sequence.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI- \_ \_ Status- \_ Slave</span><span class="sxs-lookup"><span data-stu-id="fe79c-376"><span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>MCI\_SEQ\_STATUS\_SLAVE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-377">Der **dwreturn** -Member ist auf den Synchronisierungstyp festgelegt, der für den untergeordneten Vorgang verwendet</span><span class="sxs-lookup"><span data-stu-id="fe79c-377">The **dwReturn** member is set to the synchronization type used for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI- \_ \_ Status \_ Tempo</span><span class="sxs-lookup"><span data-stu-id="fe79c-378"><span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>MCI\_SEQ\_STATUS\_TEMPO</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-379">Der **dwreturn** -Member wird auf das aktuelle Tempo einer MIDI-Sequenz in Beats pro Minute für ppqn-Dateien oder Frames pro Sekunde für SMPTE-Dateien festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-379">The **dwReturn** member is set to the current tempo of a MIDI sequence in beats per minute for PPQN files, or frames per second for SMPTE files.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fe79c-380"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-381">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-381">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="fe79c-382">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-382">The following additional flags are used with the **vcr** device type.</span></span> <span data-ttu-id="fe79c-383">Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-383">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fe79c-384"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-385">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-385">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI- \_ VCR- \_ Status assemblierungsdatensatz \_ \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-386"><span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>MCI\_VCR\_STATUS\_ASSEMBLE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-387">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn der Assemblierungs Modus auf Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-387">The **dwReturn** member is set to **TRUE** if assemble mode is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>Monitor für den MCI \_ -VCR \_ \_ -Status \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-388"><span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-389">Der **dwreturn** -Member wird auf eine Konstante festgelegt, die den derzeit ausgewählten audiomonitortyp angibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-389">The **dwReturn** member is set to a constant, indicating the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI \_ \_ -VCR \_ -Status- \_ audiomonitor- \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="fe79c-390"><span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>MCI\_VCR\_STATUS\_AUDIO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-391">Das **dwreturn** -Element wird auf die Nummer des aktuell ausgewählten audiomonitortyps festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-391">The **dwReturn** member is set to the number of the currently selected audio-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI \_ \_ -VCR \_ -statusaudiodatensatz \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-392"><span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>MCI\_VCR\_STATUS\_AUDIO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-393">Der **dwreturn** -Member ist auf **true** festgelegt, wenn Audiodaten aufgezeichnet werden, wenn der nächste Datensatz-Befehl angegeben wird. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-393">The **dwReturn** member is set to **TRUE** if audio will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="fe79c-394">Wenn Sie MCI \_ Track im *dwFlags* -Parameter dieses Befehls angeben, enthält **dwtrack** den Track, auf den diese Abfrage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-394">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI \_ VCR \_ \_ - \_ statusaudioquelle</span><span class="sxs-lookup"><span data-stu-id="fe79c-395"><span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-396">Der **dwreturn** -Member wird auf eine Konstante festgelegt, die den aktuellen audioquellentyp angibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-396">The **dwReturn** member is set to a constant, indicating the current audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI \_ \_ -VCR \_ -Status- \_ \_ audioquellnummer</span><span class="sxs-lookup"><span data-stu-id="fe79c-397"><span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>MCI\_VCR\_STATUS\_AUDIO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-398">Der **dwreturn** -Member wird auf die Nummer des derzeit ausgewählten audioquelltyps festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-398">The **dwReturn** member is set to the number of the currently selected audio-source type.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI \_ VCR \_ - \_ statusuhr</span><span class="sxs-lookup"><span data-stu-id="fe79c-399"><span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>MCI\_VCR\_STATUS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-400">Der **dwreturn** -Member ist auf den aktuellen Uhrwert festgelegt, und zwar in den Schritten der gesamten Uhr.</span><span class="sxs-lookup"><span data-stu-id="fe79c-400">The **dwReturn** member is set to the current clock value, in total clock increments.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI \_ VCR \_ - \_ statusclock- \_ ID</span><span class="sxs-lookup"><span data-stu-id="fe79c-401"><span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>MCI\_VCR\_STATUS\_CLOCK\_ID</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-402">Der **dwreturn** -Member ist auf eine Zahl festgelegt, die die verwendete Uhr eindeutig beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-402">The **dwReturn** member is set to a number which uniquely describes the clock in use.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI \_ VCR- \_ Status- \_ counter- \_ Format</span><span class="sxs-lookup"><span data-stu-id="fe79c-403"><span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>MCI\_VCR\_STATUS\_COUNTER\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-404">Das **dwreturn** -Element wird auf eine Konstante festgelegt, die das aktuelle Leistungs Muster beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-404">The **dwReturn** member is set to a constant describing the current counter format.</span></span> <span data-ttu-id="fe79c-405">Weitere Informationen finden Sie unter MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="fe79c-405">For more information, see the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>Auflösung des MCI \_ VCR- \_ Status \_ Zählers \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-406"><span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>MCI\_VCR\_STATUS\_COUNTER\_RESOLUTION</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-407">Der **dwreturn** -Member ist auf eine Konstante festgelegt, die die Auflösung des Zählers beschreibt, und ist einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="fe79c-407">The **dwReturn** member is set to a constant describing the resolution of the counter, and is one of the following values:</span></span>

-   <span data-ttu-id="fe79c-408">MCI- \_ VCR- \_ counter- \_ \_ Frames: der Counter hat eine Auflösung von Frames.</span><span class="sxs-lookup"><span data-stu-id="fe79c-408">MCI\_VCR\_COUNTER\_RES\_FRAMES: Counter has resolution of frames.</span></span>
-   <span data-ttu-id="fe79c-409">MCI- \_ VCR- \_ counter- \_ \_ Sekunden: der Counter hat eine Auflösung von Sekunden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-409">MCI\_VCR\_COUNTER\_RES\_SECONDS: Counter has resolution of seconds.</span></span>
-   <span data-ttu-id="fe79c-410">Wert des MCI- \_ VCR- \_ Status \_ Zählers \_ : das **dwreturn** -Element wird im aktuellen Zeit-/Uhrzeitformat auf den aktuellen Lesezeichen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-410">MCI\_VCR\_STATUS\_COUNTER\_VALUE: The **dwReturn** member is set to the current counter reading, in the current counter-time format.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI- \_ VCR- \_ Status- \_ Frame \_ Rate</span><span class="sxs-lookup"><span data-stu-id="fe79c-411"><span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>MCI\_VCR\_STATUS\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-412">Der **dwreturn** -Member wird auf die aktuelle systemeigene Framerate des Geräts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-412">The **dwReturn** member is set to the current native frame rate of the device.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI- \_ VCR- \_ Status \_ Index</span><span class="sxs-lookup"><span data-stu-id="fe79c-413"><span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>MCI\_VCR\_STATUS\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-414">Der **dwreturn** -Member ist auf eine Konstante festgelegt, die den aktuellen Inhalt der Bildschirm Anzeige beschreibt und eine der folgenden Elemente ist:</span><span class="sxs-lookup"><span data-stu-id="fe79c-414">The **dwReturn** member is set to a constant, describing the current contents of the on-screen display, and is one of the following:</span></span>

-   <span data-ttu-id="fe79c-415">MCI- \_ VCR- \_ Index Indikator \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-415">MCI\_VCR\_INDEX\_COUNTER</span></span>
-   <span data-ttu-id="fe79c-416">Datum des MCI- \_ VCR- \_ Indexes \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-416">MCI\_VCR\_INDEX\_DATE</span></span>
-   <span data-ttu-id="fe79c-417">MCI- \_ VCR- \_ Index \_ Zeit</span><span class="sxs-lookup"><span data-stu-id="fe79c-417">MCI\_VCR\_INDEX\_TIME</span></span>
-   <span data-ttu-id="fe79c-418">MCI- \_ VCR- \_ Index \_ Zeit Code</span><span class="sxs-lookup"><span data-stu-id="fe79c-418">MCI\_VCR\_INDEX\_TIMECODE</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI \_ VCR- \_ Status \_ Index \_ on</span><span class="sxs-lookup"><span data-stu-id="fe79c-419"><span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>MCI\_VCR\_STATUS\_INDEX\_ON</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-420">Der **dwreturn** -Member ist auf **true** festgelegt, wenn die Bildschirm Anzeige auf ON festgelegt ist. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-420">The **dwReturn** member is set to **TRUE** if the on-screen display is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI- \_ VCR- \_ \_ statusmedientyp \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-421"><span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>MCI\_VCR\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-422">Der **dwreturn** -Member ist auf einen der folgenden Elemente festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fe79c-422">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="fe79c-423">MCI \_ VCR- \_ Medien \_ 8mm</span><span class="sxs-lookup"><span data-stu-id="fe79c-423">MCI\_VCR\_MEDIA\_8MM</span></span>
-   <span data-ttu-id="fe79c-424">MCI \_ VCR- \_ Medien \_ Hi8</span><span class="sxs-lookup"><span data-stu-id="fe79c-424">MCI\_VCR\_MEDIA\_HI8</span></span>
-   <span data-ttu-id="fe79c-425">MCI \_ VCR \_ Media \_ VHS</span><span class="sxs-lookup"><span data-stu-id="fe79c-425">MCI\_VCR\_MEDIA\_VHS</span></span>
-   <span data-ttu-id="fe79c-426">MCI \_ VCR- \_ Medien \_ SVHS</span><span class="sxs-lookup"><span data-stu-id="fe79c-426">MCI\_VCR\_MEDIA\_SVHS</span></span>
-   <span data-ttu-id="fe79c-427">MCI \_ VCR- \_ Medien \_ Beta</span><span class="sxs-lookup"><span data-stu-id="fe79c-427">MCI\_VCR\_MEDIA\_BETA</span></span>
-   <span data-ttu-id="fe79c-428">MCI \_ VCR- \_ Medien ( \_ edbeta)</span><span class="sxs-lookup"><span data-stu-id="fe79c-428">MCI\_VCR\_MEDIA\_EDBETA</span></span>
-   <span data-ttu-id="fe79c-429">anderes MCI \_ VCR- \_ Medium \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-429">MCI\_VCR\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI- \_ VCR- \_ Status \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="fe79c-430"><span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>MCI\_VCR\_STATUS\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-431">Das **dwnumber** -Element wird auf die logische gatewaynummer festgelegt, wenn Sie dieses Flag mit dem MCI \_ VCR- \_ Status-Tuner- \_ \_ kanalflag verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-431">The **dwNumber** member is set to the logical-tuner number when you use this flag with the MCI\_VCR\_STATUS\_TUNER\_CHANNEL flag.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI \_ \_ -VCR \_ -Status Anzahl \_ von \_ \_ Audiospuren</span><span class="sxs-lookup"><span data-stu-id="fe79c-432"><span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_AUDIO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-433">Das **dwreturn** -Element wird auf die Anzahl der Audiospuren festgelegt, die unabhängig ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="fe79c-433">The **dwReturn** member is set to the number of audio tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI \_ VCR- \_ Status \_ Anzahl \_ von \_ Video \_ Spuren</span><span class="sxs-lookup"><span data-stu-id="fe79c-434"><span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>MCI\_VCR\_STATUS\_NUMBER\_OF\_VIDEO\_TRACKS</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-435">Das **dwreturn** -Element wird auf die Anzahl der Videospuren festgelegt, die unabhängig ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="fe79c-435">The **dwReturn** member is set to the number of video tracks that are independently selectable.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI \_ VCR- \_ Status \_ Pause \_ Timeout</span><span class="sxs-lookup"><span data-stu-id="fe79c-436"><span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>MCI\_VCR\_STATUS\_PAUSE\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-437">Der **dwreturn** -Member wird auf die maximale Dauer eines Pause-Befehls in Millisekunden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-437">The **dwReturn** member is set to the maximum duration, in milliseconds, of a pause command.</span></span> <span data-ttu-id="fe79c-438">Der Rückgabewert 0 (null) gibt an, dass kein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-438">The return value of zero indicates that no time-out will occur.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI \_ VCR- \_ Status \_ Wiedergabe \_ Format</span><span class="sxs-lookup"><span data-stu-id="fe79c-439"><span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>MCI\_VCR\_STATUS\_PLAY\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-440">Der **dwreturn** -Member ist auf einen der folgenden Elemente festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fe79c-440">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="fe79c-441">MCI \_ VCR- \_ Format \_ EP</span><span class="sxs-lookup"><span data-stu-id="fe79c-441">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="fe79c-442">MCI \_ VCR- \_ Format- \_ LP</span><span class="sxs-lookup"><span data-stu-id="fe79c-442">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="fe79c-443">anderes MCI \_ VCR- \_ Format \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-443">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="fe79c-444">MCI \_ VCR- \_ Format \_ SP</span><span class="sxs-lookup"><span data-stu-id="fe79c-444">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>Dauer des MCI \_ VCR- \_ Status \_ Postroll \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-445"><span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>MCI\_VCR\_STATUS\_POSTROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-446">Der **dwreturn** -Member wird auf die Länge des Videobands festgelegt, das nach dem Ende der Position im aktuellen Zeitformat wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-446">The **dwReturn** member is set to the length of the videotape that will play after the spot at which it was stopped, in the current time format.</span></span> <span data-ttu-id="fe79c-447">Dies ist erforderlich, um den VCR-Band Transport von einem Befehl zum Anhalten oder anhalten zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="fe79c-447">This is needed to brake the VCR tape transport from a stop or pause command.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI- \_ VCR- \_ Status \_ Einschalten \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-448"><span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>MCI\_VCR\_STATUS\_POWER\_ON</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-449">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Stromversorgung ist. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-449">The **dwReturn** member is set to **TRUE** if the power is on; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>Dauer der Vorabversion des MCI \_ VCR- \_ Status \_ \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-450"><span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>MCI\_VCR\_STATUS\_PREROLL\_DURATION</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-451">Das **dwreturn** -Element wird auf die Länge des Videobands festgelegt, das vor dem Start Ende im aktuellen Zeitformat wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-451">The **dwReturn** member is set to the length of the videotape that will play before the spot at which it was started, in the current time format.</span></span> <span data-ttu-id="fe79c-452">Dies ist erforderlich, um die VCR-Ausgabe zu stabilisieren.</span><span class="sxs-lookup"><span data-stu-id="fe79c-452">This is needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI \_ VCR- \_ Status \_ Daten Satz \_ Format</span><span class="sxs-lookup"><span data-stu-id="fe79c-453"><span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>MCI\_VCR\_STATUS\_RECORD\_FORMAT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-454">Der **dwreturn** -Member ist auf einen der folgenden Elemente festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fe79c-454">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="fe79c-455">MCI \_ VCR- \_ Format \_ EP</span><span class="sxs-lookup"><span data-stu-id="fe79c-455">MCI\_VCR\_FORMAT\_EP</span></span>
-   <span data-ttu-id="fe79c-456">MCI \_ VCR- \_ Format- \_ LP</span><span class="sxs-lookup"><span data-stu-id="fe79c-456">MCI\_VCR\_FORMAT\_LP</span></span>
-   <span data-ttu-id="fe79c-457">anderes MCI \_ VCR- \_ Format \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-457">MCI\_VCR\_FORMAT\_OTHER</span></span>
-   <span data-ttu-id="fe79c-458">MCI \_ VCR- \_ Format \_ SP</span><span class="sxs-lookup"><span data-stu-id="fe79c-458">MCI\_VCR\_FORMAT\_SP</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI- \_ VCR- \_ Status \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="fe79c-459"><span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>MCI\_VCR\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-460">Der **dwreturn** -Member ist auf die aktuelle Geschwindigkeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-460">The **dwReturn** member is set to the current speed.</span></span> <span data-ttu-id="fe79c-461">Weitere Informationen finden Sie unter MCI \_ VCR \_ Set \_ Speed-Flag des Befehls [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="fe79c-461">For more information, see the MCI\_VCR\_SET\_SPEED flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI- \_ VCR- \_ Status \_ Zeit \_ Modus</span><span class="sxs-lookup"><span data-stu-id="fe79c-462"><span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MCI\_VCR\_STATUS\_TIME\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-463">Der **dwreturn** -Member ist auf einen der folgenden Elemente festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fe79c-463">The **dwReturn** member is set to one of the following:</span></span>

-   <span data-ttu-id="fe79c-464">MCI- \_ VCR- \_ Zeit ( \_ Counter)</span><span class="sxs-lookup"><span data-stu-id="fe79c-464">MCI\_VCR\_TIME\_COUNTER</span></span>
-   <span data-ttu-id="fe79c-465">MCI- \_ VCR- \_ Zeit \_ Erkennung</span><span class="sxs-lookup"><span data-stu-id="fe79c-465">MCI\_VCR\_TIME\_DETECT</span></span>
-   <span data-ttu-id="fe79c-466">MCI- \_ VCR- \_ Zeit ( \_ Timecode)</span><span class="sxs-lookup"><span data-stu-id="fe79c-466">MCI\_VCR\_TIME\_TIMECODE</span></span>

<span data-ttu-id="fe79c-467">Weitere Informationen finden Sie im MCI \_ VCR \_ Set \_ time Mode- \_ Flag des Befehls [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="fe79c-467">For more information, see the MCI\_VCR\_SET\_TIME\_MODE flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI- \_ VCR- \_ Status- \_ \_ Zeittyp</span><span class="sxs-lookup"><span data-stu-id="fe79c-468"><span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>MCI\_VCR\_STATUS\_TIME\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-469">Das **dwreturn** -Element wird auf eine Konstante festgelegt, die den verwendeten aktuellen Zeittyp beschreibt (wird von [Play](play.md), [Record](record.md), [Seek](seek.md)usw. verwendet) und ist einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="fe79c-469">The **dwReturn** member is set to a constant describing the current time type in use (used by [play](play.md), [record](record.md), [seek](seek.md), and so on), and is one of the following:</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI- \_ VCR- \_ Zeit ( \_ Counter)</span><span class="sxs-lookup"><span data-stu-id="fe79c-470"><span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>MCI\_VCR\_TIME\_COUNTER</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-471">Der Counter-Wert wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-471">Counter is in use.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI- \_ VCR- \_ Zeit ( \_ Timecode)</span><span class="sxs-lookup"><span data-stu-id="fe79c-472"><span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>MCI\_VCR\_TIME\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-473">"Timecode" wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-473">Timecode is in use.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI- \_ VCR- \_ Status- \_ Zeit Code \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fe79c-474"><span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>MCI\_VCR\_STATUS\_TIMECODE\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-475">Der **dwreturn** -Member ist auf **true** festgelegt, wenn der Zeitcode an der aktuellen Position im Inhalt vorhanden ist. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-475">The **dwReturn** member is set to **TRUE** if timecode is present at the current position in the content; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI- \_ VCR- \_ Status- \_ Timecode- \_ Datensatz</span><span class="sxs-lookup"><span data-stu-id="fe79c-476"><span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>MCI\_VCR\_STATUS\_TIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-477">Der **dwreturn** -Member ist auf **true** festgelegt, wenn der Zeitcode aufgezeichnet wird, wenn der nächste Datensatz-Befehl angegeben wird. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-477">The **dwReturn** member is set to **TRUE** if the timecode will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI- \_ VCR- \_ Status- \_ \_ timecodetyp</span><span class="sxs-lookup"><span data-stu-id="fe79c-478"><span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>MCI\_VCR\_STATUS\_TIMECODE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-479">Der **dwreturn** -Member ist auf eine Konstante festgelegt, die den Typ des Timecodes beschreibt, der direkt vom Gerät unterstützt wird. es handelt sich um einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="fe79c-479">The **dwReturn** member is set to a constant, describing the type of timecode that is directly supported by the device, and is one of the following:</span></span>

-   <span data-ttu-id="fe79c-480">MCI \_ VCR \_ Timecode \_ Type \_ None: dieses Gerät verwendet keinen Timecode.</span><span class="sxs-lookup"><span data-stu-id="fe79c-480">MCI\_VCR\_TIMECODE\_TYPE\_NONE: This device does not use a timecode.</span></span>
-   <span data-ttu-id="fe79c-481">MCI- \_ VCR- \_ Timecode \_ Type \_ other: dieses Gerät verwendet einen nicht angegebenen Zeit Code.</span><span class="sxs-lookup"><span data-stu-id="fe79c-481">MCI\_VCR\_TIMECODE\_TYPE\_OTHER: This device uses an unspecified timecode.</span></span>
-   <span data-ttu-id="fe79c-482">MCI \_ VCR \_ Timecode \_ Type \_ SMPTE: dieses Gerät verwendet SMPTE-Timecode.</span><span class="sxs-lookup"><span data-stu-id="fe79c-482">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE: This device uses SMPTE timecode.</span></span>
-   <span data-ttu-id="fe79c-483">MCI \_ VCR \_ Timecode \_ Type \_ SMPTE \_ Drop: dieses Gerät verwendet SMPTE Drop Timecode.</span><span class="sxs-lookup"><span data-stu-id="fe79c-483">MCI\_VCR\_TIMECODE\_TYPE\_SMPTE\_DROP: This device uses SMPTE drop timecode.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI \_ VCR- \_ Status- \_ \_ Peerkanal</span><span class="sxs-lookup"><span data-stu-id="fe79c-484"><span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>MCI\_VCR\_STATUS\_TUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-485">Der **dwreturn** -Member wird auf die aktuelle Channelnummer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-485">The **dwReturn** member is set to the current channel number.</span></span> <span data-ttu-id="fe79c-486">Wenn Sie die MCI- \_ VCR- \_ Status \_ Nummer im *dwFlags* -Parameter dieses Befehls angeben, enthält **dwnumber** die logische-Tuner-Nummer, für die dieser Befehl gilt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-486">If you specify MCI\_VCR\_STATUS\_NUMBER in the *dwFlags* parameter of this command, **dwNumber** contains the logical-tuner number this command applies to.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>Video Monitor für den MCI- \_ VCR- \_ Status \_ \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-487"><span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-488">Der **dwreturn** -Member wird auf eine Konstante festgelegt, die den derzeit ausgewählten Videomonitor-Typ angibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-488">The **dwReturn** member is set to a constant, indicating the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_ \_ \_ Video \_ Monitor \_ Nummer für den MCI-VCR-Status</span><span class="sxs-lookup"><span data-stu-id="fe79c-489"><span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>MCI\_VCR\_STATUS\_VIDEO\_MONITOR\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-490">Das **dwreturn** -Element wird auf die Nummer des derzeit ausgewählten Videomonitor Typs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-490">The **dwReturn** member is set to the number of the currently selected video-monitor type.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_ \_ \_ Video \_ Daten Satz für den MCI VCR-Status</span><span class="sxs-lookup"><span data-stu-id="fe79c-491"><span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>MCI\_VCR\_STATUS\_VIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-492">Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Video aufgezeichnet wird, wenn der nächste Datensatz-Befehl angegeben wird. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-492">The **dwReturn** member is set to **TRUE** if video will be recorded when the next record command is given; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="fe79c-493">Wenn Sie MCI \_ Track im *dwFlags* -Parameter dieses Befehls angeben, enthält **dwtrack** den Track, auf den diese Abfrage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-493">If you specify MCI\_TRACK in the *dwFlags* parameter of this command, **dwTrack** contains the track this inquiry applies to.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI \_ VCR- \_ Status- \_ Video \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="fe79c-494"><span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-495">Der **dwreturn** -Member wird auf eine Konstante festgelegt, die den derzeit ausgewählten Typ der Videoquelle angibt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-495">The **dwReturn** member is set to a constant indicating the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI \_ VCR- \_ Status \_ Video- \_ Quell \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="fe79c-496"><span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>MCI\_VCR\_STATUS\_VIDEO\_SOURCE\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-497">Das **dwreturn** -Element wird auf die Nummer des derzeit ausgewählten Videoquellen Typs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-497">The **dwReturn** member is set to the number of the currently selected video-source type.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI \_ VCR \_ Status \_ Schreib \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="fe79c-498"><span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>MCI\_VCR\_STATUS\_WRITE\_PROTECTED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-499">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Medium schreibgeschützt ist. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-499">The **dwReturn** member is set to **TRUE** if the media is write-protected; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="fe79c-500">Bei VCR-Geräten verweist der *lpstatus* -Parameter auf eine [**MCI- \_ VCR- \_ statusparameterstruktur \_**](mci-vcr-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="fe79c-500">For VCR devices, the *lpStatus* parameter points to an [**MCI\_VCR\_STATUS\_PARMS**](mci-vcr-status-parms.md) structure.</span></span>

<span data-ttu-id="fe79c-501">Wenn Sie das MCI- \_ \_ statuslength-Flag zum Ermitteln der Länge des Mediums verwenden, werden für VCR-Geräte immer zwei Stunden zurückgegeben, es sei denn, die Länge wurde explizit mit dem Befehl [MCI \_ Set](mci-set.md) geändert.</span><span class="sxs-lookup"><span data-stu-id="fe79c-501">Using the MCI\_STATUS\_LENGTH flag to determine the length of the media always returns 2 hours for VCR devices, unless the length has been explicitly changed using the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="fe79c-502">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp " **Overlay** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-502">The following additional flags are used with the **overlay** device type.</span></span> <span data-ttu-id="fe79c-503">Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-503">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI \_ OVLY- \_ Status- \_ HWND</span><span class="sxs-lookup"><span data-stu-id="fe79c-504"><span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>MCI\_OVLY\_STATUS\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-505">Das **dwreturn** -Element wird auf das Handle des Fensters festgelegt, das dem Video Überlagerungs Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fe79c-505">The **dwReturn** member is set to the handle of the window associated with the video-overlay device.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI- \_ OVLY- \_ Status \_ Streckung</span><span class="sxs-lookup"><span data-stu-id="fe79c-506"><span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>MCI\_OVLY\_STATUS\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-507">Der **dwreturn** -Member ist auf **true** festgelegt, wenn die Streckung aktiviert ist. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-507">The **dwReturn** member is set to **TRUE** if stretching is enabled; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fe79c-508"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-509">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-509">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> </dl>

<span data-ttu-id="fe79c-510">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp " **Videodisk** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-510">The following additional flags are used with the **videodisc** device type.</span></span> <span data-ttu-id="fe79c-511">Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-511">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI- \_ Status \_ Medien \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fe79c-512"><span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>MCI\_STATUS\_MEDIA\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-513">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn die Medien in das Gerät eingefügt werden. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-513">The **dwReturn** member is set to **TRUE** if the media is inserted in the device; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI- \_ Status \_ Modus</span><span class="sxs-lookup"><span data-stu-id="fe79c-514"><span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>MCI\_STATUS\_MODE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-515">Der **dwreturn** -Member ist auf den aktuellen Modus des Geräts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-515">The **dwReturn** member is set to the current mode of the device.</span></span> <span data-ttu-id="fe79c-516">Videodisk-Geräte können \_ \_ \_ zusätzlich zu den Konstanten, die von jedem Gerät zurückgegeben werden können, die MCI-VD-Modus-Konstante zurückgeben, wie mit dem *dwFlags* -Parameter dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="fe79c-516">Videodisc devices can return the MCI\_VD\_MODE\_PARK constant, in addition to the constants any device can return, as documented with the *dwFlags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI- \_ VD- \_ Status- \_ Festplatten \_ Größe</span><span class="sxs-lookup"><span data-stu-id="fe79c-517"><span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>MCI\_VD\_STATUS\_DISC\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-518">Der **dwreturn** -Member wird auf die Größe der geladenen CD in Zoll (8 oder 12) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-518">The **dwReturn** member is set to the size of the loaded disc in inches (8 or 12).</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI- \_ VD- \_ Status \_ Vorwärts</span><span class="sxs-lookup"><span data-stu-id="fe79c-519"><span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>MCI\_VD\_STATUS\_FORWARD</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-520">Der **dwreturn** -Member wird bei der Wiedergabe auf **true** festgelegt. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-520">The **dwReturn** member is set to **TRUE** if playing forward; it is set to **FALSE** otherwise.</span></span>

<span data-ttu-id="fe79c-521">Dieses Flag wird vom MCI-Videodisk-Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-521">The MCI videodisc device does not support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI- \_ VD- \_ \_ statusmedientyp \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-522"><span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>MCI\_VD\_STATUS\_MEDIA\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-523">Der **dwreturn** -Member ist auf den Medientyp des eingefügten Mediums festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-523">The **dwReturn** member is set to the media type of the inserted media.</span></span> <span data-ttu-id="fe79c-524">Die folgenden Medientypen können zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="fe79c-524">The following media types can be returned:</span></span>

<span data-ttu-id="fe79c-525">MCI- \_ VD- \_ Medien- \_ CAV</span><span class="sxs-lookup"><span data-stu-id="fe79c-525">MCI\_VD\_MEDIA\_CAV</span></span>

<span data-ttu-id="fe79c-526">MCI- \_ VD- \_ Medien- \_ CLV</span><span class="sxs-lookup"><span data-stu-id="fe79c-526">MCI\_VD\_MEDIA\_CLV</span></span>

<span data-ttu-id="fe79c-527">anderes MCI- \_ VD- \_ Medium \_</span><span class="sxs-lookup"><span data-stu-id="fe79c-527">MCI\_VD\_MEDIA\_OTHER</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI- \_ VD- \_ Status \_ Seite</span><span class="sxs-lookup"><span data-stu-id="fe79c-528"><span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>MCI\_VD\_STATUS\_SIDE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-529">Der **dwreturn** -Member ist auf 1 oder 2 festgelegt, um anzugeben, welche Seite der Festplatte geladen wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-529">The **dwReturn** member is set to 1 or 2 to indicate which side of the disc is loaded.</span></span> <span data-ttu-id="fe79c-530">Dieses Flag wird nicht von allen Videodisk-Geräten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-530">Not all videodisc devices support this flag.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI- \_ VD- \_ Status \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="fe79c-531"><span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>MCI\_VD\_STATUS\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-532">Der **dwreturn** -Member wird auf die Wiedergabegeschwindigkeit in Frames pro Sekunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-532">The **dwReturn** member is set to the play speed in frames per second.</span></span> <span data-ttu-id="fe79c-533">Die mcipionr. DRV-Gerätetreiber gibt eine nicht unterstützte mcierr- \_ \_ Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="fe79c-533">The MCIPIONR.DRV device driver returns MCIERR\_UNSUPPORTED\_FUNCTION.</span></span>

</dd> </dl>

<span data-ttu-id="fe79c-534">Die folgenden zusätzlichen Flags werden mit dem **waveaudiogerätetyp** verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe79c-534">The following additional flags are used with the **waveaudio** device type.</span></span> <span data-ttu-id="fe79c-535">Diese Konstanten werden im **lengertem** -Member der Struktur verwendet, auf die durch den *lpstatus* -Parameter verwiesen wird, wenn das MCI- \_ Status \_ Element für den *dwFlags* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-535">These constants are used in the **dwItem** member of the structure pointed to by the *lpStatus* parameter when MCI\_STATUS\_ITEM is specified for the *dwFlags* parameter.</span></span>

<dl> <dt>

<span data-ttu-id="fe79c-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI \_ Wave \_ Formattag</span><span class="sxs-lookup"><span data-stu-id="fe79c-536"><span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>MCI\_WAVE\_FORMATTAG</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-537">Das **dwreturn** -Element wird auf das aktuelle Formattag festgelegt, das für die Wiedergabe, Aufzeichnung und Speicherung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-537">The **dwReturn** member is set to the current format tag used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI- \_ Wave- \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="fe79c-538"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-539">Der **dwreturn** -Member ist auf das für die Aufzeichnung verwendete Wave-Eingabegerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-539">The **dwReturn** member is set to the wave input device used for recording.</span></span> <span data-ttu-id="fe79c-540">Wenn kein Gerät verwendet wird und kein Gerät explizit festgelegt wurde, lautet die Fehlerrückgabe mcierr \_ Wave \_ inputunspezifi.</span><span class="sxs-lookup"><span data-stu-id="fe79c-540">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_INPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI- \_ Wave- \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fe79c-541"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-542">Der **dwreturn** -Member ist auf das für die Wiedergabe verwendete Wave-Ausgabegerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-542">The **dwReturn** member is set to the wave output device used for playing.</span></span> <span data-ttu-id="fe79c-543">Wenn kein Gerät verwendet wird und kein Gerät explizit festgelegt wurde, lautet die Fehlerrückgabe mcierr \_ Wave \_ outputunspezifi.</span><span class="sxs-lookup"><span data-stu-id="fe79c-543">If no device is in use and no device has been explicitly set, then the error return is MCIERR\_WAVE\_OUTPUTUNSPECIFIED.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI- \_ Wave- \_ Status \_ avgbytespersec</span><span class="sxs-lookup"><span data-stu-id="fe79c-544"><span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>MCI\_WAVE\_STATUS\_AVGBYTESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-545">Das **dwreturn** -Element wird auf die aktuellen Bytes pro Sekunde festgelegt, die zum Abspielen, aufzeichnen und Speichern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-545">The **dwReturn** member is set to the current bytes per second used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI- \_ Wave- \_ Status- \_ BitsPerSample</span><span class="sxs-lookup"><span data-stu-id="fe79c-546"><span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>MCI\_WAVE\_STATUS\_BITSPERSAMPLE</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-547">Das **dwreturn** -Element wird auf die aktuellen Bits pro Beispiel festgelegt, die zum Abspielen, aufzeichnen und Speichern von PCM-formatierten Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-547">The **dwReturn** member is set to the current bits per sample used for playing, recording, and saving PCM formatted data.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI- \_ Wellen \_ Status \_ BlockAlign</span><span class="sxs-lookup"><span data-stu-id="fe79c-548"><span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>MCI\_WAVE\_STATUS\_BLOCKALIGN</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-549">Das **dwreturn** -Element wird auf die aktuelle Block Ausrichtung festgelegt, die zum Abspielen, aufzeichnen und Speichern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-549">The **dwReturn** member is set to the current block alignment used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI- \_ Wellen \_ Status \_ Kanäle</span><span class="sxs-lookup"><span data-stu-id="fe79c-550"><span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>MCI\_WAVE\_STATUS\_CHANNELS</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-551">Der **dwreturn** -Member wird auf die aktuelle Kanalanzahl festgelegt, die zum wiedergeben, aufzeichnen und Speichern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fe79c-551">The **dwReturn** member is set to the current channel count used for playing, recording, and saving.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI- \_ Wave- \_ Status \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="fe79c-552"><span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>MCI\_WAVE\_STATUS\_LEVEL</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-553">Der **dwreturn** -Member ist auf den aktuellen Datensatz oder die Wiedergabe Ebene von PCM-formatierten Daten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fe79c-553">The **dwReturn** member is set to the current record or playback level of PCM formatted data.</span></span> <span data-ttu-id="fe79c-554">Der Wert wird abhängig von der verwendeten Stichprobengröße als 8-oder 16-Bit-Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe79c-554">The value is returned as an 8- or 16-bit value, depending on the sample size used.</span></span> <span data-ttu-id="fe79c-555">Die Rechte-oder Mono-Kanal Ebene wird im nieder wertigen Wort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe79c-555">The right or mono channel level is returned in the low-order word.</span></span> <span data-ttu-id="fe79c-556">Die linke Kanal Ebene wird im höherwertigen Wort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe79c-556">The left channel level is returned in the high-order word.</span></span>

</dd> <dt>

<span data-ttu-id="fe79c-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI- \_ Wave- \_ Status " \_ samplespersec"</span><span class="sxs-lookup"><span data-stu-id="fe79c-557"><span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>MCI\_WAVE\_STATUS\_SAMPLESPERSEC</span></span>
</dt> <dd>

<span data-ttu-id="fe79c-558">Das **dwreturn** -Element wird auf die aktuellen Stichproben pro Sekunde festgelegt, die zum Abspielen, aufzeichnen und Speichern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe79c-558">The **dwReturn** member is set to the current samples per second used for playing, recording, and saving.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe79c-559">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe79c-559">Requirements</span></span>



| <span data-ttu-id="fe79c-560">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe79c-560">Requirement</span></span> | <span data-ttu-id="fe79c-561">Wert</span><span class="sxs-lookup"><span data-stu-id="fe79c-561">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe79c-562">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe79c-562">Minimum supported client</span></span><br/> | <span data-ttu-id="fe79c-563">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe79c-563">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe79c-564">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe79c-564">Minimum supported server</span></span><br/> | <span data-ttu-id="fe79c-565">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe79c-565">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe79c-566">Header</span><span class="sxs-lookup"><span data-stu-id="fe79c-566">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe79c-567"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe79c-567"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe79c-568">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe79c-568">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe79c-569">MCI</span><span class="sxs-lookup"><span data-stu-id="fe79c-569">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fe79c-570">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="fe79c-570">MCI Commands</span></span>](mci-commands.md)
</dt> <dt>

[<span data-ttu-id="fe79c-571">MCI- \_ Ausschneiden</span><span class="sxs-lookup"><span data-stu-id="fe79c-571">MCI\_CUT</span></span>](mci-cut.md)
</dt> <dt>

[<span data-ttu-id="fe79c-572">MCI \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="fe79c-572">MCI\_DELETE</span></span>](mci-delete.md)
</dt> <dt>

[<span data-ttu-id="fe79c-573">MCI- \_ Einfügen</span><span class="sxs-lookup"><span data-stu-id="fe79c-573">MCI\_PASTE</span></span>](mci-paste.md)
</dt> <dt>

[<span data-ttu-id="fe79c-574">MCI- \_ Reserve</span><span class="sxs-lookup"><span data-stu-id="fe79c-574">MCI\_RESERVE</span></span>](mci-reserve.md)
</dt> <dt>

[<span data-ttu-id="fe79c-575">MCI- \_ Gruppe</span><span class="sxs-lookup"><span data-stu-id="fe79c-575">MCI\_SET</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="fe79c-576">Theater</span><span class="sxs-lookup"><span data-stu-id="fe79c-576">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="fe79c-577">record</span><span class="sxs-lookup"><span data-stu-id="fe79c-577">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="fe79c-578">einzuholen</span><span class="sxs-lookup"><span data-stu-id="fe79c-578">seek</span></span>](seek.md)
</dt> </dl>

 

