---
title: WOM_OPEN Meldung (MMSYSTEM. h)
description: Die WOM- \_ Meldung wird geöffnet, wenn ein Waveform-Audioausgabegerät geöffnet wird.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- WOM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfca721019b28a5bf039e8c56c75892d85bd5e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102835"
---
# <a name="wom_open-message"></a><span data-ttu-id="85285-104">WOM \_ geöffnete Nachricht</span><span class="sxs-lookup"><span data-stu-id="85285-104">WOM\_OPEN message</span></span>

<span data-ttu-id="85285-105">Die **WOM \_** -Meldung wird geöffnet, wenn ein Waveform-Audioausgabegerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="85285-105">The **WOM\_OPEN** message is sent to a waveform-audio output callback function when a waveform-audio output device is opened.</span></span>


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="85285-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85285-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85285-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="85285-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="85285-108">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="85285-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="85285-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="85285-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="85285-110">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="85285-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85285-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85285-111">Return Value</span></span>

<span data-ttu-id="85285-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="85285-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="85285-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85285-113">Requirements</span></span>



| <span data-ttu-id="85285-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85285-114">Requirement</span></span> | <span data-ttu-id="85285-115">Wert</span><span class="sxs-lookup"><span data-stu-id="85285-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85285-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85285-116">Minimum supported client</span></span><br/> | <span data-ttu-id="85285-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85285-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="85285-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85285-118">Minimum supported server</span></span><br/> | <span data-ttu-id="85285-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85285-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="85285-120">Header</span><span class="sxs-lookup"><span data-stu-id="85285-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="85285-121"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85285-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85285-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85285-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85285-123">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="85285-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="85285-124">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="85285-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





