---
title: MOM_POSITIONCB Meldung (MMSYSTEM. h)
description: Die MOM- \_ Positions Meldung wird gesendet, wenn ein mevt \_ F- \_ Rückruf Ereignis im MIDI-Ausgabestream erreicht wird.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743353"
---
# <a name="mom_positioncb-message"></a><span data-ttu-id="0ae79-104">MOM- \_ positioncb-Meldung</span><span class="sxs-lookup"><span data-stu-id="0ae79-104">MOM\_POSITIONCB message</span></span>

<span data-ttu-id="0ae79-105">Die **MOM- \_ Positions** Meldung wird gesendet, wenn ein **mevt \_ F- \_ Rückruf** Ereignis im MIDI-Ausgabestream erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="0ae79-105">The **MOM\_POSITION** message is sent when an **MEVT\_F\_CALLBACK** event is reached in the MIDI output stream.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ae79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ae79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ae79-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0ae79-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0ae79-108">Ein Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Eingabepuffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0ae79-108">A pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0ae79-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0ae79-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0ae79-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ae79-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ae79-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ae79-111">Return Value</span></span>

<span data-ttu-id="0ae79-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0ae79-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ae79-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ae79-113">Remarks</span></span>

<span data-ttu-id="0ae79-114">Die Wiedergabe des Streampuffers wird auch dann fortgesetzt, wenn die Rückruffunktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ae79-114">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="0ae79-115">Alle Ereignisse nach dem **mevt \_ F- \_ Rückruf** Ereignis im Puffer werden zeitlich geplant und gesendet, unabhängig davon, wie viel Zeit in der Rückruffunktion aufgewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ae79-115">Any events after the **MEVT\_F\_CALLBACK** event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="0ae79-116">Wenn Positions Rückrufe schneller generiert werden, als Sie von Ihrer Anwendung verarbeitet werden können, kann der **dwOffset** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur auf ein Ereignis verweisen, das Ihre Anwendung noch nicht verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="0ae79-116">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ae79-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ae79-117">Requirements</span></span>



| <span data-ttu-id="0ae79-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ae79-118">Requirement</span></span> | <span data-ttu-id="0ae79-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0ae79-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae79-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ae79-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0ae79-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ae79-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0ae79-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ae79-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0ae79-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ae79-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0ae79-124">Header</span><span class="sxs-lookup"><span data-stu-id="0ae79-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ae79-125"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ae79-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ae79-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ae79-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ae79-127">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0ae79-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

