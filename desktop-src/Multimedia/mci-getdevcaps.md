---
title: MCI_GETDEVCAPS Befehl (MMSYSTEM. h)
description: Der MCI \_ getdevcaps-Befehl ruft statische Informationen zu einem Gerät ab.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519043"
---
# <a name="mci_getdevcaps-command"></a><span data-ttu-id="6b381-104">MCI \_ getdevcaps-Befehl</span><span class="sxs-lookup"><span data-stu-id="6b381-104">MCI\_GETDEVCAPS command</span></span>

<span data-ttu-id="6b381-105">Der MCI \_ getdevcaps-Befehl ruft statische Informationen zu einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="6b381-105">The MCI\_GETDEVCAPS command retrieves static information about a device.</span></span> <span data-ttu-id="6b381-106">Alle Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="6b381-106">All devices recognize this command.</span></span> <span data-ttu-id="6b381-107">Welche Parameter und Flags für diesen Befehl verfügbar sind, hängt vom ausgewählten Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="6b381-107">The parameters and flags available for this command depend on the selected device.</span></span> <span data-ttu-id="6b381-108">Informationen werden im **dwreturn** -Member der von *lpcapsparms* identifizierten Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b381-108">Information is returned in the **dwReturn** member of the structure identified by *lpCapsParms*.</span></span>

<span data-ttu-id="6b381-109">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="6b381-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a><span data-ttu-id="6b381-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b381-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b381-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="6b381-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6b381-112">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="6b381-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6b381-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6b381-114">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="6b381-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="6b381-115">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6b381-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b381-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpcapsparms*</span><span class="sxs-lookup"><span data-stu-id="6b381-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span></span>
</dt> <dd>

