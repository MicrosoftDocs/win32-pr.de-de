---
title: ICM_DRAW_STOP_PLAY Meldung (VFW. h)
description: Durch die ICM \_ Draw- \_ \_ Wiedergabe Meldung wird ein renderingerber benachrichtigt, wenn ein Wiedergabe Vorgang beendet ist. Sie können diese Nachricht explizit oder mithilfe des icdrawstopplay-Makros senden.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- ICM_DRAW_STOP_PLAY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106551"
---
# <a name="icm_draw_stop_play-message"></a><span data-ttu-id="264b5-105">ICM \_ Draw \_ - \_ Wiedergabe Meldung</span><span class="sxs-lookup"><span data-stu-id="264b5-105">ICM\_DRAW\_STOP\_PLAY message</span></span>

<span data-ttu-id="264b5-106">Durch die **ICM \_ Draw- \_ \_ Wiedergabe** Meldung wird ein renderingerber benachrichtigt, wenn ein Wiedergabe Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="264b5-106">The **ICM\_DRAW\_STOP\_PLAY** message notifies a rendering driver when a play operation is complete.</span></span> <span data-ttu-id="264b5-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawstopplay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="264b5-107">You can send this message explicitly or by using the [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) macro.</span></span>


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="264b5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="264b5-108">Return Value</span></span>

<span data-ttu-id="264b5-109">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="264b5-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="264b5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="264b5-110">Remarks</span></span>

<span data-ttu-id="264b5-111">Verwenden Sie diese Meldung, wenn der Wiedergabe Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="264b5-111">Use this message when the play operation is complete.</span></span> <span data-ttu-id="264b5-112">Verwenden Sie die [**ICM \_ Draw \_**](icm-draw-stop.md) -Nachricht zum Beenden der zeitlichen Steuerung.</span><span class="sxs-lookup"><span data-stu-id="264b5-112">Use the [**ICM\_DRAW\_STOP**](icm-draw-stop.md) message to end timing.</span></span>

## <a name="requirements"></a><span data-ttu-id="264b5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="264b5-113">Requirements</span></span>



| <span data-ttu-id="264b5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="264b5-114">Requirement</span></span> | <span data-ttu-id="264b5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="264b5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="264b5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="264b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="264b5-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="264b5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="264b5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="264b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="264b5-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="264b5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="264b5-120">Header</span><span class="sxs-lookup"><span data-stu-id="264b5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="264b5-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="264b5-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="264b5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="264b5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="264b5-123">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="264b5-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="264b5-124">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="264b5-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





