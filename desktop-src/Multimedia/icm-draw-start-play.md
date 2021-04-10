---
title: ICM_DRAW_START_PLAY Meldung (VFW. h)
description: Die ICM \_ Draw \_ -Wiedergabe Meldung "Start" \_ stellt die Start-und Endzeit eines Wiedergabe Vorgangs für einen renderingtreiber bereit. Sie können diese Nachricht explizit oder mithilfe des icdrawstartplay-Makros senden.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103450"
---
# <a name="icm_draw_start_play-message"></a><span data-ttu-id="e7213-105">ICM \_ Draw \_ - \_ Wiedergabe Nachricht starten</span><span class="sxs-lookup"><span data-stu-id="e7213-105">ICM\_DRAW\_START\_PLAY message</span></span>

<span data-ttu-id="e7213-106">Die **ICM \_ Draw \_ \_** -Wiedergabe Meldung "Start" stellt die Start-und Endzeit eines Wiedergabe Vorgangs für einen renderingtreiber bereit.</span><span class="sxs-lookup"><span data-stu-id="e7213-106">The **ICM\_DRAW\_START\_PLAY** message provides the start and end times of a play operation to a rendering driver.</span></span> <span data-ttu-id="e7213-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawstartplay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e7213-107">You can send this message explicitly or by using the [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) macro.</span></span>


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a><span data-ttu-id="e7213-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7213-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7213-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lfrom*</span><span class="sxs-lookup"><span data-stu-id="e7213-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span></span>
</dt> <dd>

<span data-ttu-id="e7213-110">Startzeit.</span><span class="sxs-lookup"><span data-stu-id="e7213-110">Start time.</span></span>

</dd> <dt>

<span data-ttu-id="e7213-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span><span class="sxs-lookup"><span data-stu-id="e7213-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span></span>
</dt> <dd>

<span data-ttu-id="e7213-112">Endzeit.</span><span class="sxs-lookup"><span data-stu-id="e7213-112">End time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7213-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7213-113">Return Value</span></span>

<span data-ttu-id="e7213-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e7213-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7213-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7213-115">Remarks</span></span>

<span data-ttu-id="e7213-116">Diese Nachricht geht vor allen Frame Daten vor, die an den renderingtreiber gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7213-116">This message precedes any frame data sent to the rendering driver.</span></span>

<span data-ttu-id="e7213-117">Einheiten für *lfrom* und *LTO* werden mit der [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) -Meldung angegeben.</span><span class="sxs-lookup"><span data-stu-id="e7213-117">Units for *lFrom* and *lTo* are specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span> <span data-ttu-id="e7213-118">Bei Videodaten ist dies normalerweise eine Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="e7213-118">For video data this is normally a frame number.</span></span> <span data-ttu-id="e7213-119">Weitere Informationen zur Wiedergabe Rate finden Sie unter den **dwtrate** -und **dwscale** -Membern der [**icdrawbegin**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e7213-119">For more information about the playback rate, see the **dwRate** and **dwScale** members of the [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure.</span></span>

<span data-ttu-id="e7213-120">Wenn die Endzeit kleiner als die Startzeit ist, wird die Wiedergabe Richtung umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="e7213-120">If the end time is less than the start time, the playback direction is reversed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7213-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7213-121">Requirements</span></span>



| <span data-ttu-id="e7213-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7213-122">Requirement</span></span> | <span data-ttu-id="e7213-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e7213-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e7213-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7213-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e7213-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7213-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e7213-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7213-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e7213-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7213-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e7213-128">Header</span><span class="sxs-lookup"><span data-stu-id="e7213-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7213-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7213-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7213-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7213-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7213-131">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="e7213-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e7213-132">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="e7213-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





