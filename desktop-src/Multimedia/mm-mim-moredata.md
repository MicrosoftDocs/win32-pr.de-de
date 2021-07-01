---
title: MM_MIM_MOREDATA Meldung (Mmsystem.h)
description: Die MM \_ MIM \_ MOREDATA-Nachricht wird an ein Rückruffenster gesendet, wenn eine RÜCKRUFNACHRICHT von einem EINGABEGERÄT empfangen wird, die Anwendung jedoch MIM \_ DATA-Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber Schritt zu halten.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA Meldung Windows Multimedia
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
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120025"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="1c101-104">MM \_ MIM \_ MOREDATA-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1c101-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="1c101-105">Die **MM \_ MIM \_ MOREDATA-Nachricht** wird an ein Rückruffenster gesendet, wenn eine RÜCKRUFNACHRICHT von einem INPUT-Eingabegerät empfangen wird, die Anwendung jedoch [**MIM \_ DATA-Nachrichten**](mim-data.md) nicht schnell genug verarbeitet, um mit dem Eingabegerätetreiber Schritt zu halten.</span><span class="sxs-lookup"><span data-stu-id="1c101-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="1c101-106">Das Fenster empfängt diese Meldung nur, wenn die Anwendung IM \_ \_ Aufruf der funktion [**"arsInOpen"**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) den STATUS DER IO-E/A-Funktion VON DER ANWENDUNG angibt.</span><span class="sxs-lookup"><span data-stu-id="1c101-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="1c101-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c101-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c101-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="1c101-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="1c101-109">Handle für das EINGABEGERÄT, das die FEHLERMELDUNG erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="1c101-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="1c101-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="1c101-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="1c101-111">Gibt die empfangene FEHLERMELDUNG AN.</span><span class="sxs-lookup"><span data-stu-id="1c101-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="1c101-112">Die Nachricht wird wie folgt in einen Doubleword-Wert gepackt:</span><span class="sxs-lookup"><span data-stu-id="1c101-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="1c101-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c101-113">Requirement</span></span> | <span data-ttu-id="1c101-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1c101-114">Value</span></span> | <span data-ttu-id="1c101-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c101-115">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="1c101-116">Hohes Wort</span><span class="sxs-lookup"><span data-stu-id="1c101-116">High word</span></span> | <span data-ttu-id="1c101-117">Hohe Bytereihenfolge</span><span class="sxs-lookup"><span data-stu-id="1c101-117">High-order byte</span></span> | <span data-ttu-id="1c101-118">Wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c101-118">Not used.</span></span>                                           |
|           | <span data-ttu-id="1c101-119">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1c101-119">Low-order byte</span></span>  | <span data-ttu-id="1c101-120">Enthält bei Bedarf ein zweites Byte mit QUOTA-Daten.</span><span class="sxs-lookup"><span data-stu-id="1c101-120">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="1c101-121">Niedriges Wort</span><span class="sxs-lookup"><span data-stu-id="1c101-121">Low word</span></span>  | <span data-ttu-id="1c101-122">Hohe Bytereihenfolge</span><span class="sxs-lookup"><span data-stu-id="1c101-122">High-order byte</span></span> | <span data-ttu-id="1c101-123">Enthält das erste Byte derDATENÜBERTRAGUNG-Daten (falls erforderlich).</span><span class="sxs-lookup"><span data-stu-id="1c101-123">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="1c101-124">Byte mit niedriger Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1c101-124">Low-order byte</span></span>  | <span data-ttu-id="1c101-125">Enthält den STATUS VON.</span><span class="sxs-lookup"><span data-stu-id="1c101-125">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="1c101-126">Die beiden BYTES für DIE DATEN SIND optional, je nach STATUS-Byte DESINEs.</span><span class="sxs-lookup"><span data-stu-id="1c101-126">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c101-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c101-127">Return Value</span></span>

<span data-ttu-id="1c101-128">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1c101-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c101-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c101-129">Remarks</span></span>

<span data-ttu-id="1c101-130">Wenn Ihre Anwendung SCHNELLER ALS DIE DATEN verarbeiten kann, sollten Sie keinen Fensterrückrufmechanismus verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c101-130">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="1c101-131">Um die Geschwindigkeit zu maximieren, verwenden Sie eine Rückruffunktion und die [**MIM \_ MOREDATA-Nachricht**](mim-moredata.md) anstelle von MM \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="1c101-131">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="1c101-132">Eine Anwendung sollte nur eine minimale Verarbeitungsmenge von MM \_ MIM \_ MOREDATA-Nachrichten durchführen.</span><span class="sxs-lookup"><span data-stu-id="1c101-132">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="1c101-133">(Insbesondere sollten Anwendungen die [PostMessage-Funktion](/windows/win32/api/winuser/nf-winuser-postmessagea) während der Verarbeitung von MM \_ nicht aufrufen. MIM \_ MOREDATA.) Stattdessen sollte die Anwendung die Ereignisdaten in einen Puffer platzieren und dann zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1c101-133">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="1c101-134">Wenn eine Anwendung nach einer Reihe von MM MIM MOREDATA-Nachrichten eine [**MM \_ MIM \_ DATA-Nachricht**](mm-mim-data.md) empfängt, \_ hat sie eingehende \_ CAB-Ereignisse aufholt und kann zeitintensive Funktionen sicher aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1c101-134">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="1c101-135">DER STATUS von MELDUNGEN, die von einem PORTS empfangen werden, ist deaktiviert. jede Nachricht wird erweitert, um das STATUS-Byte ZU enthalten.</span><span class="sxs-lookup"><span data-stu-id="1c101-135">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="1c101-136">Diese Nachricht wird nicht gesendet, wenn eine vom SYSTEM exklusive MELDUNG empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="1c101-136">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="1c101-137">Für diese Nachricht ist kein Zeitstempel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1c101-137">No time stamp is available with this message.</span></span> <span data-ttu-id="1c101-138">Für Eingabedaten mit Zeitstempel müssen Sie die Nachrichten verwenden, die an Rückruffunktionen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c101-138">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c101-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1c101-139">Requirements</span></span>



| <span data-ttu-id="1c101-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c101-140">Requirement</span></span> | <span data-ttu-id="1c101-141">Wert</span><span class="sxs-lookup"><span data-stu-id="1c101-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c101-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c101-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1c101-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c101-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1c101-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c101-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1c101-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c101-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1c101-146">Header</span><span class="sxs-lookup"><span data-stu-id="1c101-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c101-147"><dt>Mmsystem.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1c101-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c101-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c101-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c101-149">Music Instrument Digital Interface (INSTRUMENTS)</span><span class="sxs-lookup"><span data-stu-id="1c101-149">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="1c101-150">FEHLERMELDUNGEN</span><span class="sxs-lookup"><span data-stu-id="1c101-150">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

