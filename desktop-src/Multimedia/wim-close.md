---
title: WIM_CLOSE Meldung (MMSYSTEM. h)
description: Die WIM \_ -Schließen-Nachricht wird an die angegebene Waveform-audioeingaberückruf-Funktion gesendet, wenn ein Waveform-Audioeingabegerät geschlossen wird. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- WIM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6028ac6c45aa013138aab227e79d8d210ad70bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478717"
---
# <a name="wim_close-message"></a><span data-ttu-id="74761-105">Wim- \_ Schließen-Nachricht</span><span class="sxs-lookup"><span data-stu-id="74761-105">WIM\_CLOSE message</span></span>

<span data-ttu-id="74761-106">Die **WIM- \_ Schließen** -Nachricht wird an die angegebene Waveform-audioeingaberückruf-Funktion gesendet, wenn ein Waveform-Audioeingabegerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="74761-106">The **WIM\_CLOSE** message is sent to the given waveform-audio input callback function when a waveform-audio input device is closed.</span></span> <span data-ttu-id="74761-107">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="74761-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="74761-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74761-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74761-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="74761-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="74761-110">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="74761-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="74761-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="74761-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="74761-112">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="74761-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74761-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74761-113">Return Value</span></span>

<span data-ttu-id="74761-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="74761-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="74761-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74761-115">Requirements</span></span>



| <span data-ttu-id="74761-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74761-116">Requirement</span></span> | <span data-ttu-id="74761-117">Wert</span><span class="sxs-lookup"><span data-stu-id="74761-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74761-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74761-118">Minimum supported client</span></span><br/> | <span data-ttu-id="74761-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74761-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="74761-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74761-120">Minimum supported server</span></span><br/> | <span data-ttu-id="74761-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74761-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74761-122">Header</span><span class="sxs-lookup"><span data-stu-id="74761-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="74761-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74761-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74761-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74761-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74761-125">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="74761-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="74761-126">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="74761-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





