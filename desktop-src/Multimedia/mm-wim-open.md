---
title: MM_WIM_OPEN Meldung (MMSYSTEM. h)
description: '\_ \_ Wenn ein Waveform-Audioeingabegerät geöffnet wird, wird die Nachricht mm WIM Open an ein Fenster gesendet.'
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- MM_WIM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff028dcd9dc851d94699ef5cb75707429ba149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041007"
---
# <a name="mm_wim_open-message"></a><span data-ttu-id="f8c46-104">MM \_ WIM- \_ Nachricht öffnen</span><span class="sxs-lookup"><span data-stu-id="f8c46-104">MM\_WIM\_OPEN message</span></span>

<span data-ttu-id="f8c46-105">Wenn ein Waveform-Audioeingabegerät geöffnet wird, wird die Nachricht **mm \_ WIM \_ Open** an ein Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="f8c46-105">The **MM\_WIM\_OPEN** message is sent to a window when a waveform-audio input device is opened.</span></span>


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="f8c46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8c46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c46-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hinputdev*</span><span class="sxs-lookup"><span data-stu-id="f8c46-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="f8c46-108">Handle für das Gerät, das geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f8c46-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="f8c46-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="f8c46-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f8c46-110">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f8c46-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c46-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8c46-111">Return Value</span></span>

<span data-ttu-id="f8c46-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f8c46-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c46-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8c46-113">Requirements</span></span>



| <span data-ttu-id="f8c46-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8c46-114">Requirement</span></span> | <span data-ttu-id="f8c46-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f8c46-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c46-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8c46-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c46-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8c46-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8c46-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8c46-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c46-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8c46-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8c46-120">Header</span><span class="sxs-lookup"><span data-stu-id="f8c46-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8c46-121"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8c46-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8c46-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8c46-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c46-123">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="f8c46-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="f8c46-124">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="f8c46-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





