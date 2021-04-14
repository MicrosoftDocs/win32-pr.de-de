---
title: ICM_COMPRESS_END Meldung (VFW. h)
description: Die ICM \_ -Komprimierungs \_ Nachricht benachrichtigt einen Video Komprimierungs Treiber, um die Komprimierung zu beenden und die für die Komprimierung zugewiesenen Ressourcen freizugeben Sie können diese Nachricht explizit oder mithilfe des iccompressend-Makros senden.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476008"
---
# <a name="icm_compress_end-message"></a><span data-ttu-id="a07f5-105">ICM- \_ Komprimierungs \_ Nachricht beenden</span><span class="sxs-lookup"><span data-stu-id="a07f5-105">ICM\_COMPRESS\_END message</span></span>

<span data-ttu-id="a07f5-106">Die **ICM \_ - \_** Komprimierungs Nachricht benachrichtigt einen Video Komprimierungs Treiber, um die Komprimierung zu beenden und die für die Komprimierung zugewiesenen Ressourcen freizugeben</span><span class="sxs-lookup"><span data-stu-id="a07f5-106">The **ICM\_COMPRESS\_END** message notifies a video compression driver to end compression and free resources allocated for compression.</span></span> <span data-ttu-id="a07f5-107">Sie können diese Nachricht explizit oder mithilfe des [**iccompressend**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="a07f5-107">You can send this message explicitly or by using the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro.</span></span>


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="a07f5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a07f5-108">Return Value</span></span>

<span data-ttu-id="a07f5-109">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a07f5-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a07f5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a07f5-110">Remarks</span></span>

<span data-ttu-id="a07f5-111">VCM speichert die Einstellungen der letzten [**ICM- \_ Komprimierungs \_ Begin**](icm-compress-begin.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a07f5-111">VCM saves the settings of the most recent [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message.</span></span> <span data-ttu-id="a07f5-112">**ICM \_ Das Komprimieren von \_ Begin** und **ICM- \_ Komprimierung \_** wird nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="a07f5-112">**ICM\_COMPRESS\_BEGIN** and **ICM\_COMPRESS\_END** do not nest.</span></span> <span data-ttu-id="a07f5-113">Wenn der Treiber **ICM \_ Compress \_ Begin** empfängt, bevor die Komprimierung mit **ICM- \_ Komprimierung \_ beendet** wird, sollte die Komprimierung mit neuen Parametern neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a07f5-113">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a07f5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a07f5-114">Requirements</span></span>



| <span data-ttu-id="a07f5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a07f5-115">Requirement</span></span> | <span data-ttu-id="a07f5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a07f5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a07f5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a07f5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a07f5-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a07f5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a07f5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a07f5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a07f5-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a07f5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a07f5-121">Header</span><span class="sxs-lookup"><span data-stu-id="a07f5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a07f5-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a07f5-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a07f5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a07f5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a07f5-124">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="a07f5-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a07f5-125">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="a07f5-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





