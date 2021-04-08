---
title: MCI_LOAD Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Load lädt eine Datei. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949403"
---
# <a name="mci_load-command"></a><span data-ttu-id="df4c7-105">Befehl "MCI \_ Load"</span><span class="sxs-lookup"><span data-stu-id="df4c7-105">MCI\_LOAD command</span></span>

<span data-ttu-id="df4c7-106">Der Befehl MCI \_ Load lädt eine Datei.</span><span class="sxs-lookup"><span data-stu-id="df4c7-106">The MCI\_LOAD command loads a file.</span></span> <span data-ttu-id="df4c7-107">Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="df4c7-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="df4c7-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="df4c7-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
);
```



## <a name="parameters"></a><span data-ttu-id="df4c7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="df4c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df4c7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="df4c7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="df4c7-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="df4c7-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="df4c7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="df4c7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="df4c7-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="df4c7-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="df4c7-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="df4c7-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="df4c7-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpload*</span><span class="sxs-lookup"><span data-stu-id="df4c7-115"><span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*</span></span>
</dt> <dd>

<span data-ttu-id="df4c7-116">Zeiger auf eine Struktur des [**MCI- \_ Lade- \_ Parametern**](mci-load-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="df4c7-116">Pointer to an [**MCI\_LOAD\_PARMS**](mci-load-parms.md) structure.</span></span> <span data-ttu-id="df4c7-117">(Geräte mit zusätzlichen Parametern können diese Struktur durch eine gerätespezifische Struktur ersetzen.</span><span class="sxs-lookup"><span data-stu-id="df4c7-117">(Devices with additional parameters might replace this structure with a device-specific structure.</span></span> <span data-ttu-id="df4c7-118">Für Digital Video-Geräte zeigt der **lpload** -Parameter auf eine [**MCI \_ DGV \_ \_**](/previous-versions//dd743391(v=vs.85)) -Struktur zum Laden von Daten.)</span><span class="sxs-lookup"><span data-stu-id="df4c7-118">For digital-video devices, the **lpLoad** parameter points to an [**MCI\_DGV\_LOAD\_PARMS**](/previous-versions//dd743391(v=vs.85)) structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df4c7-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df4c7-119">Return Value</span></span>

<span data-ttu-id="df4c7-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="df4c7-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="df4c7-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df4c7-121">Remarks</span></span>

<span data-ttu-id="df4c7-122">Das folgende zusätzliche Flag gilt für alle Geräte, die die MCI-Auslastung unterstützen \_ :</span><span class="sxs-lookup"><span data-stu-id="df4c7-122">The following additional flag applies to all devices supporting MCI\_LOAD:</span></span>

<dl> <dt>

<span data-ttu-id="df4c7-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI- \_ Auslastungs \_ Datei</span><span class="sxs-lookup"><span data-stu-id="df4c7-123"><span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>MCI\_LOAD\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="df4c7-124">Der **lpFileName** -Member der durch *lpload* identifizierten Struktur enthält eine Adresse eines Puffers, der den Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="df4c7-124">The **lpfilename** member of the structure identified by *lpLoad* contains an address of a buffer containing the filename.</span></span>

</dd> </dl>

<span data-ttu-id="df4c7-125">Das folgende zusätzliche Flag wird mit dem **Überlagerungs** Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="df4c7-125">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="df4c7-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="df4c7-126"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="df4c7-127">Der **RC** -Member der durch *lpload* identifizierten Struktur enthält ein gültiges Anzeige Rechteck, das den Bereich des zu aktualisierenden Video Puffers angibt.</span><span class="sxs-lookup"><span data-stu-id="df4c7-127">The **rc** member of the structure identified by *lpLoad* contains a valid display rectangle that identifies the area of the video buffer to update.</span></span>

</dd> </dl>

<span data-ttu-id="df4c7-128">Bei Video Überlagerungs Geräten verweist der *lpload* -Parameter auf eine MCI-Struktur für das [**\_ OVLY- \_ Laden von \_ para**](mci-ovly-load-parms.md) Metern.</span><span class="sxs-lookup"><span data-stu-id="df4c7-128">For video-overlay devices, the *lpLoad* parameter points to an [**MCI\_OVLY\_LOAD\_PARMS**](mci-ovly-load-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="df4c7-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df4c7-129">Requirements</span></span>



| <span data-ttu-id="df4c7-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df4c7-130">Requirement</span></span> | <span data-ttu-id="df4c7-131">Wert</span><span class="sxs-lookup"><span data-stu-id="df4c7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df4c7-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df4c7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="df4c7-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df4c7-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="df4c7-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df4c7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="df4c7-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df4c7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="df4c7-136">Header</span><span class="sxs-lookup"><span data-stu-id="df4c7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="df4c7-137"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df4c7-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df4c7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df4c7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df4c7-139">MCI</span><span class="sxs-lookup"><span data-stu-id="df4c7-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="df4c7-140">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="df4c7-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

