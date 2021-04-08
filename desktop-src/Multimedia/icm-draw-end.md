---
title: ICM_DRAW_END Meldung (VFW. h)
description: Die ICM- \_ Meldung zum Zeichnen des \_ Endes benachrichtigt einen renderingtreiber, das aktuelle Bild auf dem Bildschirm zu dekomprimieren und Ressourcen freizugeben, die für das Dekomprimieren und zeichnen reserviert wurden. Sie können diese Nachricht explizit oder mithilfe des icdrawend-Makros senden.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741961"
---
# <a name="icm_draw_end-message"></a><span data-ttu-id="e6af8-105">ICM \_ - \_ zeichenendenachricht</span><span class="sxs-lookup"><span data-stu-id="e6af8-105">ICM\_DRAW\_END message</span></span>

<span data-ttu-id="e6af8-106">Die **ICM-Meldung zum \_ Zeichnen des \_ Endes** benachrichtigt einen renderingtreiber, das aktuelle Bild auf dem Bildschirm zu dekomprimieren und Ressourcen freizugeben, die für das Dekomprimieren und zeichnen reserviert wurden.</span><span class="sxs-lookup"><span data-stu-id="e6af8-106">The **ICM\_DRAW\_END** message notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing.</span></span> <span data-ttu-id="e6af8-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawend-**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e6af8-107">You can send this message explicitly or by using the [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macro.</span></span>


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e6af8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6af8-108">Return Value</span></span>

<span data-ttu-id="e6af8-109">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e6af8-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6af8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6af8-110">Remarks</span></span>

<span data-ttu-id="e6af8-111">Die [**ICM \_ Draw- \_ Begin**](icm-draw-begin.md) -und **ICM \_ Draw \_** -Meldungen werden nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="e6af8-111">The [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) and **ICM\_DRAW\_END** messages do not nest.</span></span> <span data-ttu-id="e6af8-112">Wenn der Treiber den **ICM- \_ Zeichnen- \_ Anfang** erhält, bevor die Dekomprimierung mit dem **ICM- \_ Zeichnungs \_ Ende** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet</span><span class="sxs-lookup"><span data-stu-id="e6af8-112">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6af8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6af8-113">Requirements</span></span>



| <span data-ttu-id="e6af8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6af8-114">Requirement</span></span> | <span data-ttu-id="e6af8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e6af8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e6af8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6af8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6af8-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6af8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e6af8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6af8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6af8-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6af8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e6af8-120">Header</span><span class="sxs-lookup"><span data-stu-id="e6af8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6af8-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6af8-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6af8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6af8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6af8-123">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="e6af8-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e6af8-124">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="e6af8-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





