---
title: MIM_DATA Meldung (MMSYSTEM. h)
description: Die MIM- \_ Daten Nachricht wird an eine MIDI-Eingabe Rückruffunktion gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859309"
---
# <a name="mim_data-message"></a><span data-ttu-id="49ebf-104">MIM- \_ Daten Nachricht</span><span class="sxs-lookup"><span data-stu-id="49ebf-104">MIM\_DATA message</span></span>

<span data-ttu-id="49ebf-105">Die **MIM- \_ Daten** Nachricht wird an eine MIDI-Eingabe Rückruffunktion gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="49ebf-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="49ebf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49ebf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ebf-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwmidimessage*</span><span class="sxs-lookup"><span data-stu-id="49ebf-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="49ebf-108">Die empfangene MIDI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="49ebf-108">MIDI message that was received.</span></span> <span data-ttu-id="49ebf-109">Die Nachricht wird wie folgt in einem Double Word-Wert verpackt:</span><span class="sxs-lookup"><span data-stu-id="49ebf-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="49ebf-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49ebf-110">Requirement</span></span> | <span data-ttu-id="49ebf-111">Wert</span><span class="sxs-lookup"><span data-stu-id="49ebf-111">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="49ebf-112">Hohes Wort</span><span class="sxs-lookup"><span data-stu-id="49ebf-112">High word</span></span> | <span data-ttu-id="49ebf-113">Byte mit hoher Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="49ebf-113">High-order byte</span></span> | <span data-ttu-id="49ebf-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="49ebf-114">Not used.</span></span>                                           |
|           | <span data-ttu-id="49ebf-115">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="49ebf-115">Low-order byte</span></span>  | <span data-ttu-id="49ebf-116">Enthält ein zweites Byte von MIDI-Daten (bei Bedarf).</span><span class="sxs-lookup"><span data-stu-id="49ebf-116">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="49ebf-117">Niedriges Wort</span><span class="sxs-lookup"><span data-stu-id="49ebf-117">Low word</span></span>  | <span data-ttu-id="49ebf-118">Byte mit hoher Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="49ebf-118">High-order byte</span></span> | <span data-ttu-id="49ebf-119">Enthält das erste Byte der MIDI-Daten (bei Bedarf).</span><span class="sxs-lookup"><span data-stu-id="49ebf-119">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="49ebf-120">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="49ebf-120">Low-order byte</span></span>  | <span data-ttu-id="49ebf-121">Enthält den Status von MIDI.</span><span class="sxs-lookup"><span data-stu-id="49ebf-121">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="49ebf-122">Die beiden Byte-Daten Bytes sind optional, abhängig vom Status Byte von MIDI.</span><span class="sxs-lookup"><span data-stu-id="49ebf-122">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="49ebf-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwtimestamp*</span><span class="sxs-lookup"><span data-stu-id="49ebf-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="49ebf-124">Der Zeitpunkt, zu dem die Nachricht vom Eingabegeräte Treiber empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="49ebf-124">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="49ebf-125">Der Zeitstempel wird in Millisekunden angegeben, beginnend bei Null, als die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="49ebf-125">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ebf-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49ebf-126">Return Value</span></span>

<span data-ttu-id="49ebf-127">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="49ebf-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49ebf-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49ebf-128">Remarks</span></span>

<span data-ttu-id="49ebf-129">Bei den von einem MIDI-eingabeport empfangenen MIDI-Nachrichten ist der Status " jede Nachricht wird so erweitert, dass Sie das MIDI-Status Byte enthält.</span><span class="sxs-lookup"><span data-stu-id="49ebf-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="49ebf-130">Diese Meldung wird nicht gesendet, wenn eine vom System exklusive System exklusive Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="49ebf-130">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ebf-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49ebf-131">Requirements</span></span>



| <span data-ttu-id="49ebf-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49ebf-132">Requirement</span></span> | <span data-ttu-id="49ebf-133">Wert</span><span class="sxs-lookup"><span data-stu-id="49ebf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49ebf-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49ebf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="49ebf-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49ebf-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49ebf-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49ebf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="49ebf-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49ebf-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49ebf-138">Header</span><span class="sxs-lookup"><span data-stu-id="49ebf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ebf-139"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49ebf-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49ebf-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49ebf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ebf-141">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="49ebf-141">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="49ebf-142">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="49ebf-142">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

