---
title: MIM_DATA (Mmsystem.h)
description: Die MIM DATA-Nachricht wird an eine RÜCKRUF-Eingaberückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem \_ EINGABEGERÄT empfangen wird.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA Meldung Windows Multimedia
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
ms.openlocfilehash: a11d2701d488fe29ae6d0bc0742c32c803b28076
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118405"
---
# <a name="mim_data-message"></a><span data-ttu-id="ca208-104">MIM \_ DATA-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ca208-104">MIM\_DATA message</span></span>

<span data-ttu-id="ca208-105">Die **MIM \_ DATA-Nachricht** wird an eine RÜCKRUF-Eingaberückruffunktion gesendet, wenn eine FEHLERMELDUNG-Nachricht von einem EINGABEGERÄT empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ca208-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="ca208-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca208-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="ca208-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="ca208-108">DIE-Nachricht, die empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="ca208-108">MIDI message that was received.</span></span> <span data-ttu-id="ca208-109">Die Nachricht wird wie folgt in einen Doublewordwert gepackt:</span><span class="sxs-lookup"><span data-stu-id="ca208-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="ca208-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca208-110">Requirement</span></span> | <span data-ttu-id="ca208-111">Wert</span><span class="sxs-lookup"><span data-stu-id="ca208-111">Value</span></span> | <span data-ttu-id="ca208-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca208-112">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="ca208-113">Hohes Wort</span><span class="sxs-lookup"><span data-stu-id="ca208-113">High word</span></span> | <span data-ttu-id="ca208-114">High-Order-Byte</span><span class="sxs-lookup"><span data-stu-id="ca208-114">High-order byte</span></span> | <span data-ttu-id="ca208-115">Wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca208-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="ca208-116">Niedriges Byte</span><span class="sxs-lookup"><span data-stu-id="ca208-116">Low-order byte</span></span>  | <span data-ttu-id="ca208-117">Enthält (bei Bedarf) ein zweites Byte von DANN-Daten.</span><span class="sxs-lookup"><span data-stu-id="ca208-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="ca208-118">Niedriges Wort</span><span class="sxs-lookup"><span data-stu-id="ca208-118">Low word</span></span>  | <span data-ttu-id="ca208-119">High-Order-Byte</span><span class="sxs-lookup"><span data-stu-id="ca208-119">High-order byte</span></span> | <span data-ttu-id="ca208-120">Enthält (falls erforderlich) das erste Byte derTEN-Daten.</span><span class="sxs-lookup"><span data-stu-id="ca208-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="ca208-121">Niedriges Byte</span><span class="sxs-lookup"><span data-stu-id="ca208-121">Low-order byte</span></span>  | <span data-ttu-id="ca208-122">Enthält den STATUS DEST-Status.</span><span class="sxs-lookup"><span data-stu-id="ca208-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="ca208-123">Die beiden BYTES der BYTES-DATEN sind je nach STATUS-Byte optional.</span><span class="sxs-lookup"><span data-stu-id="ca208-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="ca208-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="ca208-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="ca208-125">Uhrzeit, zu der die Nachricht vom Eingabegerätetreiber empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="ca208-125">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="ca208-126">Der Zeitstempel wird in Millisekunden angegeben, beginnend bei 0 (null), als die [**funktion "formatInStart"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ca208-126">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca208-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca208-127">Return Value</span></span>

<span data-ttu-id="ca208-128">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ca208-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca208-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca208-129">Remarks</span></span>

<span data-ttu-id="ca208-130">Der Ausführungsstatus von über einen EINGABE-Eingabeport empfangenen SMS-Nachrichten ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca208-130">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="ca208-131">Diese Nachricht wird nicht gesendet, wenn eine exklusive SYSTEM-EXCLUSIVE-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ca208-131">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca208-132">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ca208-132">Requirements</span></span>



| <span data-ttu-id="ca208-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca208-133">Requirement</span></span> | <span data-ttu-id="ca208-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ca208-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca208-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca208-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ca208-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca208-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ca208-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca208-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ca208-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca208-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ca208-139">Header</span><span class="sxs-lookup"><span data-stu-id="ca208-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca208-140"><dt>Mmsystem.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca208-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca208-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca208-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca208-142">Instrument Digital Interface (KEYBOARD)</span><span class="sxs-lookup"><span data-stu-id="ca208-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="ca208-143">MESSAGES-Meldungen</span><span class="sxs-lookup"><span data-stu-id="ca208-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

