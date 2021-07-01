---
title: MM_MIM_DATA (Mmsystem.h)
description: Die MM MIM DATA-Nachricht wird an ein Fenster gesendet, wenn eine vollständige DANN-Nachricht von einem \_ \_ EINGABEGERÄT empfangen wird.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA Meldung Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119695"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="5d46f-104">MM \_ MIM \_ DATA-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5d46f-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="5d46f-105">Die **MM \_ MIM \_ DATA-Nachricht** wird an ein Fenster gesendet, wenn eine vollständige DANN-Nachricht von einem EINGABEGERÄT empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="5d46f-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="5d46f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d46f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d46f-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="5d46f-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="5d46f-108">Handle für das EINGABE-Eingabegerät, das die FEHLERMELDUNG-Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="5d46f-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="5d46f-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="5d46f-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="5d46f-110">DIE-Nachricht, die empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="5d46f-110">MIDI message that was received.</span></span> <span data-ttu-id="5d46f-111">Die Nachricht wird wie folgt in einen Doublewordwert gepackt:</span><span class="sxs-lookup"><span data-stu-id="5d46f-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="5d46f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d46f-112">Requirement</span></span> | <span data-ttu-id="5d46f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5d46f-113">Value</span></span> | <span data-ttu-id="5d46f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d46f-114">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="5d46f-115">Hohes Wort</span><span class="sxs-lookup"><span data-stu-id="5d46f-115">High word</span></span> | <span data-ttu-id="5d46f-116">High-Order-Byte</span><span class="sxs-lookup"><span data-stu-id="5d46f-116">High-order byte</span></span> | <span data-ttu-id="5d46f-117">Wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d46f-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="5d46f-118">Niedriges Byte</span><span class="sxs-lookup"><span data-stu-id="5d46f-118">Low-order byte</span></span>  | <span data-ttu-id="5d46f-119">Enthält (bei Bedarf) ein zweites Byte von DANN-Daten.</span><span class="sxs-lookup"><span data-stu-id="5d46f-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="5d46f-120">Niedriges Wort</span><span class="sxs-lookup"><span data-stu-id="5d46f-120">Low word</span></span>  | <span data-ttu-id="5d46f-121">High-Order-Byte</span><span class="sxs-lookup"><span data-stu-id="5d46f-121">High-order byte</span></span> | <span data-ttu-id="5d46f-122">Enthält (falls erforderlich) das erste Byte derTEN-Daten.</span><span class="sxs-lookup"><span data-stu-id="5d46f-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="5d46f-123">Niedriges Byte</span><span class="sxs-lookup"><span data-stu-id="5d46f-123">Low-order byte</span></span>  | <span data-ttu-id="5d46f-124">Enthält den STATUS DEST-Status.</span><span class="sxs-lookup"><span data-stu-id="5d46f-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="5d46f-125">Die beiden BYTES der BYTES-DATEN sind je nach STATUS-Byte optional.</span><span class="sxs-lookup"><span data-stu-id="5d46f-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d46f-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d46f-126">Return Value</span></span>

<span data-ttu-id="5d46f-127">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5d46f-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d46f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d46f-128">Remarks</span></span>

<span data-ttu-id="5d46f-129">Der Ausführungsstatus von über einen EINGABE-Eingabeport empfangenen SMS-Nachrichten ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="5d46f-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="5d46f-130">Diese Nachricht wird nicht gesendet, wenn eine exklusive SYSTEM-EXCLUSIVE-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="5d46f-130">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="5d46f-131">Für diese Nachricht ist kein Zeitstempel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d46f-131">No time stamp is available with this message.</span></span> <span data-ttu-id="5d46f-132">Für Eingabedaten mit Zeitstempel müssen Sie die Nachrichten verwenden, die an Rückruffunktionen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d46f-132">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d46f-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5d46f-133">Requirements</span></span>



| <span data-ttu-id="5d46f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d46f-134">Requirement</span></span> | <span data-ttu-id="5d46f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5d46f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d46f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d46f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5d46f-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d46f-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5d46f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d46f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5d46f-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d46f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5d46f-140">Header</span><span class="sxs-lookup"><span data-stu-id="5d46f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d46f-141"><dt>Mmsystem.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d46f-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d46f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d46f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d46f-143">Instrument Digital Interface (KEYBOARD)</span><span class="sxs-lookup"><span data-stu-id="5d46f-143">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="5d46f-144">MESSAGES-Meldungen</span><span class="sxs-lookup"><span data-stu-id="5d46f-144">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





