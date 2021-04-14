---
title: MCI_VCR_SET_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Set- \_ Parameter enthält Parameter für den MCI- \_ Befehl Set für Video-Kassetten-Recorder.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- MCI_VCR_SET_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392152"
---
# <a name="mci_vcr_set_parms-structure"></a><span data-ttu-id="1072a-104">Struktur der MCI- \_ VCR- \_ Set- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="1072a-104">MCI\_VCR\_SET\_PARMS structure</span></span>

<span data-ttu-id="1072a-105">Die Struktur der **MCI- \_ VCR- \_ Set \_** -Parameter enthält Parameter für den [**MCI-Befehl \_ Set**](mci-set.md) für Video-Kassetten-Recorder.</span><span class="sxs-lookup"><span data-stu-id="1072a-105">The **MCI\_VCR\_SET\_PARMS** structure contains parameters for the [**MCI\_SET**](mci-set.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="1072a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1072a-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="1072a-107">Member</span><span class="sxs-lookup"><span data-stu-id="1072a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1072a-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="1072a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="1072a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-110">**dwtimeformat**</span><span class="sxs-lookup"><span data-stu-id="1072a-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-111">Aktuelles Uhrzeit Format.</span><span class="sxs-lookup"><span data-stu-id="1072a-111">Current time format.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-112">**dwaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="1072a-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1072a-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-114">**dwtimemode**</span><span class="sxs-lookup"><span data-stu-id="1072a-114">**dwTimeMode**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-115">-Konstante, die die vom Gerät verwendete Zeit Steuerungs Quelle angibt.</span><span class="sxs-lookup"><span data-stu-id="1072a-115">Constant that specifies the timing source used by the device.</span></span> <span data-ttu-id="1072a-116">Bei der Zeit Steuerungs Quelle handelt es sich entweder um eine auf Videoband aufgezeichnete Zeit Leitzahl oder um die Leistungsindikatoren auf dem Gerät, die die videobandbewegung verstehen.</span><span class="sxs-lookup"><span data-stu-id="1072a-116">The timing source is either a timecode recorded on videotape, or the counters in the device that sense videotape movement.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-117">**dwrecordformat**</span><span class="sxs-lookup"><span data-stu-id="1072a-117">**dwRecordFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-118">Aufzeichnungsrate.</span><span class="sxs-lookup"><span data-stu-id="1072a-118">Recording rate.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-119">**dwcounter Format**</span><span class="sxs-lookup"><span data-stu-id="1072a-119">**dwCounterFormat**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-120">Format eines neuen Leistungswert Werts.</span><span class="sxs-lookup"><span data-stu-id="1072a-120">Format of a new counter time value.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-121">**dwIndex**</span><span class="sxs-lookup"><span data-stu-id="1072a-121">**dwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-122">Inhalt der Bildschirm Anzeige.</span><span class="sxs-lookup"><span data-stu-id="1072a-122">Contents of on-screen display.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-123">**dwtracking**</span><span class="sxs-lookup"><span data-stu-id="1072a-123">**dwTracking**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-124">Beim Nachverfolgen der VCR-Wiedergabe Rate verwendete Geschwindigkeitsanpassung.</span><span class="sxs-lookup"><span data-stu-id="1072a-124">Speed adjustment used when tracking the VCR playback rate.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-125">**dwspeed**</span><span class="sxs-lookup"><span data-stu-id="1072a-125">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-126">Wiedergabegeschwindigkeit, die vom Gerät als ganze Zahl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1072a-126">Playback speed used by the device as an integer.</span></span> <span data-ttu-id="1072a-127">Die normale Wiedergabegeschwindigkeit ist 1000, doppelte Geschwindigkeit 2000 und halb Geschwindigkeit 500.</span><span class="sxs-lookup"><span data-stu-id="1072a-127">Normal playback speed is 1000, double speed is 2000, and half speed is 500.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-128">**dwLength**</span><span class="sxs-lookup"><span data-stu-id="1072a-128">**dwLength**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-129">Die Länge des Videobands, wenn die Länge vom Gerät nicht erkennbar ist.</span><span class="sxs-lookup"><span data-stu-id="1072a-129">Videotape length when the length is undetectable by the device.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-130">**dwcounter**</span><span class="sxs-lookup"><span data-stu-id="1072a-130">**dwCounter**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-131">Neuer Leistungswert.</span><span class="sxs-lookup"><span data-stu-id="1072a-131">New counter value.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-132">**dwclock**</span><span class="sxs-lookup"><span data-stu-id="1072a-132">**dwClock**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-133">Neue Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="1072a-133">New clock time.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-134">**dwpaustitimeout**</span><span class="sxs-lookup"><span data-stu-id="1072a-134">**dwPauseTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-135">Neuer Timeout Wert für den anhaltebefehl.</span><span class="sxs-lookup"><span data-stu-id="1072a-135">New timeout value for pause command.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-136">**dwprerollduration**</span><span class="sxs-lookup"><span data-stu-id="1072a-136">**dwPrerollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-137">Die für die Stabilisierung der VCR-Ausgabe benötigte videobandlänge.</span><span class="sxs-lookup"><span data-stu-id="1072a-137">Videotape length needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="1072a-138">**dwpostrollduration**</span><span class="sxs-lookup"><span data-stu-id="1072a-138">**dwPostrollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="1072a-139">Die für den VCR-Transport erforderliche Video Bandlänge, wenn ein [**MCI \_**](mci-stop.md) -Befehl zum Beenden oder ein [**MCI \_**](mci-pause.md) -anhaltebefehl ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1072a-139">Videotape length needed to brake the VCR transport when a [**MCI\_STOP**](mci-stop.md) or [**MCI\_PAUSE**](mci-pause.md) command is issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1072a-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1072a-140">Remarks</span></span>

<span data-ttu-id="1072a-141">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1072a-141">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="1072a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1072a-142">Requirements</span></span>



| <span data-ttu-id="1072a-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1072a-143">Requirement</span></span> | <span data-ttu-id="1072a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1072a-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1072a-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1072a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1072a-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1072a-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1072a-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1072a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1072a-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1072a-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1072a-149">Header</span><span class="sxs-lookup"><span data-stu-id="1072a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="1072a-150"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="1072a-150"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1072a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1072a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1072a-152">**MCI**</span><span class="sxs-lookup"><span data-stu-id="1072a-152">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1072a-153">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="1072a-153">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="1072a-154">**MCI- \_ Pause**</span><span class="sxs-lookup"><span data-stu-id="1072a-154">**MCI\_PAUSE**</span></span>](mci-pause.md)
</dt> <dt>

[<span data-ttu-id="1072a-155">**MCI- \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="1072a-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="1072a-156">**MCI- \_ Beendigung**</span><span class="sxs-lookup"><span data-stu-id="1072a-156">**MCI\_STOP**</span></span>](mci-stop.md)
</dt> <dt>

<span data-ttu-id="1072a-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1072a-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

