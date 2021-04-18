---
title: ICM_DRAW_FLUSH Meldung (VFW. h)
description: Mit der ICM \_ Draw \_ Flush-Meldung wird ein renderingertreiber benachrichtigt, um den Inhalt aller Bild Puffer zu rendern, die darauf warten, gezeichnet zu werden. Sie können diese Nachricht explizit oder mithilfe des icdrawflush-Makros senden.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- ICM_DRAW_FLUSH-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344676"
---
# <a name="icm_draw_flush-message"></a><span data-ttu-id="f3423-105">ICM-Zeichnungs Leerungs \_ \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="f3423-105">ICM\_DRAW\_FLUSH message</span></span>

<span data-ttu-id="f3423-106">Mit der **ICM \_ Draw \_ Flush** -Meldung wird ein renderingertreiber benachrichtigt, um den Inhalt aller Bild Puffer zu rendern, die darauf warten, gezeichnet zu werden.</span><span class="sxs-lookup"><span data-stu-id="f3423-106">The **ICM\_DRAW\_FLUSH** message notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn.</span></span> <span data-ttu-id="f3423-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawflush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="f3423-107">You can send this message explicitly or by using the [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) macro.</span></span>


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f3423-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3423-108">Return Value</span></span>

<span data-ttu-id="f3423-109">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f3423-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3423-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3423-110">Remarks</span></span>

<span data-ttu-id="f3423-111">Diese Meldung wird nur von Hardware verwendet, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.</span><span class="sxs-lookup"><span data-stu-id="f3423-111">This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3423-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3423-112">Requirements</span></span>



| <span data-ttu-id="f3423-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3423-113">Requirement</span></span> | <span data-ttu-id="f3423-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f3423-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3423-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3423-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f3423-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3423-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3423-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3423-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f3423-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3423-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3423-119">Header</span><span class="sxs-lookup"><span data-stu-id="f3423-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3423-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3423-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3423-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3423-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3423-122">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="f3423-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f3423-123">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="f3423-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





