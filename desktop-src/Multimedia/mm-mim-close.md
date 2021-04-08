---
title: MM_MIM_CLOSE Meldung (MMSYSTEM. h)
description: Die \_ Meldung zum \_ Schließen von mm MIM wird an ein Fenster gesendet, wenn ein MIDI-Eingabegerät geschlossen wird.
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- MM_MIM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ce511365b1faa49faefaf4ed25c5b8befb2288
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956772"
---
# <a name="mm_mim_close-message"></a><span data-ttu-id="075ed-104">Meldung zum Schließen von mm \_ MIM \_</span><span class="sxs-lookup"><span data-stu-id="075ed-104">MM\_MIM\_CLOSE message</span></span>

<span data-ttu-id="075ed-105">Die Meldung zum **\_ \_ Schließen von mm MIM** wird an ein Fenster gesendet, wenn ein MIDI-Eingabegerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="075ed-105">The **MM\_MIM\_CLOSE** message is sent to a window when a MIDI input device is closed.</span></span>


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="075ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="075ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075ed-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*</span><span class="sxs-lookup"><span data-stu-id="075ed-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="075ed-108">Handle für das geschlossene MIDI-Eingabegerät.</span><span class="sxs-lookup"><span data-stu-id="075ed-108">Handle to the MIDI input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="075ed-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="075ed-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="075ed-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="075ed-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075ed-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="075ed-111">Return Value</span></span>

<span data-ttu-id="075ed-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="075ed-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="075ed-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="075ed-113">Remarks</span></span>

<span data-ttu-id="075ed-114">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="075ed-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="075ed-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="075ed-115">Requirements</span></span>



| <span data-ttu-id="075ed-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="075ed-116">Requirement</span></span> | <span data-ttu-id="075ed-117">Wert</span><span class="sxs-lookup"><span data-stu-id="075ed-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="075ed-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="075ed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="075ed-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="075ed-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="075ed-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="075ed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="075ed-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="075ed-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="075ed-122">Header</span><span class="sxs-lookup"><span data-stu-id="075ed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="075ed-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="075ed-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="075ed-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="075ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075ed-125">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="075ed-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="075ed-126">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="075ed-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





