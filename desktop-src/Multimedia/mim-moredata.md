---
title: MIM_MOREDATA (Mmsystem.h)
description: Die MIM MOREDATA-Nachricht wird an eine EINGABE-Rückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem EINGABEEINGABE-Gerät empfangen wird, die Anwendung mim-DATENnachrichten jedoch nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber mithalten zu \_ \_ können.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA Meldung Windows Multimedia
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
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119405"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="dd5c0-104">MIM \_ MOREDATA-Nachricht</span><span class="sxs-lookup"><span data-stu-id="dd5c0-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="dd5c0-105">Die **MIM \_ MOREDATA-Nachricht** wird an eine EINGABE-Rückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem EINGABEEINGABE-Gerät empfangen wird, die Anwendung [**mim-DATENnachrichten \_**](mim-data.md) jedoch nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber mithalten zu können.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="dd5c0-106">Die Rückruffunktion empfängt diese Nachricht nur, wenn die Anwendung im Aufruf der \_ \_ funktion [**"eigenschaftInOpen"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) den STATUS DESEJO angibt.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="dd5c0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd5c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd5c0-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="dd5c0-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="dd5c0-109">Gibt die empfangene MESSAGE-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="dd5c0-110">Die Nachricht wird wie folgt in **einen DWORD-Wert** gepackt:</span><span class="sxs-lookup"><span data-stu-id="dd5c0-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="dd5c0-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd5c0-111">Requirement</span></span> | <span data-ttu-id="dd5c0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="dd5c0-112">Value</span></span> | <span data-ttu-id="dd5c0-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd5c0-113">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="dd5c0-114">Hohes Wort</span><span class="sxs-lookup"><span data-stu-id="dd5c0-114">High word</span></span> | <span data-ttu-id="dd5c0-115">High-Order-Byte</span><span class="sxs-lookup"><span data-stu-id="dd5c0-115">High-order byte</span></span> | <span data-ttu-id="dd5c0-116">Wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="dd5c0-117">Niedriges Byte</span><span class="sxs-lookup"><span data-stu-id="dd5c0-117">Low-order byte</span></span>  | <span data-ttu-id="dd5c0-118">Enthält (bei Bedarf) ein zweites Byte von DANN-Daten.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="dd5c0-119">Niedriges Wort</span><span class="sxs-lookup"><span data-stu-id="dd5c0-119">Low word</span></span>  | <span data-ttu-id="dd5c0-120">High-Order-Byte</span><span class="sxs-lookup"><span data-stu-id="dd5c0-120">High-order byte</span></span> | <span data-ttu-id="dd5c0-121">Enthält (falls erforderlich) das erste Byte derTEN-Daten.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="dd5c0-122">Niedriges Byte</span><span class="sxs-lookup"><span data-stu-id="dd5c0-122">Low-order byte</span></span>  | <span data-ttu-id="dd5c0-123">Enthält den STATUS DEST-Status.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="dd5c0-124">Die beiden BYTES der BYTES-DATEN sind je nach STATUS-Byte optional.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="dd5c0-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="dd5c0-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="dd5c0-126">Gibt den Zeitpunkt an, zu dem die Nachricht vom Eingabegerätetreiber empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-126">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="dd5c0-127">Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0, als die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-127">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd5c0-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd5c0-128">Return Value</span></span>

<span data-ttu-id="dd5c0-129">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-129">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd5c0-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd5c0-130">Remarks</span></span>

<span data-ttu-id="dd5c0-131">Eine Anwendung sollte nur einen minimalen Verarbeitungsaufwand für MIM \_ MOREDATA-Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-131">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="dd5c0-132">(Insbesondere sollten Anwendungen die [PostMessage-Funktion](/windows/win32/api/winuser/nf-winuser-postmessagea) bei der Verarbeitung von MIM nicht aufrufen. \_ MOREDATA.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="dd5c0-133">Wenn eine Anwendung nach einer Reihe von MIM MOREDATA-Nachrichten eine [**MIM \_ DATA-Nachricht**](mim-data.md) empfängt, ist sie mit eingehenden ANMELDUNG-Ereignissen auf dem Auffangen und kann zeitintensive \_ Funktionen sicher aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-133">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="dd5c0-134">Der Ausführungsstatus von über einen EINGABE-Eingabeport empfangenen SMS-Nachrichten ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="dd5c0-135">Diese Nachricht wird nicht gesendet, wenn eine exklusive SYSTEM-EXCLUSIVE-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="dd5c0-135">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd5c0-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dd5c0-136">Requirements</span></span>



| <span data-ttu-id="dd5c0-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd5c0-137">Requirement</span></span> | <span data-ttu-id="dd5c0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="dd5c0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5c0-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd5c0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="dd5c0-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd5c0-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dd5c0-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd5c0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="dd5c0-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd5c0-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dd5c0-143">Header</span><span class="sxs-lookup"><span data-stu-id="dd5c0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd5c0-144"><dt>Mmsystem.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd5c0-144"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd5c0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd5c0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd5c0-146">Instrument Digital Interface (KEYBOARD)</span><span class="sxs-lookup"><span data-stu-id="dd5c0-146">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="dd5c0-147">MESSAGES-Meldungen</span><span class="sxs-lookup"><span data-stu-id="dd5c0-147">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

