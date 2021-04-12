---
title: MCI_RESERVE Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Reserve ordnet dem Arbeitsbereich der Gerätetreiber Instanz zusammenhängenden Speicherplatz für die Verwendung bei der nachfolgenden Aufzeichnung zu. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956934"
---
# <a name="mci_reserve-command"></a><span data-ttu-id="63141-105">MCI- \_ Reserve Befehl</span><span class="sxs-lookup"><span data-stu-id="63141-105">MCI\_RESERVE command</span></span>

<span data-ttu-id="63141-106">Der Befehl MCI \_ Reserve ordnet dem Arbeitsbereich der Gerätetreiber Instanz zusammenhängenden Speicherplatz für die Verwendung bei der nachfolgenden Aufzeichnung zu.</span><span class="sxs-lookup"><span data-stu-id="63141-106">The MCI\_RESERVE command allocates contiguous disk space for the workspace of the device driver instance for use with subsequent recording.</span></span> <span data-ttu-id="63141-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="63141-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="63141-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="63141-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
);
```



## <a name="parameters"></a><span data-ttu-id="63141-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="63141-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63141-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="63141-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="63141-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="63141-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="63141-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="63141-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="63141-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="63141-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="63141-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="63141-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="63141-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpreserve*</span><span class="sxs-lookup"><span data-stu-id="63141-115"><span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*</span></span>
</dt> <dd>

<span data-ttu-id="63141-116">Zeiger auf eine [**MCI- \_ DGV- \_ Reserve- \_ Parametern**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="63141-116">Pointer to an [**MCI\_DGV\_RESERVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63141-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63141-117">Return Value</span></span>

<span data-ttu-id="63141-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="63141-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="63141-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63141-119">Remarks</span></span>

<span data-ttu-id="63141-120">Wenn der Arbeitsbereich nicht gespeicherte Daten enthält, gehen diese Daten verloren.</span><span class="sxs-lookup"><span data-stu-id="63141-120">If the workspace contains unsaved data, this data is lost.</span></span> <span data-ttu-id="63141-121">Wenn der Speicherplatz vor dem Aufzeichnen nicht reserviert ist, führt der [MCI- \_ Daten Satz](mci-record.md) Befehl eine implizite Reserve mit gerätespezifischen Standardparametern aus.</span><span class="sxs-lookup"><span data-stu-id="63141-121">If disk space is not reserved prior to recording, the [MCI\_RECORD](mci-record.md) command performs an implied reserve with device-specific default parameters.</span></span> <span data-ttu-id="63141-122">Bei manchen Implementierungen ist Reserve nicht erforderlich und kann vom Gerätetreiber ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="63141-122">On some implementations, reserve is not required and might be ignored by the device driver.</span></span> <span data-ttu-id="63141-123">Durch das explizite reservieren von Speicherplatz können Sie besser steuern, wann die Verzögerung für die Datenträger Zuordnung erfolgt, wie viel Speicherplatz belegt wird und wo der Speicherplatz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="63141-123">Explicitly reserving space gives you better control over when the delay for disk allocation occurs, how much space is allocated, and where the disk space is allocated.</span></span> <span data-ttu-id="63141-124">Die Menge und der Speicherort des bereits für diese Geräte Instanz reservierten Speicherplatzes können durch das erneute ausstellen der MCI-Reserve geändert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="63141-124">The amount and location of disk space already reserved for this device instance can be changed by issuing MCI\_RESERVE again.</span></span> <span data-ttu-id="63141-125">Der zugeordnete und noch nicht verwendete Speicherplatz wird nicht aufgehoben, bis aufgezeichnete Daten gespeichert werden oder bis die Gerätetreiber Instanz geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="63141-125">Any allocated and still unused disk space is not deallocated until any recorded data is saved or until the device driver instance is closed.</span></span>

<span data-ttu-id="63141-126">Wenn das Video mit dem MCI- \_ Flag off des Befehls [MCI \_ setvideo](mci-setvideo.md) ausgeschaltet ist, enthält der reservierte Speicherplatz kein Video.</span><span class="sxs-lookup"><span data-stu-id="63141-126">If video is turned off with the MCI\_OFF flag of the [MCI\_SETVIDEO](mci-setvideo.md) command, the space reserved does not include any video.</span></span> <span data-ttu-id="63141-127">Wenn Audiodaten mit dem MCI- \_ Flag off des Befehls [MCI \_ setaudioausgeschaltet](mci-setaudio.md) werden, umfasst der reservierte Speicherplatz keine Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="63141-127">If audio is turned off with the MCI\_OFF flag of the [MCI\_SETAUDIO](mci-setaudio.md) command, the space reserved does not include any audio.</span></span> <span data-ttu-id="63141-128">Wenn sowohl Audiodaten als auch Videos ausgeschaltet sind oder die angeforderte Größe 0 (null) ist, ist kein Speicherplatz reserviert, und der vorhandene reservierte Speicherplatz wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="63141-128">If both audio and video are turned off or if the requested size is zero, no space is reserved and any existing reserved space is deallocated.</span></span>

<span data-ttu-id="63141-129">Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="63141-129">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="63141-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI- \_ DGV- \_ Reserve \_ in</span><span class="sxs-lookup"><span data-stu-id="63141-130"><span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI\_DGV\_RESERVE\_IN</span></span>
</dt> <dd>

<span data-ttu-id="63141-131">Der **lpstrinpath** -Member der durch *lpreserve* identifizierten Struktur enthält die Adresse eines Puffers, der den Speicherort einer temporären Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="63141-131">The **lpstrPath** member of the structure identified by *lpReserve* contains an address of a buffer containing the location of a temporary file.</span></span> <span data-ttu-id="63141-132">Der Puffer enthält nur das Laufwerk und den Verzeichnispfad der Datei, die zum Speichern der aufgezeichneten Daten verwendet wird. der Dateiname wird vom Gerätetreiber angegeben.</span><span class="sxs-lookup"><span data-stu-id="63141-132">The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.</span></span> <span data-ttu-id="63141-133">Diese temporäre Datei wird gelöscht, wenn die Geräte Instanz geschlossen wird, es sei denn, Sie wird explizit gespeichert.</span><span class="sxs-lookup"><span data-stu-id="63141-133">This temporary file is deleted when the device instance is closed unless it is explicitly saved.</span></span> <span data-ttu-id="63141-134">Wenn dieses Flag weggelassen wird, gibt der Gerätetreiber an, wo Speicherplatz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="63141-134">If this flag is omitted, the device driver specifies where disk space is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="63141-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI- \_ DGV- \_ Reserve \_ Größe</span><span class="sxs-lookup"><span data-stu-id="63141-135"><span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI\_DGV\_RESERVE\_SIZE</span></span>
</dt> <dd>

<span data-ttu-id="63141-136">Der **dwSize** -Member der durch *lpreserve* identifizierten Struktur gibt die ungefähre Menge an Speicherplatz an, die im Arbeitsbereich für die Aufzeichnung reserviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="63141-136">The **dwSize** member of the structure identified by *lpReserve* specifies the approximate amount of disk space to reserve in the workspace for recording.</span></span> <span data-ttu-id="63141-137">Der Wert wird im aktuellen Zeitformat angegeben.</span><span class="sxs-lookup"><span data-stu-id="63141-137">The value is specified in the current time format.</span></span> <span data-ttu-id="63141-138">Die Menge des Speicherplatzes wird aus der angeforderten Zeit geschätzt und aus dem Dateiformat und Video-und audioalgorithmus sowie Qualitätswerten.</span><span class="sxs-lookup"><span data-stu-id="63141-138">The amount of disk space is estimated from the requested time and from which file format and video and audio algorithm and quality values are in effect.</span></span> <span data-ttu-id="63141-139">Wenn dieses Flag weggelassen wird, verwendet der Gerätetreiber möglicherweise einen Standardwert, den er definiert.</span><span class="sxs-lookup"><span data-stu-id="63141-139">If this flag is omitted, the device driver might use a default value it defines.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63141-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63141-140">Requirements</span></span>



| <span data-ttu-id="63141-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63141-141">Requirement</span></span> | <span data-ttu-id="63141-142">Wert</span><span class="sxs-lookup"><span data-stu-id="63141-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63141-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63141-143">Minimum supported client</span></span><br/> | <span data-ttu-id="63141-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63141-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="63141-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63141-145">Minimum supported server</span></span><br/> | <span data-ttu-id="63141-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63141-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="63141-147">Header</span><span class="sxs-lookup"><span data-stu-id="63141-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="63141-148"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63141-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63141-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63141-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63141-150">MCI</span><span class="sxs-lookup"><span data-stu-id="63141-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="63141-151">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="63141-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

