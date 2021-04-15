---
title: ICM_DRAW_START Meldung (VFW. h)
description: Die ICM \_ Draw- \_ Start Meldung benachrichtigt einen renderingtreiber, seine interne Uhr für die zeitliche Steuerung von Zeichnungs Frames zu starten. Sie können diese Nachricht explizit oder mithilfe des icdrawstart-Makros senden.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391824"
---
# <a name="icm_draw_start-message"></a><span data-ttu-id="0497b-105">ICM- \_ Zeichnen- \_ Start Meldung</span><span class="sxs-lookup"><span data-stu-id="0497b-105">ICM\_DRAW\_START message</span></span>

<span data-ttu-id="0497b-106">Die **ICM \_ Draw- \_ Start** Meldung benachrichtigt einen renderingtreiber, seine interne Uhr für die zeitliche Steuerung von Zeichnungs Frames zu starten.</span><span class="sxs-lookup"><span data-stu-id="0497b-106">The **ICM\_DRAW\_START** message notifies a rendering driver to start its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="0497b-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawstart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="0497b-107">You can send this message explicitly or by using the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) macro.</span></span>


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="0497b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0497b-108">Return Value</span></span>

<span data-ttu-id="0497b-109">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0497b-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0497b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0497b-110">Remarks</span></span>

<span data-ttu-id="0497b-111">Diese Meldung wird von Hardware verwendet, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.</span><span class="sxs-lookup"><span data-stu-id="0497b-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="0497b-112">Wenn der Treiber diese Nachricht empfängt, sollte er mit dem Rendern von Daten mit der Rate beginnen, die mit der [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) -Meldung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0497b-112">When the driver receives this message, it should start rendering data at the rate specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="0497b-113">Die **ICM \_ Draw- \_ Start** -und [**ICM \_ Draw- \_ halte**](icm-draw-stop.md) Meldungen werden nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="0497b-113">The **ICM\_DRAW\_START** and [**ICM\_DRAW\_STOP**](icm-draw-stop.md) messages do not nest.</span></span> <span data-ttu-id="0497b-114">Wenn Ihr Treiber den **ICM- \_ Zeichnen- \_ Start** empfängt, bevor das Rendering mit **ICM \_ Draw- \_ Stopp** beendet wird, sollte das Rendering mit neuen Parametern neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="0497b-114">If your driver receives **ICM\_DRAW\_START** before rendering is stopped with **ICM\_DRAW\_STOP**, it should restart rendering with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="0497b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0497b-115">Requirements</span></span>



| <span data-ttu-id="0497b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0497b-116">Requirement</span></span> | <span data-ttu-id="0497b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0497b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0497b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0497b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0497b-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0497b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0497b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0497b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0497b-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0497b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0497b-122">Header</span><span class="sxs-lookup"><span data-stu-id="0497b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0497b-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0497b-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0497b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0497b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0497b-125">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="0497b-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0497b-126">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="0497b-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





