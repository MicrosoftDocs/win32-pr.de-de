---
title: WM_CAP_PAL_AUTOCREATE Meldung (VFW. h)
description: Die "WM \_ Cap \_ PAL \_ AutoCreate"-Meldung fordert an, dass der Erfassungs Treiber Beispiel Video Frames erstellt und automatisch eine neue Palette erstellt. Sie können diese Nachricht explizit oder mithilfe des-Makros cappaletteauto senden.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340991"
---
# <a name="wm_cap_pal_autocreate-message"></a><span data-ttu-id="8c917-105">WM \_ Cap \_ PAL \_ AutoCreate-Meldung</span><span class="sxs-lookup"><span data-stu-id="8c917-105">WM\_CAP\_PAL\_AUTOCREATE message</span></span>

<span data-ttu-id="8c917-106">Die " **WM \_ Cap \_ PAL \_ AutoCreate** "-Meldung fordert an, dass der Erfassungs Treiber Beispiel Video Frames erstellt und automatisch eine neue Palette erstellt.</span><span class="sxs-lookup"><span data-stu-id="8c917-106">The **WM\_CAP\_PAL\_AUTOCREATE** message requests that the capture driver sample video frames and automatically create a new palette.</span></span> <span data-ttu-id="8c917-107">Sie können diese Nachricht explizit oder mithilfe des-Makros [**cappaletteauto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) senden.</span><span class="sxs-lookup"><span data-stu-id="8c917-107">You can send this message explicitly or by using the [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) macro.</span></span>


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="8c917-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c917-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c917-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="8c917-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="8c917-110">Anzahl der zu Stichproben enden Frames.</span><span class="sxs-lookup"><span data-stu-id="8c917-110">Number of frames to sample.</span></span>

</dd> <dt>

<span data-ttu-id="8c917-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*icolors*</span><span class="sxs-lookup"><span data-stu-id="8c917-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="8c917-112">Anzahl der Farben in der Palette.</span><span class="sxs-lookup"><span data-stu-id="8c917-112">Number of colors in the palette.</span></span> <span data-ttu-id="8c917-113">Der Maximalwert für diesen Parameter ist 256.</span><span class="sxs-lookup"><span data-stu-id="8c917-113">The maximum value for this parameter is 256.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c917-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c917-114">Return Value</span></span>

<span data-ttu-id="8c917-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="8c917-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="8c917-116">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8c917-116">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c917-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c917-117">Remarks</span></span>

<span data-ttu-id="8c917-118">Die Videosequenz für Stichproben sollte alle gewünschten Farben in der Palette enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c917-118">The sampled video sequence should include all the colors you want in the palette.</span></span> <span data-ttu-id="8c917-119">Um die beste Palette zu erhalten, müssen Sie möglicherweise die gesamte Sequenz anstelle eines Teils davon abgleichen.</span><span class="sxs-lookup"><span data-stu-id="8c917-119">To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c917-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c917-120">Requirements</span></span>



| <span data-ttu-id="8c917-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c917-121">Requirement</span></span> | <span data-ttu-id="8c917-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8c917-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8c917-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c917-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8c917-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c917-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8c917-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c917-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8c917-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c917-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8c917-127">Header</span><span class="sxs-lookup"><span data-stu-id="8c917-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c917-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c917-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c917-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c917-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c917-130">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="8c917-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="8c917-131">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="8c917-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





