---
title: ICM_DRAW_RENDERBUFFER Meldung (VFW. h)
description: Mit der ICM \_ Draw- \_ renderbuffer-Meldung wird ein renderingertreiber benachrichtigt, um die Frames zu zeichnen, die an ihn übermittelt wurden. Sie können diese Nachricht explizit oder mithilfe des icdrawrenderbuffer-Makros senden.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- ICM_DRAW_RENDERBUFFER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956935"
---
# <a name="icm_draw_renderbuffer-message"></a><span data-ttu-id="abbf5-105">ICM \_ Draw- \_ renderbuffer-Meldung</span><span class="sxs-lookup"><span data-stu-id="abbf5-105">ICM\_DRAW\_RENDERBUFFER message</span></span>

<span data-ttu-id="abbf5-106">Mit der **ICM Draw-renderbuffer-Meldung wird ein \_ \_ renderingertreiber** benachrichtigt, um die Frames zu zeichnen, die an ihn übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="abbf5-106">The **ICM\_DRAW\_RENDERBUFFER** message notifies a rendering driver to draw the frames that have been passed to it.</span></span> <span data-ttu-id="abbf5-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawrenderbuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="abbf5-107">You can send this message explicitly or by using the [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) macro.</span></span>


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="abbf5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abbf5-108">Return Value</span></span>

<span data-ttu-id="abbf5-109">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="abbf5-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abbf5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abbf5-110">Remarks</span></span>

<span data-ttu-id="abbf5-111">Verwenden Sie diese Meldung mit Hardware, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.</span><span class="sxs-lookup"><span data-stu-id="abbf5-111">Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="abbf5-112">Diese Meldung wird in der Regel verwendet, um einen Suchvorgang auszuführen, wenn der Treiber speziell angewiesen werden muss, jeden Video Frame, der an ihn übergeben wird, anzuzeigen, anstatt eine Sequenz von Video Frames zu spielen.</span><span class="sxs-lookup"><span data-stu-id="abbf5-112">This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="abbf5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abbf5-113">Requirements</span></span>



| <span data-ttu-id="abbf5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abbf5-114">Requirement</span></span> | <span data-ttu-id="abbf5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="abbf5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="abbf5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abbf5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="abbf5-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abbf5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="abbf5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abbf5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="abbf5-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abbf5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="abbf5-120">Header</span><span class="sxs-lookup"><span data-stu-id="abbf5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="abbf5-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="abbf5-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abbf5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abbf5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abbf5-123">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="abbf5-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="abbf5-124">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="abbf5-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





