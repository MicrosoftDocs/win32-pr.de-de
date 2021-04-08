---
title: ICM_GETBUFFERSWANTED Meldung (VFW. h)
description: Die ICM \_ getbufferswanted-Nachricht fragt einen Treiber nach der Anzahl der zuzuordnenden Puffer ab. Sie können diese Nachricht explizit oder mit dem icgetbufferswanted-Makro senden.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949539"
---
# <a name="icm_getbufferswanted-message"></a><span data-ttu-id="654d5-105">ICM \_ getbufferswanted-Nachricht</span><span class="sxs-lookup"><span data-stu-id="654d5-105">ICM\_GETBUFFERSWANTED message</span></span>

<span data-ttu-id="654d5-106">Die **ICM \_ getbufferswanted** -Nachricht fragt einen Treiber nach der Anzahl der zuzuordnenden Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="654d5-106">The **ICM\_GETBUFFERSWANTED** message queries a driver for the number of buffers to allocate.</span></span> <span data-ttu-id="654d5-107">Sie können diese Nachricht explizit oder mit dem [**icgetbufferswanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="654d5-107">You can send this message explicitly or by using the [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) macro.</span></span>


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="654d5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="654d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="654d5-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwbuffers*</span><span class="sxs-lookup"><span data-stu-id="654d5-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span></span>
</dt> <dd>

<span data-ttu-id="654d5-110">Adresse, die die Anzahl der Abtastungen enthält, die der Treiber zum effizienten Rendering der Daten benötigt.</span><span class="sxs-lookup"><span data-stu-id="654d5-110">Address to contain the number of samples the driver needs to efficiently render the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="654d5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="654d5-111">Return Value</span></span>

<span data-ttu-id="654d5-112">Gibt bei erfolgreicher Ausführung von ICERR OK zurück, \_ andernfalls wird ICERR \_ nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="654d5-112">Returns ICERR\_OK if successful or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="654d5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="654d5-113">Remarks</span></span>

<span data-ttu-id="654d5-114">Diese Meldung wird von Treibern verwendet, die Hardware zum Rendering von Daten verwenden und eine minimale Zeitverzögerung sicherstellen möchten, die durch warten auf das Eintreffen von Puffern verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="654d5-114">This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive.</span></span> <span data-ttu-id="654d5-115">Wenn ein Treiber z. b. ein Video Dekomprimierungs Board steuert, das 10 Videorahmen aufnehmen kann, kann es für diese Nachricht 10 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="654d5-115">For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message.</span></span> <span data-ttu-id="654d5-116">Dadurch werden Anwendungen angewiesen, 10 Frames vor dem Frame zu behalten, den Sie zurzeit benötigt.</span><span class="sxs-lookup"><span data-stu-id="654d5-116">This instructs applications to try to stay 10 frames ahead of the frame it currently needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="654d5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="654d5-117">Requirements</span></span>



| <span data-ttu-id="654d5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="654d5-118">Requirement</span></span> | <span data-ttu-id="654d5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="654d5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="654d5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="654d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="654d5-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="654d5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="654d5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="654d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="654d5-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="654d5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="654d5-124">Header</span><span class="sxs-lookup"><span data-stu-id="654d5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="654d5-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="654d5-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654d5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="654d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654d5-127">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="654d5-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="654d5-128">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="654d5-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