<span data-ttu-id="6b381-117">Zeiger auf eine [**MCI \_ getdevcaps \_**](mci-getdevcaps-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="6b381-117">Pointer to an [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b381-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b381-118">Return Value</span></span>

<span data-ttu-id="6b381-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="6b381-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b381-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b381-120">Remarks</span></span>

<span data-ttu-id="6b381-121">Die folgenden zusätzlichen Standard-und Befehls spezifischen Flags gelten für alle Geräte, die MCI \_ getdevcaps unterstützen:</span><span class="sxs-lookup"><span data-stu-id="6b381-121">The following additional standard and command-specific flags apply to all devices supporting MCI\_GETDEVCAPS:</span></span>

<dl> <dt>

<span data-ttu-id="6b381-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI \_ getdevcaps- \_ Verbund \_ Gerät</span><span class="sxs-lookup"><span data-stu-id="6b381-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI\_GETDEVCAPS\_COMPOUND\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-123">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Datenspeicher verwendet, das explizit geöffnet und geschlossen werden muss. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-123">The **dwReturn** member is set to **TRUE** if the device uses data storage that must be explicitly opened and closed; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI \_ getdevcaps \_ - \_ Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="6b381-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI\_GETDEVCAPS\_DEVICE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-125">Der **dwreturn** -Member wird auf einen der Werte festgelegt, die unter [MCI-Gerätetypen](mci-device-types.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6b381-125">The **dwReturn** member is set to one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b381-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ getdevcaps \_ hat \_ Audiodaten</span><span class="sxs-lookup"><span data-stu-id="6b381-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI\_GETDEVCAPS\_HAS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="6b381-127">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät über eine Audioausgabe verfügt. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-127">The **dwReturn** member is set to **TRUE** if the device has audio output; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ getdevcaps \_ hat \_ Video</span><span class="sxs-lookup"><span data-stu-id="6b381-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI\_GETDEVCAPS\_HAS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="6b381-129">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät über eine Videoausgabe verfügt. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-129">The **dwReturn** member is set to **TRUE** if the device has video output; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="6b381-130">Beispielsweise ist der-Member für Geräte, die den Videodisk-Befehlssatz unterstützen, auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-130">For example, the member is set to **TRUE** for devices that support the videodisc command set.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI \_ getdevcaps- \_ Element</span><span class="sxs-lookup"><span data-stu-id="6b381-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI\_GETDEVCAPS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="6b381-132">Gibt an, dass das **dwitem** -Element der MCI-Struktur " [**\_ getdevcaps \_**](mci-getdevcaps-parms.md) " eine der folgenden Konstanten enthält:</span><span class="sxs-lookup"><span data-stu-id="6b381-132">Specifies that the **dwItem** member of the [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure contains one of the following constants:</span></span>

</dd> <dt>

<span data-ttu-id="6b381-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ getdevcaps \_ kann \_ auswerfen</span><span class="sxs-lookup"><span data-stu-id="6b381-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI\_GETDEVCAPS\_CAN\_EJECT</span></span>
</dt> <dd>

<span data-ttu-id="6b381-134">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät die Medien auswerfen kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-134">The **dwReturn** member is set to **TRUE** if the device can eject the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ getdevcaps kann wiedergegeben werden \_ \_</span><span class="sxs-lookup"><span data-stu-id="6b381-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI\_GETDEVCAPS\_CAN\_PLAY</span></span>
</dt> <dd>

<span data-ttu-id="6b381-136">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät die Medien wiedergeben kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-136">The **dwReturn** member is set to **TRUE** if the device can play the media; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="6b381-137">Wenn ein Gerät den Wert **true** angibt, bedeutet dies, dass das Gerät die Befehle [MCI \_ Pause](mci-pause.md) und [ \_ MCI](mci-stop.md) -Befehl sowie den Befehl [MCI \_ Play](mci-play.md) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b381-137">If a device specifies **TRUE**, it implies the device supports the [MCI\_PAUSE](mci-pause.md) and [MCI\_STOP](mci-stop.md) commands as well as the [MCI\_PLAY](mci-play.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ getdevcaps \_ kann \_ aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="6b381-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI\_GETDEVCAPS\_CAN\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="6b381-139">Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät eine Aufzeichnung unterstützt. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-139">The **dwReturn** member is set to **TRUE** if the device supports recording; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="6b381-140">Wenn ein Gerät **true** angibt, bedeutet dies, dass das Gerät die Befehle MCI \_ Anhalten und MCI- \_ Befehl sowie den Befehl [MCI- \_ Datensatz](mci-record.md) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b381-140">If a device specifies **TRUE**, it implies the device supports the MCI\_PAUSE and MCI\_STOP commands as well as the [MCI\_RECORD](mci-record.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ getdevcaps \_ kann \_ Speichern</span><span class="sxs-lookup"><span data-stu-id="6b381-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI\_GETDEVCAPS\_CAN\_SAVE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-142">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät eine Datei speichern kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-142">The **dwReturn** member is set to **TRUE** if the device can save a file; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ getdevcaps \_ verwendet \_ Dateien</span><span class="sxs-lookup"><span data-stu-id="6b381-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI\_GETDEVCAPS\_USES\_FILES</span></span>
</dt> <dd>

<span data-ttu-id="6b381-144">Der **dwreturn** -Member ist auf **true** festgelegt, wenn für das Gerät ein Dateiname erforderlich ist. Andernfalls wird **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-144">The **dwReturn** member is set to **TRUE** if the device requires a filename; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="6b381-145">Dateien werden nur von Verbund Geräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b381-145">Only compound devices use files.</span></span>

</dd> </dl>

<span data-ttu-id="6b381-146">Die folgenden Flags können im **dwitem** -Member von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) für den **Digitalvideo** -Gerätetyp angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6b381-146">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="6b381-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ eingefroren werden</span><span class="sxs-lookup"><span data-stu-id="6b381-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-148">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Frames Einfrieren kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-148">The **dwReturn** member is set to **TRUE** if the device can freeze frames; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ Sperren</span><span class="sxs-lookup"><span data-stu-id="6b381-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK</span></span>
</dt> <dd>

<span data-ttu-id="6b381-150">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät gesperrt werden kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-150">The **dwReturn** member is set to **TRUE** if the device can lock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="6b381-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-152">Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät in umgekehrter Reihenfolge wiedergegeben werden kann Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-152">The **dwReturn** member is set to **TRUE** if the device can play in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ Str \_ werden</span><span class="sxs-lookup"><span data-stu-id="6b381-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STR\_IN</span></span>
</dt> <dd>

<span data-ttu-id="6b381-154">Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät Eingaben ausdehnen kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-154">The **dwReturn** member is set to **TRUE** if the device can stretch input; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ gestreckt werden</span><span class="sxs-lookup"><span data-stu-id="6b381-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="6b381-156">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät ein Bildstrecken kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-156">The **dwReturn** member is set to **TRUE** if the device can stretch an image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ getdevcaps \_ kann \_ Testen</span><span class="sxs-lookup"><span data-stu-id="6b381-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="6b381-158">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Tests ausführen kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-158">The **dwReturn** member is set to **TRUE** if the device can perform tests; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ getdevcaps \_ hat \_ weiterhin</span><span class="sxs-lookup"><span data-stu-id="6b381-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI\_DGV\_GETDEVCAPS\_HAS\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="6b381-160">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät weiterhin Bilder anzeigen kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-160">The **dwReturn** member is set to **TRUE** if the device can display still images; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ getdevcaps ( \_ Max. \_ Fenster)</span><span class="sxs-lookup"><span data-stu-id="6b381-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI\_DGV\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="6b381-162">Der **dwreturn** -Member ist auf die maximale Anzahl von Fenstern festgelegt, die das Gerät gleichzeitig verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="6b381-162">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI \_ DGV \_ getdevcaps- \_ höchst \_ Rate</span><span class="sxs-lookup"><span data-stu-id="6b381-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MAXIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-164">Der **dwreturn** -Member wird auf die maximale Wiedergabe Rate für das Gerät in Frames pro Sekunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-164">The **dwReturn** member is set to the maximum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>minimale Rate der MCI \_ DGV- \_ getdevcaps \_ \_</span><span class="sxs-lookup"><span data-stu-id="6b381-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MINIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-166">Der **dwreturn** -Member wird auf die minimale Wiedergabe Rate für das Gerät in Frames pro Sekunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-166">The **dwReturn** member is set to the minimum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI \_ DGV \_ getdevcaps- \_ Paletten</span><span class="sxs-lookup"><span data-stu-id="6b381-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI\_DGV\_GETDEVCAPS\_PALETTES</span></span>
</dt> <dd>

<span data-ttu-id="6b381-168">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät einen Palettenhandle zurückgeben kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-168">The **dwReturn** member is set to **TRUE** if the device can return a palette handle; otherwise, it is set to **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="6b381-169">Die folgenden Flags können für den **VCR** -Gerätetyp im Element " **dwitem** " von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6b381-169">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="6b381-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI \_ getdevcaps- \_ Takt \_ Inkrement- \_ Rate</span><span class="sxs-lookup"><span data-stu-id="6b381-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI\_GETDEVCAPS\_CLOCK\_INCREMENT\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-171">Der **dwreturn** -Member wird auf die Anzahl der Inkremente pro Sekunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-171">The **dwReturn** member is set to the number of increments per second.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ die \_ Länge erkennen</span><span class="sxs-lookup"><span data-stu-id="6b381-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_DETECT\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="6b381-173">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät die Länge des Mediums erkennen kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-173">The **dwReturn** member is set to **TRUE** if the device is capable of detecting the length of the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ eingefroren werden.</span><span class="sxs-lookup"><span data-stu-id="6b381-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-175">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät das Ausgabe Bild Einfrieren kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-175">The **dwReturn** member is set to **TRUE** if the device is capable of freezing the output image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ Quellen überwachen \_</span><span class="sxs-lookup"><span data-stu-id="6b381-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_MONITOR\_SOURCES</span></span>
</dt> <dd>

<span data-ttu-id="6b381-177">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Quellen überwachen kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-177">The **dwReturn** member is set to **TRUE** if the device is capable of monitoring sources; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ vorab</span><span class="sxs-lookup"><span data-stu-id="6b381-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="6b381-179">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät über ein vorab Element verfügen kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-179">The **dwReturn** member is set to **TRUE** if the device is capable of preroll; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ getdevcaps \_ kann eine \_ Vorschau anzeigen</span><span class="sxs-lookup"><span data-stu-id="6b381-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREVIEW</span></span>
</dt> <dd>

<span data-ttu-id="6b381-181">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät Vorschau Versionen unterstützt. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-181">The **dwReturn** member is set to **TRUE** if the device is capable of previews; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="6b381-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-183">Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät in umgekehrter Reihenfolge wiedergegeben werden kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-183">The **dwReturn** member is set to **TRUE** if the device is capable of playing in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI \_ VCR \_ getdevcaps \_ kann \_ Testen</span><span class="sxs-lookup"><span data-stu-id="6b381-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="6b381-185">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät getestet werden kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-185">The **dwReturn** member is set to **TRUE** if the device is capable of testing; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ getdevcaps \_ hat \_ Clock</span><span class="sxs-lookup"><span data-stu-id="6b381-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="6b381-187">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät eine externe Uhr unterstützt. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-187">The **dwReturn** member is set to **TRUE** if the device supports an external clock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI \_ VCR \_ getdevcaps \_ hat \_ Timecode</span><span class="sxs-lookup"><span data-stu-id="6b381-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-189">Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät über eine Zeitcode-Funktion verfügt oder wenn diese Funktion unbekannt ist. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-189">The **dwReturn** member is set to **TRUE** if device has timecode capability or if this capability is unknown; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI \_ VCR \_ getdevcaps- \_ Anzahl \_ von \_ Markierungen</span><span class="sxs-lookup"><span data-stu-id="6b381-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI\_VCR\_GETDEVCAPS\_NUMBER\_OF\_MARKS</span></span>
</dt> <dd>

<span data-ttu-id="6b381-191">Der **dwreturn** -Member wird auf die Anzahl der Markierungen (99) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-191">The **dwReturn** member is set to the number of marks (99).</span></span>

</dd> <dt>

<span data-ttu-id="6b381-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI \_ VCR \_ getdevcaps- \_ Such \_ Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="6b381-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI\_VCR\_GETDEVCAPS\_SEEK\_ACCURACY</span></span>
</dt> <dd>

<span data-ttu-id="6b381-193">Der **dwreturn** -Member ist auf die Such Genauigkeit des Geräts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-193">The **dwReturn** member is set to the seek accuracy of the device.</span></span>

</dd> </dl>

<span data-ttu-id="6b381-194">Die folgenden Flags können im **dwitem** -Member von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) für den **Überlagerungs** Gerätetyp angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6b381-194">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="6b381-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ getdevcaps \_ kann \_ eingefroren werden.</span><span class="sxs-lookup"><span data-stu-id="6b381-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-196">Der **dwreturn** -Member ist auf " **true** " festgelegt, wenn das Gerät das Image Einfrieren kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-196">The **dwReturn** member is set to **TRUE** if the device can freeze the image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI \_ OVLY \_ getdevcaps \_ kann \_ gestreckt werden</span><span class="sxs-lookup"><span data-stu-id="6b381-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="6b381-198">Der **dwreturn** -Member ist auf **true** festgelegt, wenn das Gerät das Bild zum Ausfüllen des Frames Strecken kann. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-198">The **dwReturn** member is set to **TRUE** if the device can stretch the image to fill the frame; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ getdevcaps ( \_ Max. \_ Fenster)</span><span class="sxs-lookup"><span data-stu-id="6b381-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI\_OVLY\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="6b381-200">Der **dwreturn** -Member ist auf die maximale Anzahl von Fenstern festgelegt, die das Gerät gleichzeitig verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="6b381-200">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> </dl>

<span data-ttu-id="6b381-201">Die folgenden Flags können im **dwitem** -Member von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) für den **Videodisk** -Gerätetyp angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6b381-201">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="6b381-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI- \_ VD- \_ getdevcaps \_ können \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="6b381-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI\_VD\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-203">Der **dwreturn** -Member ist auf **true** festgelegt, wenn der Videodisk-Player in umgekehrter Richtung wiedergegeben werden kann Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-203">The **dwReturn** member is set to **TRUE** if the videodisc player can play in reverse; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="6b381-204">Einige Spieler können CLV-Scheiben in umgekehrter Reihenfolge und in den CAV-Bild Platten wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="6b381-204">Some players can play CLV discs in reverse as well as CAV discs.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI- \_ VD \_ getdevcaps- \_ CAV</span><span class="sxs-lookup"><span data-stu-id="6b381-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI\_VD\_GETDEVCAPS\_CAV</span></span>
</dt> <dd>

<span data-ttu-id="6b381-206">Gibt bei Kombination mit anderen Elementen an, dass die Rückgabe Informationen auf Videodisks im CAV-Format gelten.</span><span class="sxs-lookup"><span data-stu-id="6b381-206">When combined with other items, specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="6b381-207">Dies ist die Standardeinstellung, wenn keine Video Disk eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6b381-207">This is the default if no videodisc is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ getdevcaps \_ CLV</span><span class="sxs-lookup"><span data-stu-id="6b381-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI\_VD\_GETDEVCAPS\_CLV</span></span>
</dt> <dd>

<span data-ttu-id="6b381-209">Gibt bei Kombination mit anderen Elementen an, dass die Rückgabe Informationen auf Videodisks im CLV-Format zutreffen.</span><span class="sxs-lookup"><span data-stu-id="6b381-209">When combined with other items, specifies that the return information applies to CLV format videodiscs.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>schnelle Rate der MCI- \_ VD- \_ getdevcaps \_ \_</span><span class="sxs-lookup"><span data-stu-id="6b381-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI\_VD\_GETDEVCAPS\_FAST\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-211">Das **dwreturn** -Element wird auf die standardmäßige schnelle Wiedergabe Rate in Frames pro Sekunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-211">The **dwReturn** member is set to the standard fast play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI- \_ VD- \_ getdevcaps- \_ Normal \_ Rate</span><span class="sxs-lookup"><span data-stu-id="6b381-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI\_VD\_GETDEVCAPS\_NORMAL\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-213">Der **dwreturn** -Member wird auf die normale Wiedergabe Rate in Frames pro Sekunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-213">The **dwReturn** member is set to the normal play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>langsame MCI- \_ VD- \_ getdevcaps- \_ \_ Rate</span><span class="sxs-lookup"><span data-stu-id="6b381-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI\_VD\_GETDEVCAPS\_SLOW\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="6b381-215">Der **dwreturn** -Member ist auf die standardmäßige langsame Wiedergabe Rate in Frames pro Sekunde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-215">The **dwReturn** member is set to the standard slow play rate in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="6b381-216">Die folgenden Flags können im **dwitem** -Member von [**MCI \_ getdevcaps- \_ Parametern**](mci-getdevcaps-parms.md) für den **waveaudiogerätetyp** angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6b381-216">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="6b381-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI- \_ Wave \_ getdevcaps- \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b381-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI\_WAVE\_GETDEVCAPS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="6b381-218">Das **dwreturn** -Element wird auf die Gesamtzahl der Wellenform-Eingabegeräte (Aufzeichnung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-218">The **dwReturn** member is set to the total number of waveform input (recording) devices.</span></span>

</dd> <dt>

<span data-ttu-id="6b381-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI- \_ Wave \_ getdevcaps- \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="6b381-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI\_WAVE\_GETDEVCAPS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="6b381-220">Der **dwreturn** -Member ist auf die Gesamtzahl der Wellen Geräte-Ausgabegeräte (Wiedergabe) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b381-220">The **dwReturn** member is set to the total number of waveform output (playback) devices.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b381-221">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b381-221">Requirements</span></span>



| <span data-ttu-id="6b381-222">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b381-222">Requirement</span></span> | <span data-ttu-id="6b381-223">Wert</span><span class="sxs-lookup"><span data-stu-id="6b381-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b381-224">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b381-224">Minimum supported client</span></span><br/> | <span data-ttu-id="6b381-225">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b381-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6b381-226">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b381-226">Minimum supported server</span></span><br/> | <span data-ttu-id="6b381-227">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b381-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6b381-228">Header</span><span class="sxs-lookup"><span data-stu-id="6b381-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b381-229"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b381-229"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b381-230">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b381-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b381-231">MCI</span><span class="sxs-lookup"><span data-stu-id="6b381-231">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6b381-232">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="6b381-232">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

