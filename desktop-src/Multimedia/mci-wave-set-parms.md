---
title: MCI_WAVE_SET_PARMS-Struktur (mciapi. h)
description: Die Struktur von MCI \_ \_ -Wellen Satz \_ -Parametern enthält Informationen zum MCI \_ -Befehl Set für Waveform-Audiogeräte.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- MCI_WAVE_SET_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859221"
---
# <a name="mci_wave_set_parms-structure"></a><span data-ttu-id="a30f9-104">Struktur von MCI- \_ Wellen \_ Satz- \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="a30f9-104">MCI\_WAVE\_SET\_PARMS structure</span></span>

<span data-ttu-id="a30f9-105">Die Struktur von **MCI- \_ Wellen \_ Satz- \_ Parametern** enthält Informationen zum [**MCI-Befehl \_ Set**](mci-set.md) für Waveform-Audiogeräte.</span><span class="sxs-lookup"><span data-stu-id="a30f9-105">The **MCI\_WAVE\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30f9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a30f9-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="a30f9-107">Member</span><span class="sxs-lookup"><span data-stu-id="a30f9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a30f9-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="a30f9-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="a30f9-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-110">**dwtimeformat**</span><span class="sxs-lookup"><span data-stu-id="a30f9-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-111">Das Zeitformat des Geräts.</span><span class="sxs-lookup"><span data-stu-id="a30f9-111">Device's time format.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-112">**dwaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="a30f9-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-113">Die Kanalnummer für die Audioausgabe.</span><span class="sxs-lookup"><span data-stu-id="a30f9-113">Channel number for audio output.</span></span> <span data-ttu-id="a30f9-114">Wird normalerweise verwendet, wenn ein Kanal ein-oder ausgeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="a30f9-114">Typically used when turning a channel on or off.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-115">**Winput**</span><span class="sxs-lookup"><span data-stu-id="a30f9-115">**wInput**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-116">Audioeingabechannel.</span><span class="sxs-lookup"><span data-stu-id="a30f9-116">Audio input channel.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-117">**woutput**</span><span class="sxs-lookup"><span data-stu-id="a30f9-117">**wOutput**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-118">Ausgabegerät, das verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a30f9-118">Output device to use.</span></span> <span data-ttu-id="a30f9-119">Dieser Wert kann z. b. 2 lauten, wenn ein System über zwei installierte Soundkarten verfügt.</span><span class="sxs-lookup"><span data-stu-id="a30f9-119">For example, this value could be 2 if a system had two installed sound cards.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-120">**wformattag**</span><span class="sxs-lookup"><span data-stu-id="a30f9-120">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-121">Format der Waveform-Audiodaten, z. b. Wave- \_ Format \_ PCM.</span><span class="sxs-lookup"><span data-stu-id="a30f9-121">Format of the waveform-audio data, such as WAVE\_FORMAT\_PCM.</span></span> <span data-ttu-id="a30f9-122">Mögliche Werte sind in "mmreg. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="a30f9-122">Possible values are defined in Mmreg.h.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-123">**wReserved2**</span><span class="sxs-lookup"><span data-stu-id="a30f9-123">**wReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-124">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a30f9-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-125">**nchannels**</span><span class="sxs-lookup"><span data-stu-id="a30f9-125">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-126">Mono (1) oder Stereo (2).</span><span class="sxs-lookup"><span data-stu-id="a30f9-126">Mono (1) or stereo (2).</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-127">**wReserved3**</span><span class="sxs-lookup"><span data-stu-id="a30f9-127">**wReserved3**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-128">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a30f9-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-129">**nsamplespersec**</span><span class="sxs-lookup"><span data-stu-id="a30f9-129">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-130">Stichproben pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="a30f9-130">Samples per second.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-131">**navgbytespersec**</span><span class="sxs-lookup"><span data-stu-id="a30f9-131">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-132">Die Stichprobenrate in Byte pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="a30f9-132">Sample rate in bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-133">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="a30f9-133">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-134">Blockieren der Ausrichtung der Daten.</span><span class="sxs-lookup"><span data-stu-id="a30f9-134">Block alignment of the data.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-135">**wReserved4**</span><span class="sxs-lookup"><span data-stu-id="a30f9-135">**wReserved4**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-136">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a30f9-136">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-137">**wbitspersample**</span><span class="sxs-lookup"><span data-stu-id="a30f9-137">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-138">Bits pro Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="a30f9-138">Bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="a30f9-139">**wReserved5**</span><span class="sxs-lookup"><span data-stu-id="a30f9-139">**wReserved5**</span></span>
</dt> <dd>

<span data-ttu-id="a30f9-140">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a30f9-140">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a30f9-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a30f9-141">Remarks</span></span>

<span data-ttu-id="a30f9-142">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a30f9-142">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="a30f9-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a30f9-143">Requirements</span></span>



| <span data-ttu-id="a30f9-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a30f9-144">Requirement</span></span> | <span data-ttu-id="a30f9-145">Wert</span><span class="sxs-lookup"><span data-stu-id="a30f9-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a30f9-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a30f9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a30f9-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a30f9-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a30f9-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a30f9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a30f9-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a30f9-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a30f9-150">Header</span><span class="sxs-lookup"><span data-stu-id="a30f9-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="a30f9-151"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a30f9-151"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a30f9-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a30f9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30f9-153">**MCI**</span><span class="sxs-lookup"><span data-stu-id="a30f9-153">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a30f9-154">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="a30f9-154">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="a30f9-155">**MCI- \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="a30f9-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="a30f9-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a30f9-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

