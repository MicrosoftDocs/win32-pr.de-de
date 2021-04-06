---
title: ICM_DECOMPRESS_END Meldung (VFW. h)
description: Die ICM \_ -Dekomprimierungs \_ Nachricht benachrichtigt einen Video-Dekomprimierungs Treiber, um die Dekomprimierung und die für die Dekomprimierung zugeordneten Ressourcen freizugeben. Sie können diese Nachricht explizit oder mithilfe des icdecompressend-Makros senden.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742969"
---
# <a name="icm_decompress_end-message"></a><span data-ttu-id="ac09c-105">ICM- \_ Dekomprimierungs \_ Nachricht beenden</span><span class="sxs-lookup"><span data-stu-id="ac09c-105">ICM\_DECOMPRESS\_END message</span></span>

<span data-ttu-id="ac09c-106">Die **ICM- \_ Dekomprimierungs \_** Nachricht benachrichtigt einen Video-Dekomprimierungs Treiber, um die Dekomprimierung und die für die Dekomprimierung zugeordneten Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ac09c-106">The **ICM\_DECOMPRESS\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="ac09c-107">Sie können diese Nachricht explizit oder mithilfe des [**icdecompressend**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="ac09c-107">You can send this message explicitly or by using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ac09c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac09c-108">Return Value</span></span>

<span data-ttu-id="ac09c-109">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ac09c-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac09c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac09c-110">Remarks</span></span>

<span data-ttu-id="ac09c-111">Der Treiber sollte alle Ressourcen freigeben, die für die [**ICM- \_ Dekomprimierungs- \_ Begin**](icm-decompress-begin.md) -Nachricht reserviert wurden.</span><span class="sxs-lookup"><span data-stu-id="ac09c-111">The driver should free any resources allocated for the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="ac09c-112">[**ICM \_ \_**](icm-decompress-begin.md) Das **\_ \_ Beenden** der BEGIN-und ICM-Debug wird nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="ac09c-112">[**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) and **ICM\_DECOMPRESS\_END** do not nest.</span></span> <span data-ttu-id="ac09c-113">Wenn der Treiber **ICM \_ Decompress \_** vor dem Beenden der Dekomprimierung mit **ICM \_ Decompress \_ Beenden** empfängt, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ac09c-113">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac09c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac09c-114">Requirements</span></span>



| <span data-ttu-id="ac09c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac09c-115">Requirement</span></span> | <span data-ttu-id="ac09c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ac09c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac09c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac09c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ac09c-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac09c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ac09c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac09c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ac09c-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac09c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ac09c-121">Header</span><span class="sxs-lookup"><span data-stu-id="ac09c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac09c-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac09c-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac09c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac09c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac09c-124">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="ac09c-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ac09c-125">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="ac09c-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





