---
title: MIM_MOREDATA Meldung (MMSYSTEM. h)
description: Die MIM \_ MoreData-Nachricht wird an eine Funktion für die Verwendung von MIDI-Eingaben gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird. die MIM-Daten Nachrichten werden von der Anwendung jedoch nicht \_ schnell genug verarbeitet, um mit dem Eingabegeräte Treiber zu arbeiten.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743929"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="d3739-104">MIM \_ MoreData-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d3739-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="d3739-105">Die **MIM \_ MoreData** -Nachricht wird an eine Funktion für die Verwendung von MIDI-Eingaben gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird. die [**MIM- \_ Daten**](mim-data.md) Nachrichten werden von der Anwendung jedoch nicht schnell genug verarbeitet, um mit dem Eingabegeräte Treiber zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3739-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="d3739-106">Die Rückruffunktion empfängt diese Nachricht nur dann, wenn die Anwendung den Status der MIDI-e/a \_ \_ im Aufrufs der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="d3739-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="d3739-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3739-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3739-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwmidimessage*</span><span class="sxs-lookup"><span data-stu-id="d3739-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="d3739-109">Gibt die empfangene MIDI-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="d3739-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="d3739-110">Die Nachricht wird wie folgt in einem **DWORD**-Wert verpackt:</span><span class="sxs-lookup"><span data-stu-id="d3739-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="d3739-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3739-111">Requirement</span></span> | <span data-ttu-id="d3739-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d3739-112">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="d3739-113">Hohes Wort</span><span class="sxs-lookup"><span data-stu-id="d3739-113">High word</span></span> | <span data-ttu-id="d3739-114">Byte mit hoher Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d3739-114">High-order byte</span></span> | <span data-ttu-id="d3739-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3739-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="d3739-116">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d3739-116">Low-order byte</span></span>  | <span data-ttu-id="d3739-117">Enthält ein zweites Byte von MIDI-Daten (bei Bedarf).</span><span class="sxs-lookup"><span data-stu-id="d3739-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="d3739-118">Niedriges Wort</span><span class="sxs-lookup"><span data-stu-id="d3739-118">Low word</span></span>  | <span data-ttu-id="d3739-119">Byte mit hoher Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d3739-119">High-order byte</span></span> | <span data-ttu-id="d3739-120">Enthält das erste Byte der MIDI-Daten (bei Bedarf).</span><span class="sxs-lookup"><span data-stu-id="d3739-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="d3739-121">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d3739-121">Low-order byte</span></span>  | <span data-ttu-id="d3739-122">Enthält den Status von MIDI.</span><span class="sxs-lookup"><span data-stu-id="d3739-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="d3739-123">Die beiden Byte-Daten Bytes sind optional, abhängig vom Status Byte von MIDI.</span><span class="sxs-lookup"><span data-stu-id="d3739-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="d3739-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwtimestamp*</span><span class="sxs-lookup"><span data-stu-id="d3739-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="d3739-125">Gibt die Uhrzeit an, zu der die Nachricht vom Eingabegeräte Treiber empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="d3739-125">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="d3739-126">Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0, wenn die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d3739-126">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3739-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3739-127">Return Value</span></span>

<span data-ttu-id="d3739-128">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d3739-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3739-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3739-129">Remarks</span></span>

<span data-ttu-id="d3739-130">Eine Anwendung sollte nur eine minimale Menge an Verarbeitung von MIM- \_ MoreData-Nachrichten durchführen.</span><span class="sxs-lookup"><span data-stu-id="d3739-130">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="d3739-131">(Insbesondere sollten Anwendungen die [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion bei der Verarbeitung von MIM \_ nicht aufzurufen. MoreData.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d3739-131">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="d3739-132">Wenn eine Anwendung eine [**MIM- \_ Daten**](mim-data.md) Nachricht nach einer Reihe von MIM- \_ Daten Nachrichten empfängt, hat Sie eingehende MIDI-Ereignisse erfasst und kann zeitintensive Funktionen sicher aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d3739-132">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="d3739-133">Bei den von einem MIDI-eingabeport empfangenen MIDI-Nachrichten ist der Status " jede Nachricht wird so erweitert, dass Sie das MIDI-Status Byte enthält.</span><span class="sxs-lookup"><span data-stu-id="d3739-133">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="d3739-134">Diese Meldung wird nicht gesendet, wenn eine vom System exklusive System exklusive Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="d3739-134">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3739-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3739-135">Requirements</span></span>



| <span data-ttu-id="d3739-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3739-136">Requirement</span></span> | <span data-ttu-id="d3739-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d3739-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3739-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3739-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d3739-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3739-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d3739-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3739-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d3739-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3739-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d3739-142">Header</span><span class="sxs-lookup"><span data-stu-id="d3739-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3739-143"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3739-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3739-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3739-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3739-145">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="d3739-145">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="d3739-146">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d3739-146">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

