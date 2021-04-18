---
title: MM_MIM_LONGERROR Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm MIM \_ longerror wird an ein Fenster gesendet, wenn eine ungültige oder unvollständige, vom System exklusive System exklusive Nachricht empfangen wird.
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- MM_MIM_LONGERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344700"
---
# <a name="mm_mim_longerror-message"></a><span data-ttu-id="f1500-104">MM \_ MIM \_ longerror-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f1500-104">MM\_MIM\_LONGERROR message</span></span>

<span data-ttu-id="f1500-105">Die Meldung **mm \_ MIM \_ longerror** wird an ein Fenster gesendet, wenn eine ungültige oder unvollständige, vom System exklusive System exklusive Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f1500-105">The **MM\_MIM\_LONGERROR** message is sent to a window when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="f1500-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1500-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1500-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*</span><span class="sxs-lookup"><span data-stu-id="f1500-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="f1500-108">Handle für das MIDI-Eingabegerät, das die ungültige Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="f1500-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="f1500-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*</span><span class="sxs-lookup"><span data-stu-id="f1500-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="f1500-110">Ein Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Puffer identifiziert, der die ungültige Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="f1500-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1500-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1500-111">Return Value</span></span>

<span data-ttu-id="f1500-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f1500-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1500-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1500-113">Remarks</span></span>

<span data-ttu-id="f1500-114">Der zurückgegebene Puffer ist möglicherweise nicht voll.</span><span class="sxs-lookup"><span data-stu-id="f1500-114">The returned buffer might not be full.</span></span> <span data-ttu-id="f1500-115">Um die Anzahl der Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden, verwenden Sie den **dwbyteslock** -Member der von *lpmidihdr* angegebenen [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f1500-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1500-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1500-116">Requirements</span></span>



| <span data-ttu-id="f1500-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1500-117">Requirement</span></span> | <span data-ttu-id="f1500-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f1500-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1500-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1500-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1500-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1500-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1500-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1500-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1500-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1500-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1500-123">Header</span><span class="sxs-lookup"><span data-stu-id="f1500-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1500-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1500-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1500-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1500-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1500-126">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="f1500-126">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="f1500-127">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f1500-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

