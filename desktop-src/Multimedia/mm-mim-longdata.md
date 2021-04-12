---
title: MM_MIM_LONGDATA Meldung (MMSYSTEM. h)
description: Die mm \_ MIM \_ longdata-Nachricht wird an ein Fenster gesendet, wenn entweder eine vollständige, vom System exklusive System exklusive Nachricht empfangen wird oder wenn ein Puffer mit System exklusiven Daten aufgefüllt wurde.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105903"
---
# <a name="mm_mim_longdata-message"></a><span data-ttu-id="935ab-104">MM \_ MIM \_ longdata-Nachricht</span><span class="sxs-lookup"><span data-stu-id="935ab-104">MM\_MIM\_LONGDATA message</span></span>

<span data-ttu-id="935ab-105">Die **mm \_ MIM \_ longdata** -Nachricht wird an ein Fenster gesendet, wenn entweder eine vollständige, vom System exklusive System exklusive Nachricht empfangen wird oder wenn ein Puffer mit System exklusiven Daten aufgefüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="935ab-105">The **MM\_MIM\_LONGDATA** message is sent to a window when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="935ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="935ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="935ab-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*</span><span class="sxs-lookup"><span data-stu-id="935ab-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="935ab-108">Handle für das MIDI-Eingabegerät, das die Daten empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="935ab-108">Handle to the MIDI input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="935ab-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*</span><span class="sxs-lookup"><span data-stu-id="935ab-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="935ab-110">Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Puffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="935ab-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="935ab-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="935ab-111">Return Value</span></span>

<span data-ttu-id="935ab-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="935ab-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="935ab-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="935ab-113">Remarks</span></span>

<span data-ttu-id="935ab-114">Der zurückgegebene Puffer ist möglicherweise nicht voll.</span><span class="sxs-lookup"><span data-stu-id="935ab-114">The returned buffer might not be full.</span></span> <span data-ttu-id="935ab-115">Um die Anzahl von Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden, verwenden Sie den **dwbyteslock** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, auf die von *lpmidihdr* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="935ab-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure pointed to by *lpMidiHdr*.</span></span>

<span data-ttu-id="935ab-116">Mit dieser Meldung ist kein Zeitstempel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="935ab-116">No time stamp is available with this message.</span></span> <span data-ttu-id="935ab-117">Für Zeitstempel-Eingabedaten müssen Sie die Nachrichten verwenden, die an Rückruf Funktionen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="935ab-117">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="935ab-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="935ab-118">Requirements</span></span>



| <span data-ttu-id="935ab-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="935ab-119">Requirement</span></span> | <span data-ttu-id="935ab-120">Wert</span><span class="sxs-lookup"><span data-stu-id="935ab-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935ab-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="935ab-121">Minimum supported client</span></span><br/> | <span data-ttu-id="935ab-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="935ab-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="935ab-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="935ab-123">Minimum supported server</span></span><br/> | <span data-ttu-id="935ab-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="935ab-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="935ab-125">Header</span><span class="sxs-lookup"><span data-stu-id="935ab-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="935ab-126"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="935ab-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935ab-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="935ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935ab-128">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="935ab-128">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="935ab-129">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="935ab-129">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

