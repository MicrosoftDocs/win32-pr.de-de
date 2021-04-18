---
title: WOM_CLOSE Meldung (MMSYSTEM. h)
description: Die WOM \_ Close-Nachricht wird an eine Funktion für die Funktion "Waveform-Audioausgabe" gesendet, wenn ein Waveform-Audioausgabegerät geschlossen wird. Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- WOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340780"
---
# <a name="wom_close-message"></a><span data-ttu-id="89b34-105">WOM- \_ Schließen-Meldung</span><span class="sxs-lookup"><span data-stu-id="89b34-105">WOM\_CLOSE message</span></span>

<span data-ttu-id="89b34-106">Die **WOM \_ Close** -Nachricht wird an eine Funktion für die Funktion "Waveform-Audioausgabe" gesendet, wenn ein Waveform-Audioausgabegerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="89b34-106">The **WOM\_CLOSE** message is sent to a waveform-audio output callback function when a waveform-audio output device is closed.</span></span> <span data-ttu-id="89b34-107">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="89b34-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="89b34-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89b34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b34-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="89b34-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="89b34-110">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="89b34-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="89b34-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="89b34-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="89b34-112">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="89b34-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89b34-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89b34-113">Return Value</span></span>

<span data-ttu-id="89b34-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="89b34-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b34-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89b34-115">Requirements</span></span>



| <span data-ttu-id="89b34-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89b34-116">Requirement</span></span> | <span data-ttu-id="89b34-117">Wert</span><span class="sxs-lookup"><span data-stu-id="89b34-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b34-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89b34-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89b34-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89b34-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="89b34-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89b34-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89b34-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89b34-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="89b34-122">Header</span><span class="sxs-lookup"><span data-stu-id="89b34-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89b34-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89b34-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b34-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89b34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b34-125">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="89b34-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="89b34-126">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="89b34-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





