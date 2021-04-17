---
title: MIM_CLOSE Meldung (MMSYSTEM. h)
description: Die MIM \_ Close-Nachricht wird an eine Funktion der MIDI-Eingabe Rückruffunktion gesendet, wenn ein MIDI-Eingabegerät geschlossen wird.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- MIM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517408"
---
# <a name="mim_close-message"></a><span data-ttu-id="9d479-104">MIM \_ Close Message</span><span class="sxs-lookup"><span data-stu-id="9d479-104">MIM\_CLOSE message</span></span>

<span data-ttu-id="9d479-105">Die **MIM \_ Close** -Nachricht wird an eine Funktion der MIDI-Eingabe Rückruffunktion gesendet, wenn ein MIDI-Eingabegerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9d479-105">The **MIM\_CLOSE** message is sent to a MIDI input callback function when a MIDI input device is closed.</span></span>


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="9d479-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d479-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9d479-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9d479-108">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="9d479-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="9d479-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9d479-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9d479-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="9d479-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d479-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d479-111">Return Value</span></span>

<span data-ttu-id="9d479-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9d479-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d479-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d479-113">Remarks</span></span>

<span data-ttu-id="9d479-114">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9d479-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d479-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d479-115">Requirements</span></span>



| <span data-ttu-id="9d479-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d479-116">Requirement</span></span> | <span data-ttu-id="9d479-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9d479-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d479-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d479-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9d479-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d479-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9d479-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d479-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9d479-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d479-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d479-122">Header</span><span class="sxs-lookup"><span data-stu-id="9d479-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d479-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d479-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d479-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d479-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d479-125">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="9d479-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="9d479-126">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="9d479-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





