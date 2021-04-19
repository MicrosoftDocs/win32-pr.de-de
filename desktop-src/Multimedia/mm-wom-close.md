---
title: MM_WOM_CLOSE Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm WOM \_ Close wird an ein Fenster gesendet, wenn ein Waveform-Audioausgabegerät geschlossen wird. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- MM_WOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343070"
---
# <a name="mm_wom_close-message"></a><span data-ttu-id="d8a17-105">Meldung zum Schließen von mm \_ WOM \_</span><span class="sxs-lookup"><span data-stu-id="d8a17-105">MM\_WOM\_CLOSE message</span></span>

<span data-ttu-id="d8a17-106">Die Meldung **mm \_ WOM \_ Close** wird an ein Fenster gesendet, wenn ein Waveform-Audioausgabegerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d8a17-106">The **MM\_WOM\_CLOSE** message is sent to a window when a waveform-audio output device is closed.</span></span> <span data-ttu-id="d8a17-107">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d8a17-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="d8a17-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8a17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8a17-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*houtputdev*</span><span class="sxs-lookup"><span data-stu-id="d8a17-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="d8a17-110">Handle für das Gerät, das geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d8a17-110">Handle to the device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="d8a17-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="d8a17-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d8a17-112">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d8a17-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8a17-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8a17-113">Return Value</span></span>

<span data-ttu-id="d8a17-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d8a17-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8a17-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8a17-115">Requirements</span></span>



| <span data-ttu-id="d8a17-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8a17-116">Requirement</span></span> | <span data-ttu-id="d8a17-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d8a17-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a17-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8a17-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d8a17-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8a17-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8a17-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8a17-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d8a17-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8a17-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8a17-122">Header</span><span class="sxs-lookup"><span data-stu-id="d8a17-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8a17-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8a17-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8a17-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8a17-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a17-125">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="d8a17-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="d8a17-126">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="d8a17-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





