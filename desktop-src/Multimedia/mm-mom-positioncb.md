---
title: MM_MOM_POSITIONCB Meldung (MMSYSTEM. h)
description: Die "mm \_ MOM \_ positioncb"-Nachricht wird an ein Fenster gesendet, wenn ein mevt \_ F- \_ Rückruf Ereignis im MIDI-Ausgabestream erreicht wird.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949481"
---
# <a name="mm_mom_positioncb-message"></a><span data-ttu-id="ac994-104">MM \_ MOM \_ positioncb-Meldung</span><span class="sxs-lookup"><span data-stu-id="ac994-104">MM\_MOM\_POSITIONCB message</span></span>

<span data-ttu-id="ac994-105">Die " **mm \_ MOM \_ positioncb** "-Nachricht wird an ein Fenster gesendet, wenn ein mevt \_ F- \_ Rückruf Ereignis im MIDI-Ausgabestream erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="ac994-105">The **MM\_MOM\_POSITIONCB** message is sent to a window when an MEVT\_F\_CALLBACK event is reached in the MIDI output stream.</span></span>


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="ac994-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac994-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac994-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*</span><span class="sxs-lookup"><span data-stu-id="ac994-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="ac994-108">Ein Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die das Ereignis identifiziert, das den Rückruf verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="ac994-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the event that caused the callback.</span></span> <span data-ttu-id="ac994-109">Der **dwOffset** -Member gibt den Offset des Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="ac994-109">The **dwOffset** member gives the offset of the event.</span></span>

</dd> <dt>

<span data-ttu-id="ac994-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="ac994-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ac994-111">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="ac994-111">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac994-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac994-112">Return Value</span></span>

<span data-ttu-id="ac994-113">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ac994-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac994-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac994-114">Remarks</span></span>

<span data-ttu-id="ac994-115">Die Wiedergabe des Streampuffers wird auch dann fortgesetzt, wenn die Rückruffunktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac994-115">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="ac994-116">Alle Ereignisse nach dem mevt \_ F \_ -Rückruf Ereignis im Puffer werden zeitlich geplant und gesendet, unabhängig davon, wie viel Zeit in der Rückruffunktion aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac994-116">Any events after the MEVT\_F\_CALLBACK event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="ac994-117">Wenn Positions Rückrufe schneller generiert werden, als Sie von Ihrer Anwendung verarbeitet werden können, kann der **dwOffset** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur auf ein Ereignis verweisen, das Ihre Anwendung noch nicht verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="ac994-117">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac994-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac994-118">Requirements</span></span>



| <span data-ttu-id="ac994-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac994-119">Requirement</span></span> | <span data-ttu-id="ac994-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ac994-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac994-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac994-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac994-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac994-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac994-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac994-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ac994-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac994-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac994-125">Header</span><span class="sxs-lookup"><span data-stu-id="ac994-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac994-126"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac994-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac994-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac994-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac994-128">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="ac994-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

