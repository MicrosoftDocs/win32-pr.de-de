---
title: MIM_OPEN Meldung (MMSYSTEM. h)
description: Die MIM- \_ Open-Nachricht wird an eine Funktion der MIDI-Eingabe Rückruffunktion gesendet, wenn ein MIDI-Eingabegerät geöffnet wird.
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- MIM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49fcfd05ef7702fbc7bf3108365e49660071ae9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391572"
---
# <a name="mim_open-message"></a><span data-ttu-id="450e4-104">Meldung zum Öffnen von MIM \_</span><span class="sxs-lookup"><span data-stu-id="450e4-104">MIM\_OPEN message</span></span>

<span data-ttu-id="450e4-105">Die **MIM- \_ Open** -Nachricht wird an eine Funktion der MIDI-Eingabe Rückruffunktion gesendet, wenn ein MIDI-Eingabegerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="450e4-105">The **MIM\_OPEN** message is sent to a MIDI input callback function when a MIDI input device is opened.</span></span>


```C++
MIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="450e4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="450e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="450e4-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="450e4-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="450e4-108">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="450e4-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="450e4-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="450e4-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="450e4-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="450e4-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="450e4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="450e4-111">Return Value</span></span>

<span data-ttu-id="450e4-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="450e4-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="450e4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="450e4-113">Requirements</span></span>



| <span data-ttu-id="450e4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="450e4-114">Requirement</span></span> | <span data-ttu-id="450e4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="450e4-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="450e4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="450e4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="450e4-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="450e4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="450e4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="450e4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="450e4-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="450e4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="450e4-120">Header</span><span class="sxs-lookup"><span data-stu-id="450e4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="450e4-121"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="450e4-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="450e4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="450e4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="450e4-123">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="450e4-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="450e4-124">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="450e4-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





