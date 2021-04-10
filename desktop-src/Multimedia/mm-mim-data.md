---
title: MM_MIM_DATA Meldung (MMSYSTEM. h)
description: Die mm \_ MIM- \_ Daten Nachricht wird an ein Fenster gesendet, wenn von einem MIDI-Eingabegerät eine komplette MIDI-Nachricht empfangen wird.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA-Nachricht (Multimedia)
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
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040213"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="15447-104">MM \_ MIM- \_ Daten Nachricht</span><span class="sxs-lookup"><span data-stu-id="15447-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="15447-105">Die **mm \_ MIM- \_ Daten** Nachricht wird an ein Fenster gesendet, wenn von einem MIDI-Eingabegerät eine komplette MIDI-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="15447-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="15447-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15447-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15447-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*</span><span class="sxs-lookup"><span data-stu-id="15447-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="15447-108">Handle für das MIDI-Eingabegerät, das die MIDI-Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="15447-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="15447-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lmidimessage*</span><span class="sxs-lookup"><span data-stu-id="15447-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="15447-110">Die empfangene MIDI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="15447-110">MIDI message that was received.</span></span> <span data-ttu-id="15447-111">Die Nachricht wird wie folgt in einem Double Word-Wert verpackt:</span><span class="sxs-lookup"><span data-stu-id="15447-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="15447-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15447-112">Requirement</span></span> | <span data-ttu-id="15447-113">Wert</span><span class="sxs-lookup"><span data-stu-id="15447-113">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="15447-114">Hohes Wort</span><span class="sxs-lookup"><span data-stu-id="15447-114">High word</span></span> | <span data-ttu-id="15447-115">Byte mit hoher Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="15447-115">High-order byte</span></span> | <span data-ttu-id="15447-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="15447-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="15447-117">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="15447-117">Low-order byte</span></span>  | <span data-ttu-id="15447-118">Enthält ein zweites Byte von MIDI-Daten (bei Bedarf).</span><span class="sxs-lookup"><span data-stu-id="15447-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="15447-119">Niedriges Wort</span><span class="sxs-lookup"><span data-stu-id="15447-119">Low word</span></span>  | <span data-ttu-id="15447-120">Byte mit hoher Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="15447-120">High-order byte</span></span> | <span data-ttu-id="15447-121">Enthält das erste Byte der MIDI-Daten (bei Bedarf).</span><span class="sxs-lookup"><span data-stu-id="15447-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="15447-122">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="15447-122">Low-order byte</span></span>  | <span data-ttu-id="15447-123">Enthält den Status von MIDI.</span><span class="sxs-lookup"><span data-stu-id="15447-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="15447-124">Die beiden Byte-Daten Bytes sind optional, abhängig vom Status Byte von MIDI.</span><span class="sxs-lookup"><span data-stu-id="15447-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15447-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15447-125">Return Value</span></span>

<span data-ttu-id="15447-126">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="15447-126">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15447-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15447-127">Remarks</span></span>

<span data-ttu-id="15447-128">Bei den von einem MIDI-eingabeport empfangenen MIDI-Nachrichten ist der Status " jede Nachricht wird so erweitert, dass Sie das MIDI-Status Byte enthält.</span><span class="sxs-lookup"><span data-stu-id="15447-128">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="15447-129">Diese Meldung wird nicht gesendet, wenn eine vom System exklusive System exklusive Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="15447-129">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="15447-130">Mit dieser Meldung ist kein Zeitstempel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15447-130">No time stamp is available with this message.</span></span> <span data-ttu-id="15447-131">Für Zeitstempel-Eingabedaten müssen Sie die Nachrichten verwenden, die an Rückruf Funktionen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="15447-131">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="15447-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15447-132">Requirements</span></span>



| <span data-ttu-id="15447-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15447-133">Requirement</span></span> | <span data-ttu-id="15447-134">Wert</span><span class="sxs-lookup"><span data-stu-id="15447-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15447-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15447-135">Minimum supported client</span></span><br/> | <span data-ttu-id="15447-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15447-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15447-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15447-137">Minimum supported server</span></span><br/> | <span data-ttu-id="15447-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15447-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15447-139">Header</span><span class="sxs-lookup"><span data-stu-id="15447-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="15447-140"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15447-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15447-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15447-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15447-142">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="15447-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="15447-143">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="15447-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





