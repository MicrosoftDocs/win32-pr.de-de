---
title: MCI_QUALITY Befehl (MMSYSTEM. h)
description: Mit dem MCI \_ -Qualitäts Befehl wird eine benutzerdefinierte Qualität für die Datenkomprimierung von Audiodaten, Videodaten oder Bild Daten definiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391510"
---
# <a name="mci_quality-command"></a><span data-ttu-id="985f1-105">MCI- \_ Qualitäts Befehl</span><span class="sxs-lookup"><span data-stu-id="985f1-105">MCI\_QUALITY command</span></span>

<span data-ttu-id="985f1-106">Mit dem MCI \_ -Qualitäts Befehl wird eine benutzerdefinierte Qualität für die Datenkomprimierung von Audiodaten, Videodaten oder Bild Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="985f1-106">The MCI\_QUALITY command defines a custom quality level for audio, video, or still image data compression.</span></span> <span data-ttu-id="985f1-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="985f1-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="985f1-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="985f1-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
);
```



## <a name="parameters"></a><span data-ttu-id="985f1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="985f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="985f1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="985f1-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="985f1-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="985f1-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="985f1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="985f1-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="985f1-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="985f1-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="985f1-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="985f1-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="985f1-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpquality*</span><span class="sxs-lookup"><span data-stu-id="985f1-115"><span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*</span></span>
</dt> <dd>

<span data-ttu-id="985f1-116">Zeiger auf eine [**MCI \_ DGV \_ Quality \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="985f1-116">Pointer to an [**MCI\_DGV\_QUALITY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="985f1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="985f1-117">Return Value</span></span>

<span data-ttu-id="985f1-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="985f1-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="985f1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="985f1-119">Remarks</span></span>

<span data-ttu-id="985f1-120">Der Name, der für diese Qualitätsstufe definiert ist, kann beim Festlegen der Audiodatei, des Videos oder der Qualität mit den Befehls [MCI \_ setaudiound](mci-setaudio.md) [MCI \_ setvideo](mci-setvideo.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="985f1-120">The name defined for this quality level can be used when setting the audio, video, or still quality with the [MCI\_SETAUDIO](mci-setaudio.md) and [MCI\_SETVIDEO](mci-setvideo.md) commands.</span></span>

<span data-ttu-id="985f1-121">Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="985f1-121">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="985f1-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ Quality \_ alg</span><span class="sxs-lookup"><span data-stu-id="985f1-122"><span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI\_QUALITY\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="985f1-123">Der **lpstrinalgorithmus** -Member der Struktur, die von *lpquality* identifiziert wird, enthält eine Adresse eines Puffers, der den Namen des Algorithmus enthält.</span><span class="sxs-lookup"><span data-stu-id="985f1-123">The **lpstrAlgorithm** member of the structure identified by *lpQuality* contains an address of a buffer containing the name of the algorithm.</span></span> <span data-ttu-id="985f1-124">Dieser Algorithmus muss vom Gerätetreiber unterstützt werden und muss mit dem verwendeten audiodeskriptor (noch) und dem verwendeten Video Deskriptor kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="985f1-124">This algorithm must be supported by the device driver, and must be compatible with the audio, still, or video descriptor that is used.</span></span> <span data-ttu-id="985f1-125">Wenn dieses Flag weggelassen wird, wird der aktuelle Algorithmus verwendet.</span><span class="sxs-lookup"><span data-stu-id="985f1-125">If this flag is omitted, the current algorithm is used.</span></span>

</dd> <dt>

<span data-ttu-id="985f1-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI- \_ Qualitäts \_ Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="985f1-126"><span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>MCI\_QUALITY\_DIALOG</span></span>
</dt> <dd>

<span data-ttu-id="985f1-127">Der Gerätetreiber sollte ein Dialogfeld zum Angeben der Qualitäts Ebene anzeigen.</span><span class="sxs-lookup"><span data-stu-id="985f1-127">The device driver should display a dialog box for specifying the quality level.</span></span> <span data-ttu-id="985f1-128">Das Dialogfeld enthält algorithmusspezifische Felder, die intern vom Gerätetreiber verwendet werden, um eine Struktur zu erstellen, die eine bestimmte Qualitätsstufe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="985f1-128">The dialog box has algorithm-specific fields used internally by the device driver to create a structure describing a specific quality level.</span></span>

</dd> <dt>

<span data-ttu-id="985f1-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI- \_ Qualitäts \_ handle</span><span class="sxs-lookup"><span data-stu-id="985f1-129"><span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI\_QUALITY\_HANDLE</span></span>
</dt> <dd>

<span data-ttu-id="985f1-130">Der **dwhandle** -Member der-Struktur, die von *lpquality* identifiziert wird, enthält ein Handle für eine-Struktur.</span><span class="sxs-lookup"><span data-stu-id="985f1-130">The **dwHandle** member of the structure identified by *lpQuality* contains a handle to a structure.</span></span> <span data-ttu-id="985f1-131">Die Struktur enthält algorithmische spezifische Daten, die die jeweilige Qualitätsstufe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="985f1-131">The structure contains algorithmic-specific data describing the specific quality level.</span></span> <span data-ttu-id="985f1-132">Das Format der Strukturen für die Algorithmen ist Geräte abhängig.</span><span class="sxs-lookup"><span data-stu-id="985f1-132">The format of the structures for the algorithms is device dependent.</span></span>

</dd> <dt>

<span data-ttu-id="985f1-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI- \_ Qualitäts \_ Element</span><span class="sxs-lookup"><span data-stu-id="985f1-133"><span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>MCI\_QUALITY\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="985f1-134">Eine-Konstante, die angibt, dass der Algorithmustyp im **dwitem** -Member der durch *lpquality* identifizierten-Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="985f1-134">A constant indicating the type of algorithm is included in the **dwItem** member of the structure identified by *lpQuality*.</span></span>

</dd> <dt>

<span data-ttu-id="985f1-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>Name der MCI- \_ Qualität \_</span><span class="sxs-lookup"><span data-stu-id="985f1-135"><span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI\_QUALITY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="985f1-136">Der **lpstrinname** -Member der Struktur, die von *lpquality* identifiziert wird, enthält eine Adresse eines Puffers, der den Qualitäts Deskriptor enthält.</span><span class="sxs-lookup"><span data-stu-id="985f1-136">The **lpstrName** member of the structure identified by *lpQuality* contains an address of a buffer containing the quality descriptor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="985f1-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="985f1-137">Requirements</span></span>



| <span data-ttu-id="985f1-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="985f1-138">Requirement</span></span> | <span data-ttu-id="985f1-139">Wert</span><span class="sxs-lookup"><span data-stu-id="985f1-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985f1-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="985f1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="985f1-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="985f1-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="985f1-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="985f1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="985f1-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="985f1-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="985f1-144">Header</span><span class="sxs-lookup"><span data-stu-id="985f1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="985f1-145"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="985f1-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985f1-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="985f1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985f1-147">MCI</span><span class="sxs-lookup"><span data-stu-id="985f1-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="985f1-148">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="985f1-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

