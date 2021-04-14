---
title: ICM_DRAW_WINDOW Meldung (VFW. h)
description: Die ICM- \_ Meldung zum Zeichnen des \_ Fensters benachrichtigt einen renderingtreiber, dass das für die ICM Draw-BEGIN-Meldung angegebene Fenster \_ \_ neu gezeichnet werden muss.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- ICM_DRAW_WINDOW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476242"
---
# <a name="icm_draw_window-message"></a><span data-ttu-id="a058e-104">ICM- \_ Zeichnungs \_ Fenster Meldung</span><span class="sxs-lookup"><span data-stu-id="a058e-104">ICM\_DRAW\_WINDOW message</span></span>

<span data-ttu-id="a058e-105">Die **ICM-Meldung zum \_ Zeichnen des \_ Fensters** benachrichtigt einen renderingtreiber, dass das für die [**ICM \_ Draw- \_ Begin**](icm-draw-begin.md) -Meldung angegebene Fenster neu gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="a058e-105">The **ICM\_DRAW\_WINDOW** message notifies a rendering driver that the window specified for the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message needs to be redrawn.</span></span> <span data-ttu-id="a058e-106">Das Fenster wurde verschoben oder vorübergehend verdeckt.</span><span class="sxs-lookup"><span data-stu-id="a058e-106">The window has moved or become temporarily obscured.</span></span> <span data-ttu-id="a058e-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawwindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="a058e-107">You can send this message explicitly or by using the [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) macro.</span></span>


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="a058e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a058e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a058e-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="a058e-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="a058e-110">Zeiger auf das Ziel Rechteck in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="a058e-110">Pointer to the destination rectangle in screen coordinates.</span></span> <span data-ttu-id="a058e-111">Wenn dieser Parameter auf ein leeres Rechteck zeigt, sollte das Zeichnen deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a058e-111">If this parameter points to an empty rectangle, drawing should be turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a058e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a058e-112">Return Value</span></span>

<span data-ttu-id="a058e-113">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a058e-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a058e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a058e-114">Remarks</span></span>

<span data-ttu-id="a058e-115">Diese Meldung wird von Hardware unterstützt, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.</span><span class="sxs-lookup"><span data-stu-id="a058e-115">This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="a058e-116">Videoüberlagerungs Treiber verwenden diese Nachricht, um zu zeichnen, wenn das Fenster verdeckt oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="a058e-116">Video-overlay drivers use this message to draw when the window is obscured or moved.</span></span> <span data-ttu-id="a058e-117">Wenn ein für den [**ICM- \_ Zeichnen- \_ Anfang**](icm-draw-begin.md) angegebener Fenster vollständig von anderen Fenstern ausgeblendet wird, ist das Ziel Rechteck leer.</span><span class="sxs-lookup"><span data-stu-id="a058e-117">When a window specified for [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) is completely hidden by other windows, the destination rectangle is empty.</span></span> <span data-ttu-id="a058e-118">Treiber sollten Video Überlagerungs Hardware deaktivieren, wenn diese Bedingung auftritt.</span><span class="sxs-lookup"><span data-stu-id="a058e-118">Drivers should turn off video-overlay hardware when this condition occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a058e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a058e-119">Requirements</span></span>



| <span data-ttu-id="a058e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a058e-120">Requirement</span></span> | <span data-ttu-id="a058e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a058e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a058e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a058e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a058e-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a058e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a058e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a058e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a058e-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a058e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a058e-126">Header</span><span class="sxs-lookup"><span data-stu-id="a058e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a058e-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a058e-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a058e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a058e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a058e-129">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="a058e-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a058e-130">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="a058e-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





