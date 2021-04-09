---
title: MM_MIM_OPEN Meldung (MMSYSTEM. h)
description: Die \_ von mm MIM \_ geöffnete Nachricht wird an ein Fenster gesendet, wenn ein MIDI-Eingabegerät geöffnet wird.
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- MM_MIM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858628"
---
# <a name="mm_mim_open-message"></a><span data-ttu-id="8b5d1-104">Von mm \_ MIM \_ geöffnete Nachricht</span><span class="sxs-lookup"><span data-stu-id="8b5d1-104">MM\_MIM\_OPEN message</span></span>

<span data-ttu-id="8b5d1-105">Die von **mm \_ MIM \_ geöffnete** Nachricht wird an ein Fenster gesendet, wenn ein MIDI-Eingabegerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-105">The **MM\_MIM\_OPEN** message is sent to a window when a MIDI input device is opened.</span></span>


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="8b5d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b5d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5d1-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*</span><span class="sxs-lookup"><span data-stu-id="8b5d1-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="8b5d1-108">Handle für das geöffnete MIDI-Eingabegerät.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-108">Handle to the MIDI input device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="8b5d1-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="8b5d1-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8b5d1-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5d1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b5d1-111">Return Value</span></span>

<span data-ttu-id="8b5d1-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5d1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b5d1-113">Requirements</span></span>



| <span data-ttu-id="8b5d1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b5d1-114">Requirement</span></span> | <span data-ttu-id="8b5d1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8b5d1-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5d1-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b5d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8b5d1-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b5d1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8b5d1-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b5d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8b5d1-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b5d1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8b5d1-120">Header</span><span class="sxs-lookup"><span data-stu-id="8b5d1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b5d1-121"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b5d1-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b5d1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b5d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5d1-123">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="8b5d1-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="8b5d1-124">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8b5d1-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





