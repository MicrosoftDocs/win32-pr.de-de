---
title: MM_WIM_CLOSE Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm WIM \_ Close wird an ein Fenster gesendet, wenn ein Waveform-Audioeingabegerät geschlossen wird. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- MM_WIM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040072"
---
# <a name="mm_wim_close-message"></a><span data-ttu-id="8c6fe-105">MM- \_ WIM- \_ Schließen-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8c6fe-105">MM\_WIM\_CLOSE message</span></span>

<span data-ttu-id="8c6fe-106">Die Meldung **mm \_ WIM \_ Close** wird an ein Fenster gesendet, wenn ein Waveform-Audioeingabegerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-106">The **MM\_WIM\_CLOSE** message is sent to a window when a waveform-audio input device is closed.</span></span> <span data-ttu-id="8c6fe-107">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="8c6fe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c6fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c6fe-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hinputdev*</span><span class="sxs-lookup"><span data-stu-id="8c6fe-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="8c6fe-110">Handle für das gesperrte Waveform-Audioeingabegerät.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-110">Handle to the waveform-audio input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="8c6fe-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="8c6fe-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8c6fe-112">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c6fe-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c6fe-113">Return Value</span></span>

<span data-ttu-id="8c6fe-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8c6fe-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6fe-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c6fe-115">Requirements</span></span>



| <span data-ttu-id="8c6fe-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c6fe-116">Requirement</span></span> | <span data-ttu-id="8c6fe-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8c6fe-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6fe-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c6fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6fe-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c6fe-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c6fe-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c6fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6fe-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c6fe-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c6fe-122">Header</span><span class="sxs-lookup"><span data-stu-id="8c6fe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c6fe-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c6fe-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c6fe-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c6fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6fe-125">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="8c6fe-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="8c6fe-126">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="8c6fe-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





