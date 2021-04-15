---
title: ICM_DRAW_STOP Meldung (VFW. h)
description: Mit der ICM \_ Draw- \_ Meldung wird ein renderingertreiber benachrichtigt, um die interne Uhr für die zeitliche Steuerung von Zeichnungs Frames anzuhalten. Sie können diese Nachricht explizit oder mithilfe des icdrawstopemakros senden.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476245"
---
# <a name="icm_draw_stop-message"></a><span data-ttu-id="99120-105">ICM- \_ Zeichnungs \_ Ende (Meldung)</span><span class="sxs-lookup"><span data-stu-id="99120-105">ICM\_DRAW\_STOP message</span></span>

<span data-ttu-id="99120-106">Mit der **ICM \_ Draw \_** -Meldung wird ein renderingertreiber benachrichtigt, um die interne Uhr für die zeitliche Steuerung von Zeichnungs Frames anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="99120-106">The **ICM\_DRAW\_STOP** message notifies a rendering driver to stop its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="99120-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawstopemakros**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) senden.</span><span class="sxs-lookup"><span data-stu-id="99120-107">You can send this message explicitly or by using the [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) macro.</span></span>


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="99120-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99120-108">Return Value</span></span>

<span data-ttu-id="99120-109">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="99120-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99120-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99120-110">Remarks</span></span>

<span data-ttu-id="99120-111">Diese Meldung wird von Hardware verwendet, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.</span><span class="sxs-lookup"><span data-stu-id="99120-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="99120-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99120-112">Requirements</span></span>



| <span data-ttu-id="99120-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99120-113">Requirement</span></span> | <span data-ttu-id="99120-114">Wert</span><span class="sxs-lookup"><span data-stu-id="99120-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="99120-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99120-115">Minimum supported client</span></span><br/> | <span data-ttu-id="99120-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99120-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="99120-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99120-117">Minimum supported server</span></span><br/> | <span data-ttu-id="99120-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99120-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="99120-119">Header</span><span class="sxs-lookup"><span data-stu-id="99120-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="99120-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="99120-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99120-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99120-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99120-122">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="99120-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="99120-123">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="99120-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





