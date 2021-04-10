---
title: MM_MIM_MOREDATA Meldung (MMSYSTEM. h)
description: Die mm \_ MIM \_ MoreData-Nachricht wird an ein Rückruf Fenster gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird, die Anwendung jedoch MIM- \_ Daten Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabe-Gerätetreiber Schritt zu halten.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040581"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="c79ff-104">MM \_ MIM \_ MoreData-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c79ff-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="c79ff-105">Die **mm \_ MIM \_ MoreData** -Nachricht wird an ein Rückruf Fenster gesendet, wenn eine MIDI-Nachricht von einem MIDI-Eingabegerät empfangen wird, die Anwendung jedoch [**MIM- \_ Daten**](mim-data.md) Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabe-Gerätetreiber Schritt zu halten.</span><span class="sxs-lookup"><span data-stu-id="c79ff-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="c79ff-106">Das Fenster empfängt diese Meldung nur dann, wenn die Anwendung den Status der MIDI-e/a im-Befehl \_ \_ für die [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="c79ff-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="c79ff-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c79ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79ff-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*</span><span class="sxs-lookup"><span data-stu-id="c79ff-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="c79ff-109">Handle für das MIDI-Eingabegerät, das die MIDI-Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="c79ff-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="c79ff-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lmidimessage*</span><span class="sxs-lookup"><span data-stu-id="c79ff-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="c79ff-111">Gibt die empfangene MIDI-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="c79ff-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="c79ff-112">Die Nachricht wird wie folgt in einem Double Word-Wert verpackt:</span><span class="sxs-lookup"><span data-stu-id="c79ff-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="c79ff-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c79ff-113">Requirement</span></span> | <span data-ttu-id="c79ff-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c79ff-114">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="c79ff-115">Hohes Wort</span><span class="sxs-lookup"><span data-stu-id="c79ff-115">High word</span></span> | <span data-ttu-id="c79ff-116">Byte mit hoher Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c79ff-116">High-order byte</span></span> | <span data-ttu-id="c79ff-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c79ff-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="c79ff-118">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c79ff-118">Low-order byte</span></span>  | <span data-ttu-id="c79ff-119">Enthält ein zweites Byte von MIDI-Daten (bei Bedarf).</span><span class="sxs-lookup"><span data-stu-id="c79ff-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="c79ff-120">Niedriges Wort</span><span class="sxs-lookup"><span data-stu-id="c79ff-120">Low word</span></span>  | <span data-ttu-id="c79ff-121">Byte mit hoher Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c79ff-121">High-order byte</span></span> | <span data-ttu-id="c79ff-122">Enthält das erste Byte der MIDI-Daten (bei Bedarf).</span><span class="sxs-lookup"><span data-stu-id="c79ff-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="c79ff-123">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="c79ff-123">Low-order byte</span></span>  | <span data-ttu-id="c79ff-124">Enthält den Status von MIDI.</span><span class="sxs-lookup"><span data-stu-id="c79ff-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="c79ff-125">Die beiden Byte-Daten Bytes sind optional, abhängig vom Status Byte von MIDI.</span><span class="sxs-lookup"><span data-stu-id="c79ff-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c79ff-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c79ff-126">Return Value</span></span>

<span data-ttu-id="c79ff-127">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c79ff-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79ff-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c79ff-128">Remarks</span></span>

<span data-ttu-id="c79ff-129">Wenn Ihre Anwendung die Daten von MIDI schneller empfängt, als Sie verarbeiten kann, sollten Sie keinen Fenster Rückrufmechanismus verwenden.</span><span class="sxs-lookup"><span data-stu-id="c79ff-129">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="c79ff-130">Verwenden Sie zum Maximieren der Geschwindigkeit eine Rückruffunktion, und verwenden Sie die [**MIM \_ MoreData**](mim-moredata.md) -Nachricht anstelle von mm \_ MIM \_ MoreData.</span><span class="sxs-lookup"><span data-stu-id="c79ff-130">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="c79ff-131">Eine Anwendung sollte nur eine minimale Menge an Verarbeitung von mm \_ MIM- \_ Daten Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c79ff-131">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="c79ff-132">(Insbesondere sollten Anwendungen die [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion bei der Verarbeitung von mm \_ nicht aufzurufen. MIM \_ MoreData.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c79ff-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="c79ff-133">Wenn eine Anwendung eine [**mm \_ MIM- \_ Daten**](mm-mim-data.md) Nachricht nach einer Reihe von mm \_ MIM- \_ Daten Nachrichten empfängt, hat Sie eingehende MIDI-Ereignisse erfasst und kann zeitintensive Funktionen sicher aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c79ff-133">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="c79ff-134">Bei den von einem MIDI-eingabeport empfangenen MIDI-Nachrichten ist der Status " jede Nachricht wird so erweitert, dass Sie das MIDI-Status Byte enthält.</span><span class="sxs-lookup"><span data-stu-id="c79ff-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="c79ff-135">Diese Meldung wird nicht gesendet, wenn eine vom System exklusive System exklusive Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c79ff-135">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="c79ff-136">Mit dieser Meldung ist kein Zeitstempel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c79ff-136">No time stamp is available with this message.</span></span> <span data-ttu-id="c79ff-137">Für Zeitstempel-Eingabedaten müssen Sie die Nachrichten verwenden, die an Rückruf Funktionen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c79ff-137">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c79ff-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c79ff-138">Requirements</span></span>



| <span data-ttu-id="c79ff-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c79ff-139">Requirement</span></span> | <span data-ttu-id="c79ff-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c79ff-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c79ff-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c79ff-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c79ff-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c79ff-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c79ff-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c79ff-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c79ff-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c79ff-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c79ff-145">Header</span><span class="sxs-lookup"><span data-stu-id="c79ff-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c79ff-146"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c79ff-146"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c79ff-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c79ff-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79ff-148">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="c79ff-148">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="c79ff-149">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="c79ff-149">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

