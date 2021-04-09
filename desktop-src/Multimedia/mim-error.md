---
title: MIM_ERROR Meldung (MMSYSTEM. h)
description: Die MIM- \_ Fehlermeldung wird an eine MIDI-Eingabe Rückruffunktion gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird.
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- MIM_ERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103043"
---
# <a name="mim_error-message"></a><span data-ttu-id="e889e-104">MIM- \_ Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="e889e-104">MIM\_ERROR message</span></span>

<span data-ttu-id="e889e-105">Die **MIM- \_ Fehler** Meldung wird an eine MIDI-Eingabe Rückruffunktion gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="e889e-105">The **MIM\_ERROR** message is sent to a MIDI input callback function when an invalid MIDI message is received.</span></span>


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="e889e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e889e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e889e-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwmidimessage*</span><span class="sxs-lookup"><span data-stu-id="e889e-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="e889e-108">Es wurde eine ungültige MIDI-Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="e889e-108">Invalid MIDI message that was received.</span></span> <span data-ttu-id="e889e-109">Die Nachricht wird in einem Double Word-Wert mit dem ersten Byte der Nachricht im nieder wertigen Byte verpackt.</span><span class="sxs-lookup"><span data-stu-id="e889e-109">The message is packed into a doubleword value with the first byte of the message in the low-order byte.</span></span>

</dd> <dt>

<span data-ttu-id="e889e-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwtimestamp*</span><span class="sxs-lookup"><span data-stu-id="e889e-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="e889e-111">Der Zeitpunkt, zu dem die Nachricht vom Eingabegeräte Treiber empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="e889e-111">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="e889e-112">Der Zeitstempel wird in Millisekunden angegeben, beginnend bei Null, als die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e889e-112">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e889e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e889e-113">Return Value</span></span>

<span data-ttu-id="e889e-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e889e-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e889e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e889e-115">Requirements</span></span>



| <span data-ttu-id="e889e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e889e-116">Requirement</span></span> | <span data-ttu-id="e889e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e889e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e889e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e889e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e889e-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e889e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e889e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e889e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e889e-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e889e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e889e-122">Header</span><span class="sxs-lookup"><span data-stu-id="e889e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e889e-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e889e-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e889e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e889e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e889e-125">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="e889e-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="e889e-126">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e889e-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

