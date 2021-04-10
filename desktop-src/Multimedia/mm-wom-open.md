---
title: MM_WOM_OPEN Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm WOM \_ Öffnen wird an ein Fenster gesendet, wenn das angegebene Waveform-Audioausgabegerät geöffnet wird.
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783910389f2b9be9193c8f7bb0722f70261f5fce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106520"
---
# <a name="mm_wom_open-message"></a><span data-ttu-id="0f955-104">Meldung zum Öffnen von mm \_ WOM \_</span><span class="sxs-lookup"><span data-stu-id="0f955-104">MM\_WOM\_OPEN message</span></span>

<span data-ttu-id="0f955-105">Die Meldung **mm \_ WOM \_ Öffnen** wird an ein Fenster gesendet, wenn das angegebene Waveform-Audioausgabegerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="0f955-105">The **MM\_WOM\_OPEN** message is sent to a window when the given waveform-audio output device is opened.</span></span>


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="0f955-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f955-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f955-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*houtputdev*</span><span class="sxs-lookup"><span data-stu-id="0f955-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="0f955-108">Handle für das Gerät, das geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="0f955-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="0f955-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="0f955-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0f955-110">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="0f955-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f955-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f955-111">Return Value</span></span>

<span data-ttu-id="0f955-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0f955-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f955-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f955-113">Requirements</span></span>



| <span data-ttu-id="0f955-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f955-114">Requirement</span></span> | <span data-ttu-id="0f955-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0f955-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f955-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f955-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0f955-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f955-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0f955-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f955-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0f955-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f955-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0f955-120">Header</span><span class="sxs-lookup"><span data-stu-id="0f955-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f955-121"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f955-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f955-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f955-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f955-123">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="0f955-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="0f955-124">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="0f955-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





