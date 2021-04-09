---
title: WM_CAP_DLG_VIDEODISPLAY Meldung (VFW. h)
description: In der \_ Meldung "WM Cap \_ DLG \_ Videodisplay" wird ein Dialogfeld angezeigt, in dem der Benutzer die Videoausgabe festlegen oder anpassen kann.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956436"
---
# <a name="wm_cap_dlg_videodisplay-message"></a><span data-ttu-id="6c559-104">WM- \_ Cap- \_ DLG- \_ Videoanzeige Meldung</span><span class="sxs-lookup"><span data-stu-id="6c559-104">WM\_CAP\_DLG\_VIDEODISPLAY message</span></span>

<span data-ttu-id="6c559-105">In der Meldung " **WM \_ Cap \_ DLG \_ Videodisplay** " wird ein Dialogfeld angezeigt, in dem der Benutzer die Videoausgabe festlegen oder anpassen kann.</span><span class="sxs-lookup"><span data-stu-id="6c559-105">The **WM\_CAP\_DLG\_VIDEODISPLAY** message displays a dialog box in which the user can set or adjust the video output.</span></span> <span data-ttu-id="6c559-106">Dieses Dialogfeld enthält möglicherweise Steuerelemente, die den Farbton, den Kontrast und die Helligkeit des angezeigten Bilds sowie die Ausrichtung der Schlüsselfarbe beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="6c559-106">This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment.</span></span> <span data-ttu-id="6c559-107">Sie können diese Nachricht explizit oder mithilfe des [**capdlgvideodisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="6c559-107">You can send this message explicitly or by using the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro.</span></span>


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="6c559-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c559-108">Return Value</span></span>

<span data-ttu-id="6c559-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="6c559-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c559-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c559-110">Remarks</span></span>

<span data-ttu-id="6c559-111">Die Steuerelemente in diesem Dialogfeld wirken sich nicht auf die digitalisierten Videodaten aus; Sie wirken sich nur auf die Ausgabe oder die erneute Anzeige des Videosignals aus.</span><span class="sxs-lookup"><span data-stu-id="6c559-111">The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.</span></span>

<span data-ttu-id="6c559-112">Das Dialogfeld Video Anzeige ist für jeden Aufzeichnungs Treiber eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6c559-112">The Video Display dialog box is unique for each capture driver.</span></span> <span data-ttu-id="6c559-113">Einige Erfassungs Treiber unterstützen möglicherweise keine Video Anzeige (Dialogfeld).</span><span class="sxs-lookup"><span data-stu-id="6c559-113">Some capture drivers might not support a Video Display dialog box.</span></span> <span data-ttu-id="6c559-114">Anwendungen können bestimmen, ob der Erfassungs Treiber diese Nachricht unterstützt, indem Sie den **fhasdlgvideodisplay** -Member der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6c559-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoDisplay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c559-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c559-115">Requirements</span></span>



| <span data-ttu-id="6c559-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c559-116">Requirement</span></span> | <span data-ttu-id="6c559-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6c559-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c559-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c559-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6c559-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c559-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6c559-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c559-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6c559-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c559-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6c559-122">Header</span><span class="sxs-lookup"><span data-stu-id="6c559-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c559-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c559-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c559-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c559-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c559-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="6c559-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6c559-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="6c559-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





