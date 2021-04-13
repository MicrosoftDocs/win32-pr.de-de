---
title: MIM_LONGERROR Meldung (MMSYSTEM. h)
description: Die MIM \_ longerror-Nachricht wird an eine Eingabe Rückruffunktion von MIDI gesendet, wenn eine ungültige oder unvollständige, vom System exklusive System exklusive Nachricht empfangen wird.
ms.assetid: 7e3b0716-33c4-449c-a200-e5ba72428dc1
keywords:
- MIM_LONGERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631c4fdcd31eef01d691aea80100427d116ae7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475510"
---
# <a name="mim_longerror-message"></a><span data-ttu-id="7f05a-104">MIM \_ longerror-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7f05a-104">MIM\_LONGERROR message</span></span>

<span data-ttu-id="7f05a-105">Die **MIM \_ longerror** -Nachricht wird an eine Eingabe Rückruffunktion von MIDI gesendet, wenn eine ungültige oder unvollständige, vom System exklusive System exklusive Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="7f05a-105">The **MIM\_LONGERROR** message is sent to a MIDI input callback function when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MIM_LONGERROR 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="7f05a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f05a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f05a-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*</span><span class="sxs-lookup"><span data-stu-id="7f05a-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="7f05a-108">Ein Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Puffer identifiziert, der die ungültige Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="7f05a-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="7f05a-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwtimestamp*</span><span class="sxs-lookup"><span data-stu-id="7f05a-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="7f05a-110">Zeitpunkt, zu dem die Daten vom Eingabegeräte Treiber empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="7f05a-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="7f05a-111">Der Zeitstempel wird in Millisekunden angegeben, beginnend bei Null, als die [**midiinstart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) -Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7f05a-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f05a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f05a-112">Return Value</span></span>

<span data-ttu-id="7f05a-113">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7f05a-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f05a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f05a-114">Remarks</span></span>

<span data-ttu-id="7f05a-115">Der zurückgegebene Puffer ist möglicherweise nicht voll.</span><span class="sxs-lookup"><span data-stu-id="7f05a-115">The returned buffer might not be full.</span></span> <span data-ttu-id="7f05a-116">Um die Anzahl der Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden, verwenden Sie den **dwbyteslock** -Member der von *lpmidihdr* angegebenen [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7f05a-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f05a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f05a-117">Requirements</span></span>



| <span data-ttu-id="7f05a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f05a-118">Requirement</span></span> | <span data-ttu-id="7f05a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7f05a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f05a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f05a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f05a-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f05a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7f05a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f05a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f05a-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f05a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7f05a-124">Header</span><span class="sxs-lookup"><span data-stu-id="7f05a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f05a-125"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f05a-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f05a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f05a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f05a-127">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="7f05a-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="7f05a-128">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="7f05a-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

