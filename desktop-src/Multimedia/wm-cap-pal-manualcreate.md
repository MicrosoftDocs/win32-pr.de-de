---
title: WM_CAP_PAL_MANUALCREATE Meldung (VFW. h)
description: Die "WM \_ Cap \_ PAL \_ manualcreate"-Meldung fordert an, dass der Erfassungs Treiber manuell Video Frames erstellt und eine neue Palette erstellt. Sie können diese Nachricht explizit oder mithilfe des cappalettemanual-Makros senden.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740960"
---
# <a name="wm_cap_pal_manualcreate-message"></a><span data-ttu-id="1437a-105">WM \_ Cap \_ PAL \_ manualcreate-Meldung</span><span class="sxs-lookup"><span data-stu-id="1437a-105">WM\_CAP\_PAL\_MANUALCREATE message</span></span>

<span data-ttu-id="1437a-106">Die " **WM \_ Cap \_ PAL \_ manualcreate** "-Meldung fordert an, dass der Erfassungs Treiber manuell Video Frames erstellt und eine neue Palette erstellt.</span><span class="sxs-lookup"><span data-stu-id="1437a-106">The **WM\_CAP\_PAL\_MANUALCREATE** message requests that the capture driver manually sample video frames and create a new palette.</span></span> <span data-ttu-id="1437a-107">Sie können diese Nachricht explizit oder mithilfe des [**cappalettemanual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="1437a-107">You can send this message explicitly or by using the [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) macro.</span></span>


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="1437a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1437a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1437a-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*in den Griff*</span><span class="sxs-lookup"><span data-stu-id="1437a-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span></span>
</dt> <dd>

<span data-ttu-id="1437a-110">Palettenhistogrammflag.</span><span class="sxs-lookup"><span data-stu-id="1437a-110">Palette histogram flag.</span></span> <span data-ttu-id="1437a-111">Legen Sie diesen Parameter für jeden Frame, der zum Erstellen der optimalen Palette gehört, auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="1437a-111">Set this parameter to **TRUE** for each frame included in creating the optimal palette.</span></span> <span data-ttu-id="1437a-112">Nachdem der letzte Frame erfasst wurde, legen Sie diesen Parameter auf " **false** " fest, um die optimale Palette zu berechnen und an den Erfassungs Treiber zu senden.</span><span class="sxs-lookup"><span data-stu-id="1437a-112">After the last frame has been collected, set this parameter to **FALSE** to calculate the optimal palette and send it to the capture driver.</span></span>

</dd> <dt>

<span data-ttu-id="1437a-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*icolors*</span><span class="sxs-lookup"><span data-stu-id="1437a-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="1437a-114">Anzahl der Farben in der Palette.</span><span class="sxs-lookup"><span data-stu-id="1437a-114">Number of colors in the palette.</span></span> <span data-ttu-id="1437a-115">Der Maximalwert für diesen Parameter ist 256.</span><span class="sxs-lookup"><span data-stu-id="1437a-115">The maximum value for this parameter is 256.</span></span> <span data-ttu-id="1437a-116">Dieser Wert wird nur während der Auflistung des ersten Frames in einer Sequenz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1437a-116">This value is used only during collection of the first frame in a sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1437a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1437a-117">Return Value</span></span>

<span data-ttu-id="1437a-118">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1437a-118">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="1437a-119">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1437a-119">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="1437a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1437a-120">Requirements</span></span>



| <span data-ttu-id="1437a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1437a-121">Requirement</span></span> | <span data-ttu-id="1437a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1437a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1437a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1437a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1437a-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1437a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1437a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1437a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1437a-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1437a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1437a-127">Header</span><span class="sxs-lookup"><span data-stu-id="1437a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1437a-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1437a-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1437a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1437a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1437a-130">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="1437a-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1437a-131">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="1437a-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





